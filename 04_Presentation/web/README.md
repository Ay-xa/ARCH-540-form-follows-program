# GP1 Progress Review 1 — 网页版（scroll-driven page）

日期：2026-10-27。对应 Drive 里的 `Presentation Draft.pdf`（18 页）和 `GP1_Progress_Review_1_Outline.md` 第 6 稿英文版。

## 怎么打开

- 直接双击 `index.html` 就能看（照片在 `assets/`，工具截图从 `../screenshots/` 读）。
- 想用本地服务器：在仓库根目录运行 `python -m http.server 8767`，再开 `http://localhost:8767/Assignment_2/04_Presentation/web/index.html`。
- 字体（Newsreader、Schibsted Grotesk）从 Google Fonts 加载；没网时退回系统字体，其它功能不受影响。没有用任何动画库。

## 页面结构（和 PDF 页序一致，2026-10-28 改）

| 段 | 对应 PDF | 左栏文字 | 右边舞台里发生什么 |
|---|---|---|---|
| 开场 | p1 | 标题、设问 | 桥下照片：底图是新给的干天照片（`bridge_dry_aligned.jpg`，用 14 个对应点做了透视变形，对齐到雨天标注图的画框），上面叠雨天标注图。两种看法同时可用：跟着光标走的柔边圆圈（半径是画幅宽的 36%），和一根默认停在左边缘的推拉条，拖它（鼠标、触摸、方向键都行）雨天图就从左边填进来 |
| 照片带 | （新增） | 一行引言 + 署名 | 首页照片下方一条照片带，随页面竖向滚动 1:1 横向滑动（往回滚就往回退，循环无缝）：你给的两张 + 温哥华市 Shape Your City 弹出广场相册里选的 6 张（14th & Granville、18th & Cambie、Carrall、Bute & Alberni、Cambie Bridge North、Burrard Bridge North） |
| Problem | p2–3 | 问题 + 揭示问题的文献 | 一道墙升起："外面是天气，里面是一个设定" |
| Thesis | p4 | 命题、研究问题 | 墙裂成五段色带 |
| Method, and where I am | p5–6 | 两段短文字（Tactical sequence 已删） | **路线图第一次完整出现**，逐项画出，不高光；段末出现红色虚线框 CURRENT STAGE，框住 Critique + Research |
| Critique | p7–9 | Opportunity、Claim、五段定义 | 开头路线图绿色底板收缩到 **Critique**，只留 Logical Argument 标签；然后切到五张剖面逐段加围合 |
| Direction | p10 | 因果方向、怎么检验、结果、愿景（Critique 段到 Vision 结束） | 韦恩图合拢：Vernacular Intelligence、host / support / derive、三个卫星圆 |
| Premises from the literature | p11–12 | 三个子问题及各自方法 | 开头路线图高光 **Research**（四个标签）；然后韦恩图的三个圆分开，变成 Activity / Space / Decision |
| Activity | p13–15 | 前提 P1、P2、P3 连成一段（Threshold 标题已去掉），PDF 里的红色句子做成 `<mark>`，滚到屏幕下三分之一处时像马克笔一样从左划到右，字变红 | Activity 圆放大：PET 范围、+4 °C、容忍范围变宽、代谢率小人 |
| Space | p16 | 策略积累 + 三张手稿说明 | Space 圆：8 个线稿；后半段 kit-of-parts 手稿从左到右揭开 |
| Decision | p17–18 | 规则 R1–R8（可点） | 开头路线图高光 **Translation**（三个标签）；然后 Decision 圆 + 五段色带标冬 / 夏 |
| Test | （大纲第 7 节） | 工具做三件事、A–D 结果、缺口 | 结果柱状图 + 两张工具截图 |
| What comes next | （大纲第 8–9 节） | 研究继续：加强活动与空间的联系、更多案例、丰富 kit-of-parts；设计原则；两个问题；打开工具 | 路线图高光 Research（不是 GP2）；再回到韦恩图 + 结束语 |

左侧竖栏是路线图的文字版，随滚动高亮当前所在的步骤（"I am here" 一行已删）。三张图都是按原图重画成 SVG（路线图、韦恩图）或直接用原图（手稿），所以能随滚动变化。

## 为什么浏览器面板里照片会不见

Claude 的浏览器面板有时把 `index.html` 当成一段内嵌文本（地址栏是 `data:`）打开，而不是从文件夹打开，这时相对路径的照片和截图都找不到。双击文件（`file://`）或用本地服务器打开都正常。首页现在有保护：照片加载不到时显示一行说明，不留空框。

## 两个已做的决定

1. **五段而不是四段。** PDF 第 9 页的渐变图是四段（没有 protected），但大纲第 6 稿、研究策略文件和规则 R1 都是五段，网页按五段画。
2. **文字一律取自大纲英文版**，数字和文献名没有改写。阈值都是借用的，页脚写明。
3. **字号层级照 PDF**：页标题（衬线，绿色底条，如 The literature that revealed the problem）> 小节标题（粗体无衬线，如 P1 The binary is not necessary）> 正文 16px、列表 15px。加粗的引导词（City of Vancouver documents:）降到半粗。

## 照片带的版权

6 张来自 City of Vancouver 的 Shape Your City 相册（https://www.shapeyourcity.ca/pop-up-plazas/photos/20078），不是自由许可，页面上注明"City of Vancouver, Shape Your City, reproduced for an academic review"。只在课程评图和论文里用；公开发布前要确认市政府的使用条款。清单和来源在 `assets/plazas/credits.json`。

## 没做的

- 没做中文切换；评图对象是英文评委。
- 没做深色模式。
- 原始参考图存了一份在 `assets/vernacular_intelligence_ref.jpg`（韦恩图原稿），网页里用的是重画的 SVG。
- 首页两张照片不是同一张底片（雨天图是重新生成的，人和构图都不同），所以只能对齐拱、桥墩、花坛、桌子，人物对不上是正常的。对齐脚本在会话 scratchpad 里，没有放进仓库。
- 右边舞台靠滚动位置驱动，同一位置永远是同一画面；系统设了"减少动效"时直接跳到每段的终态。

## 独立链接（2026-10-29）

发布在 claude.ai 的 Artifact：https://claude.ai/artifact/DaftdihfHwQyDw2pnBfhSr（第 2 版）。链接默认私密，要让别人打开，需在页面右上角 Share 菜单里开放。

打包方式：把 `index.html` 去掉外壳（发布平台自带 doctype / html / head / body），`../screenshots/` 的两张工具截图搬到页面旁边的 `screenshots/`，去掉指向本地原型的 Open the tool 按钮；11 张图和 2 张截图一起上传，共 3.2 MB。网页本身没有改内容。再发布时重复这一步即可。

同一天顺手修了窄屏的一个问题：导航栏一行不换行会把整页撑宽，`.layout` 的窄屏列改成 `minmax(0,1fr)`。
