# anime.js 动效学习笔记（Motion Notes）

日期：2026-10-22。来源：https://animejs.com/ 首页与文档（版本 4.5.0，作者 Julian Garnier，MIT 免费）。状态：**学习笔记，还没有改工具**。目的是弄清这个网站的动效为什么好、它靠什么做到，以及放进我们的工具（`02_Prototypes/Version_01/index.html`）时该怎么接。

---

## 1. 一句话

anime.js 是一个"动画引擎"（animation engine）：你告诉它"把这个数从 A 变到 B，花多久，用什么节奏"，它负责每一帧算出中间值。它不管画面长什么样，只管**数怎么变**。所以它既能动网页上的按钮、文字、SVG 线条，也能动 three.js 里的体块位置、颜色、相机。这一点对我们很重要：我们的三维场景是 three.js 画的，anime.js 可以直接驱动它。

---

## 2. 网站本身为什么好看（动效的几条原则）

逐段看了首页，它的"好"不是花哨，而是几条一致的做法：

| 做法 | 首页上的样子 | 对我们的启发 |
|---|---|---|
| **滚动驱动**（scroll-driven） | 相机镜头是一个 three.js 三维模型（glTF），随页面滚动转动、拆开、合拢；你停它就停，倒着滚它倒着放 | "进度"不一定靠时间，可以靠使用者的操作（滚动、拖滑块、按下一步）。我们的六个步骤天然是一条进度 |
| **节奏曲线**（easing） | 几乎所有动作都是"快起慢停"（`out(3)`、`outQuart`、`outQuint`）或"慢起快中慢停"（`inOut(2–4)`），很少匀速 | 我们现有的"晕染"已经用了慢起慢停；其它瞬间切换的地方（换方案、换步骤、变淡）可以同样处理 |
| **错开出场**（stagger） | 一片点阵不是一起动，而是从中心向外一圈圈延迟，看起来像涟漪 | 房间一个个落位、体块一块块升起、流线一条条点亮，比"一下全出来"好读 |
| **时间线**（timeline） | 时钟的小刻度和指针是同一条时间线上的两段，位置用 `'<'`（接在前一段末尾）这种相对写法排 | "体块升起 → 楼板铺开 → 房间落位 → 流线流动"可以排成一条时间线，顺序和重叠都写在一处 |
| **弹簧**（spring） | 拖圆点松手后会弹两下再停 | 推拉体块松手时让面轻轻弹回整数，比硬停自然 |
| **克制** | 深色底、单一橙红强调色、动作短（几百毫秒）、一次只动一个主体 | 和我们"白纸 + 一个主色"的风格一致，不需要为了动效换风格 |

首页的技术构成（在浏览器里核实过）：一个 WebGL 画布（three.js，镜头模型用 glTF）+ 五个小的 2D 画布（各功能示例）+ 很多 SVG。首页脚本里 `spring` 出现 14 次、`seek`（跳到时间线某处）8 次、`three` 37 次；滚动是把时间线的进度"跳"到滚动位置，再用弹簧把它抹平，所以手感是跟手又不生硬。

---

## 3. 它提供的零件（按对我们有用的程度排序）

### 3.1 `animate(target, { ... })` —— 把数变过去
- `target` 可以是网页元素、CSS 选择器、**普通 JS 对象**（例如 `mesh.position`、`material`、`BLEED.uR`）。
- 常用参数：`duration`（毫秒）、`delay`、`ease`（节奏名）、`loop`、`alternate`（来回）、`autoplay`。
- 每个属性可以单独给参数：`rotate: { from: '-1turn', delay: 0 }`。
- 关键帧（keyframes）：`x: [0, 100, 200]`，或 `keyframes: { '0%': {...}, '50%': {...}, '100%': {...} }`。
- 回调：`onUpdate`、`onRender`、`onComplete`、`onBegin`。**我们的场景是"要画才画"（`draw()`），不是一直在转的循环，所以每个动画都要在 `onUpdate` 里叫一次 `draw()`，否则数变了画面不动。**
- 控制：`play() / pause() / reverse() / seek(ms) / restart() / cancel()`。

### 3.2 `createTimeline()` —— 排顺序
```js
createTimeline({ defaults: { duration: 600, ease: 'outQuart' } })
  .label('start')
  .add(massA.position, { y: 0 }, 'start')          // 和 'start' 同时
  .add(slabs,          { opacity: 1 }, '<')         // 接在上一段末尾
  .add(roomLabels,     { opacity: 1 }, '<<+=150')   // 上一段开始后 150 ms
  .call(() => draw(), '<');                          // 到这一刻调一个函数
```
位置写法：绝对毫秒 `500`、`'+=100'`、`'-=100'`、`'<'`（上一段末尾）、`'<<'`（上一段开头）、标签名、`stagger(10)`。
整条时间线可以 `seek()`、`reverse()`、`pause()`，这就是"把六个步骤做成一条可以前后拖的进度"的基础。

### 3.3 `stagger(value, { from, grid, axis, ease, start })` —— 错开
- `delay: stagger(50)`：第 n 个目标晚 50·n 毫秒。
- `stagger([1, .1])`：把值从 1 到 0.1 分摊给各目标。
- `from: 'center' | 'first' | 'last' | 索引`，`grid: [cols, rows]` 按二维距离算延迟（涟漪）。
- 也能用在时间线位置上：`.add('.dot', {...}, stagger(200))`。
- 对我们：房间按"离门厅的距离"或"从南到北"依次落位，用 `from` + 自定义顺序就行。

### 3.4 节奏（easings）
- 名称：`linear`、`in/out/inOut/outIn` 后接 `Quad/Cubic/Quart/Quint/Sine/Expo/Circ/Bounce/Back/Elastic`，或带参数 `out(3)`、`inOut(2.4)`。
- 弹簧：`spring({ bounce: .25, duration: 350 })`（感知参数，推荐）或 `spring({ stiffness, damping, mass })`（物理参数）。弹簧会覆盖 `duration`。
- 网站有一个"Easings editor"可以拖着看曲线：https://animejs.com/easings-editor（从首页底部 EASINGS EDITOR 进）。
- 建议我们固定两三种：出场 `outQuart`、变淡 `outSine`、推拉松手 `spring({ bounce: .2 })`。

### 3.5 `onScroll()` —— 滚动当进度
`autoplay: onScroll({ container, target, enter, leave, sync: true | 0.25 | 'play pause' })`。`sync: true` 是进度严格跟滚动；`sync: .25` 是带阻尼跟随（首页镜头那种手感）。我们的工具不是长页面，暂时用处不大；但"把进度交给某个滑块"的思路一样，可以用 `seek()` 自己接。

### 3.6 Three.js 适配器（adapter，4.5.0 新）
- `import 'animejs/adapters/three'` 之后，可以直接 `animate(mesh, { x: 100, rotateY: 30, opacity: .5, color: '#ff8800' })`，它自动写到 `mesh.position.x`、`mesh.rotation.y`（按**度**）、`mesh.material.opacity`、`mesh.material.color`。
- `getInstances(instancedMesh)` 可以逐个动 InstancedMesh 的每个实例（我们的树是 InstancedMesh）。
- 注意事项（文档 gotchas）：
  - 要动 `opacity` 的材质必须 `transparent = true`（我们大部分材质已经是）。
  - 一个材质被几个网格共用时，动它会一起动；要单独动就每个网格克隆材质。
  - `Group` 没有材质，动 group 的 opacity 没效果，要把子网格数组当目标。
  - **three 必须只有一份实例**：通过 CDN 用时要让适配器里的 `three` 走我们 importmap 的那份（见第 5 节）。
- 不用适配器也能动：`animate(mesh.position, { y: 0 })`、`animate(mesh.material, { opacity: 1 })` 本来就是"普通 JS 对象"。先用这种，最稳。

### 3.7 其它（现在用不上，记一下）
`createDraggable`（拖拽、吸附、甩出）、SVG 工具（`createDrawable` 画线、`morphTo` 形变、`createMotionPath` 沿路径走）、`splitText`（逐字出场）、`layout`（元素换位置时自动补间）、`createScope`（按屏幕宽度切换动画）、`waapi.animate`（更轻的 3 KB 版，只动 CSS）。
二维平面图是 SVG 画的（`renderPlan()`），以后要"房间轮廓画出来""剖面线一笔笔描"可以用 `createDrawable`。

---

## 4. 和我们工具现状的对照

现在工具里的动效（都在 `index.html`）：

| 现有 | 做法 | 用 anime.js 会怎样 |
|---|---|---|
| 展示步的"晕染"（`playBleed`） | 自己写 `requestAnimationFrame` + 手算 `t*t*(3-2t)` | `animate(BLEED.uR, { value: [r0, R], duration: 6500, ease: 'inOutSine', onUpdate: draw })`，三行 |
| 风的粒子（`windLoop`） | 自己的物理循环 | **不换**。它是模拟不是补间，anime.js 不适合 |
| 流线短划（`flowLoop`） | 自己的循环，按时间推相位 | 可换可不换；换成 `createTimer({ loop: true, onUpdate })` 只是统一管理，不一定更好 |
| 换步骤 `setStep(n)`、换体块方案、隔离一个体块时变淡 | 直接重建 `dyn` 组，瞬间切换 | **最值得做的地方**：旧的淡出（opacity → 0.1）、新的淡入 + 从地面升起（position.y 从 -0.5 → 0），房间按顺序 `stagger` 落位 |
| 推拉体块松手 | 直接定位 | `spring` 回弹到吸附值 |
| 网页面板（按钮、卡片） | CSS `@keyframes rise` | 保留 CSS；小东西不必上库 |

另外注意：工具里已有 `prefers-reduced-motion` 的处理（样式第 68 行）。anime.js 不会自动尊重这个设置，接进来时要在动画总开关里判断：减少动效时 `duration: 0` 或直接 `seek` 到末尾。

---

## 5. 怎么装（不用打包工具，和现在的 three 一样走 CDN）

工具现在用 importmap 引 three（`index.html` 第 4170 行）。加 anime.js 只需在 importmap 里加一行：

```html
<script type="importmap">{ "imports": {
  "three": "https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js",
  "three/addons/": "https://cdn.jsdelivr.net/npm/three@0.160.0/examples/jsm/",
  "animejs": "https://cdn.jsdelivr.net/npm/animejs@4.5.0/dist/bundles/anime.esm.min.js"
} }</script>
```
然后在模块脚本里 `import { animate, createTimeline, stagger, spring, utils } from "animejs";`。

- 版本固定写 `@4.5.0`（2026-10-22 核实：jsDelivr 与 esm.sh 都是 4.5.0；5.0 还是 beta，不用）。
- **只能有一份**：工具里平面过渡动画（`animatePlanDiff`，2026-10-22 晚）已经用 `import(...)` 从 jsDelivr 的 `anime.esm.min.js` 动态加载过一次；三维模块脚本里的 importmap 必须指向**同一个地址**，浏览器才会只加载一份、两处共用一个引擎。用 esm.sh 就会变成两份（两个引擎、多 27 KB）。
- 如果以后要用 three 适配器，用 `https://esm.sh/animejs@4.5.0/adapters/three?external=three`，`?external=three` 让它用我们 importmap 里的那份 three，避免"两份 three"的坑。
- 体积：核心约 27 KB（gzip 后更小），只 import 用到的部分；对一个单文件工具可以接受。
- 也有 UMD 版（`anime.umd.min.js`，全局 `anime` 对象），但我们已经是 ES module，不需要。
- **已验证（2026-10-22，在浏览器里实测）**：`https://esm.sh/animejs@4.5.0` 能加载，`animate / createTimeline / stagger / spring / utils / onScroll / createTimer / eases` 都在；`animate({ value: 10 }, { value: 100, duration: 300, ease: 'outQuart' })` 跑完后值是 100，`onUpdate` 每帧调用、`onComplete` 触发。
- 引擎默认 `pauseOnDocumentHidden: true`：标签页切到后台时自动暂停，回来再继续。这对我们是好事（不白耗电），但测试时要注意：页面不在前台，动画就不会走。

---

## 6. 建议的第一步（小、可撤回）

1. **先替换"晕染"**：把 `playBleed` 的手写循环换成 `animate`，行为不变，用来验证库接得通、`onUpdate: draw` 的模式对。**已做（2026-10-22）**：importmap 加了 `animejs`，`playBleed` 改为 `animate(BLEED.uR, { value: R, duration: 6500, ease: t => t*t*(3-2t), onUpdate: draw })`；实测半径 27 → 170 左右、6.5 秒收尾、中途退回第 5 步会停，和原来一致。
2. **换步骤的过渡**：`setStep` 时旧体块淡出 200 ms、新内容升起 400 ms（`outQuart`），房间按 `stagger(30)` 落位。只动 `dyn` 组里的网格，不碰数据和规则。**已做（2026-10-22）**：`setStep` 登记一次 `stepFxRequest()`，下一次 `rebuild` 把旧的一组整组挪到旁边淡出 0.22 秒（`outSine`），新的一组从地面下方 0.8 m 升起并淡入 0.48 秒（`outQuart`）；体块和标高框先出，功能房间和它们的名字按排布顺序每隔 28 ms 出一间（最多错开 18 间），中庭、核、流线、风在房间中段出。整条过渡用一个 `createTimer` 驱动，每帧只 `draw()` 一次（没有用一百多个 `animate` 各自重绘）。任何别的重建（推拉、改标高）会先 `stepFxFinish()` 立刻收尾。系统设了"减少动效"时跳过。实测 4→5 / 5→4 约 0.9 秒、113 个物件，5→6 和晕染同时开始，6→5 晕染正确停掉；截图 `04_Presentation/screenshots/2026-10-22_v01_step_transition_0/1/2.jpg`。
3. **方案 A/B/C/D 切换**：同一组体块从旧位置补间到新位置（而不是重建），看得出"哪里变了"。这一步要改重建逻辑，等 1、2 稳了再做。
4. 推拉松手的 `spring` 回弹：最后做，锦上添花。

每一步都只是"数怎么过渡"，不改任何规则、评分或数值（见 `Research_Strategy.md` 第 6 节）；动效是表达层，不影响模拟结果。

---

## 7. 文档索引（给以后查）
- 安装：https://animejs.com/documentation/getting-started/installation
- animate：https://animejs.com/documentation/animation ；关键帧：…/animation/keyframes ；JS 对象：…/animation/animatable-properties/javascript-object-properties
- 时间线：https://animejs.com/documentation/timeline ；位置写法：…/timeline/time-position
- stagger：https://animejs.com/documentation/utilities/stagger
- 节奏：https://animejs.com/documentation/easings/built-in-eases ；弹簧：…/easings/spring
- 滚动：https://animejs.com/documentation/events/onscroll
- Three.js 适配器：https://animejs.com/documentation/adapters/threejs-adapter ；注意事项：…/adapters/threejs-adapter/threejs-adapter-common-gotchas
- 引擎（执行顺序、帧率、页面隐藏时暂停）：https://animejs.com/documentation/engine
