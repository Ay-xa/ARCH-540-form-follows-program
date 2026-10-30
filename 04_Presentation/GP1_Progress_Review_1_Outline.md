# GP1 Progress Review #1 — 演讲大纲（第 6 稿，加 Chicago 脚注）

日期：2026-10-27。评图：2026-10-28 4:10pm，Room 4 ANNEX Small（门禁 27295#），评图人 James Huemoeller、Xun Liu。讲 ≤ 9 分钟，其余讨论。
作业要求见 Drive：`ARCH 548 GP1/Assignment 3  - Progress Review/ARCH-548_2025WT1_Assignment 3.pdf`。

**本稿依据：** 用户的 `Assignment 3  - Progress Review/演讲的逻辑.docx` 中的 **v2**（2026-10-27 15:06 存）是主干，顺序和措辞以它为准。我补的部分标 **〔补〕**，并写了补的原因；需要你确认的标 **〔待定〕**。
**前提（用户 2026-10-26 确认）：** thesis 是一个论证，工具是这个论证能运行的版本。在 GP1 里，工具是证明，不是成果本身。GP2 不设计真的建筑。
**来源标签：** A = 读过全文；B = 只看过摘要或网页。
**引用格式：** Chicago（notes-bibliography），每个引用文献的段落后加脚注；说明和待核项在中文版末尾，参考文献在全文末尾。
**英文版在本文件后半部分。** 逐页讲稿 `GP1_Progress_Review_1_Script.md` 还是按第 4 稿写的，等大纲定了再重写。

**和第 5 稿相比，v2 改了这些：**
1. 标题换成 "Just Enough: Conditioning as a Calibrated Gradient"。
2. Statement 从问句改为 **thesis statement**：一句开场设问加一句论点。删掉了 "How much conditioning is enough?" 和"另一种可能"那句。
3. 三个子问题（Activity / Space / Decision）挪到"前提"开头，每个注明方法，变成后面三段的路标。
4. 主张扩写了：开头加了"活动差异是没用上的设计机会"，后面加了空间策略、研究成果是"一套方法"、"从固定的房间走向随气候和活动演化的建筑"。
5. **新增一段"空间策略积累"**（case study，interpretive），放在工具之前。冬季花园、热辐射和心理调节（视觉）是新加的。
6. 原来第 7 段里的乡土手法和 Hou 的寒冷地区手法挪进了新的"空间策略积累"。"设计原则"一段只留你的一句话。

---

## 整体逻辑

```
问题（含"出发点"文献）→ Thesis statement + 研究问题
→ 方法 + 现在在哪一步 → 主张（五段渐变）
→ Activity：前提 P1–P3（借用的相关性文献，逻辑论证）
→ Space：空间策略积累（案例研究，interpretive）
→ Decision：规则 R1–R8 → 工具检验（simulation）→ 结果与缺口
→ 设计原则（kit-of-parts）
```

**文献出现两次，角色不同：** 在"问题"里，它让人看到现状哪里不对、哪里还没人做；在"前提"里，它支撑论证的每一步。**文献不负责"证实" thesis**，证实靠工具检验，以及以后的对照组和实测。

**v2 的结构比第 5 稿更顺：** 三个子问题现在正好对应后面连续三段：Activity → 前提，Space → 空间策略，Decision → 工具。听的人能跟着这条线走。

---

## 0. 标题 + 开场图（0:20）〔补开场图，作业要求〕
- **标题：** "Just Enough: Conditioning as a Calibrated Gradient"
- **开场图：** `Images for Presentation/Raw` 里冬天桥下冷清的公园（Burrard、Cambie）和夏天 W 18th & Cambie 的人群，左右并排。

## 1. 问题（1:15）
**叙述（你的原文）：**
- 温哥华的公共生活受天气影响很大。冬季多雨、低温，可能让某些公共活动难以持续。
- 与此同时，建筑通常用室内和室外之间一道明确的围护边界来组织环境控制。
- **第一个发现：不同活动对环境的需求不同。** 一个在跑步的人、一个在喝咖啡的人、一个长时间用电脑的人，需要的温度、风速、遮雨条件和环境稳定程度并不相同。
- **问题：** 为什么在建筑设计早期做功能布局时，很少直接利用不同活动对环境的适应能力，来决定一个空间需要多少保护？我们通常先定房间的位置、大小和功能，再想办法让它达到预期的环境条件。

**出发点文献（说明"现状哪里不对、哪里还没人做"）：**
- **温哥华市政文件：** 公众确实在要遮雨、带暖的停留空间。依据是《Hot Tea, Rain City》2018（约 1200 人参与、96 张反馈卡，定性），以及《Downtown Public Space Strategy》2021 提出的 "year-round"、"rain-friendly public spaces"。（A，`Vancouver_Documents_Round1.md`）[^c1]
- **A2 的乡土文献（Oliver、Turan）：** 建筑曾经是调和气候，而不是隔绝气候。[^c2]
- **Mora & Bean 2018：** ASHRAE 55 本身就是二分的。机械调节的建筑用 PMV，自然调节的建筑用适应性模型，中间没有过渡。适应性模型还要求室外平均 ≥ 10℃，温哥华约 11 月到 4 月不满足。（A）[^c3]
- **Hou 2025、Ma 2026：** 半室外空间的研究大多在湿热气候里做，考虑冬季温和多雨情况的研究几乎没有。这是空白。（A）[^c4]
- **工具类文献（Forma、AURA、Li 2026）：** 现有工具从形体算性能，或从平面算通风，没有一个把"活动需要多少防护"放进排布。这也是空白。（Forma B；AURA、Li 2026 A）[^c5]

**〔待定〕一处还没有来源：**
- **"我们通常先定房间、再考虑环境条件"：** 这是你的观察，目前只有间接佐证：Forma 的更新方向是把性能分析提前（B）；AURA 显示平面布局对室温的影响不小于窗户（A，预印本）。建议讲成 "typically"。主张里的英文句 "Architecture often treats environmental comfort as something provided to space after its organization" 也是同一个说法，评图人问"依据是什么"时要有准备。[^c6]

## 2. Thesis statement + 研究问题（0:45）
- **开场设问：**
  > What if conditioning is not a fixed property of a room, but a changing relationship between climate, activity, architecture, and season?
  - 原来的 "time" 已按你的决定改成 "season"，和工具目前分冬季、夏季一致。
- **Thesis statement：**
  > Conditioned space can be reinterpreted as a calibrated gradient of climatic protection and exposure, where activity-specific environmental needs and microclimatic conditions guide spatial arrangement and protection strategies.
  - 我数了是 27 个词，符合作业"≤ 35 词、一句话"的要求。原文句末没有句号，我加上了。
  - 它是 thesis，不是 topic：它提出了一个可以被反驳的主张。"can be" 语气偏弱，你之前说放哪句稍后再定，这里先照你的写。
- **Research question：**
  > How can activity-specific environmental requirements inform early-stage spatial organization to reduce the potential for over-conditioning while maintaining acceptable comfort and usability?
  - 原文 "over conditioning" 写成 "over-conditioning"。

## 3. 方法 + 现在在哪一步（0:30）〔补内容，作业要求 "declare where you are in the tactical sequence"；v2 只有标题〕
- 一句话讲方法：逻辑论证是主干；三个子问题各用一种方法（见第 5–7 段开头的路标）。
- A2 的 8 步方法表，标 "You are here"：
  - 01 气候：温哥华天气文件的季节平均、相似气候城市。✓
  - 03 案例：26 个社区中心平面（21 个读了平面图），归纳出 5 种流线类型。✓（`Circulation_Patterns.md`）
  - 05 规则提炼：R1–R8、五段定义。✓
  - 06/07 原型和检验：工具已经能运行，检验刚开始。▶ **现在在这里**
  - 02 乡土分析、04 使用者分析：还薄；空间策略和 kit-of-parts 还没成库（见第 6、8 段）。
- 时长从 0:45 缩到 0:30：子问题表挪到了第 5 段开头，这里不用再讲一遍。

## 4. 主张（1:00）
**你的原文，按讲的顺序：**
- **机会：** 然而人们进行不同活动时，需要的环境条件不同，这种差异为建筑空间组织提供了尚未充分利用的设计机会。
  > Architecture often treats environmental comfort as something provided to space after its organization.
- **主张：** 调节不是"有 / 无"，而是从 exposed 到 controlled 的五段渐变；每个活动只给"刚好够"的防护。通过活动与气候的关系建立 Conditioning Gradient，并将其转化为空间组织原则。
- **五段按围合方式定义：** 无屋顶 = exposed；有屋顶、少于两面墙 = protected；有屋顶、至少两面墙 = buffered；四面封闭、无机械调节 = tempered；有机械调节 = controlled。（`STAGE_RULES.md` 第 1 节）配图：一条五段剖面色带。
- **因果方向：** 建筑体块决定防护程度，防护程度决定能承接的活动。空间策略再进一步调节，帮助空间承接活动。
- **怎么检验：** 现在用规则和模拟比较不同配置。以后会加上 AI 辅助解释，并检验它们的实际性能与使用边界（对照组、实测）。
- **研究成果：** 不是唯一正确的最优方案，而是一套能让环境性能更早进入建筑决策、并允许比较与复核的逻辑。
  > From performance evaluation to performance-informed spatial design.
- **愿景：** 从固定的房间和固定的环境设定，走向能够随气候与活动变化而演化的建筑。

**已定（用户 2026-10-27）：**
1. "AI 辅助解释"和"检验实际性能"是工具以后要做的功能，讲成将来时（"will add"、"will test"）。现在点房间看到的解释，是按规则一步步追溯出来的。
2. "研究成果"从"一套方法"改成"一套逻辑"，和 GP1 里"渐变论证是主角，工具是证明"一致。

**时长提醒：** 这一段从 0:50 加长到约 1:00，内容还很满。如果超时，先删"愿景"一句（它和开场设问意思接近）。

## 5. Activity — 前提：文献（logical argument）（1:30）
**路标（你的原文）：**
| 子问题 | 方法 | 段落 |
|---|---|---|
| **Activity：** 不同活动需要什么环境条件？它们能够适应多少变化？ | 借用的相关性文献（PET、行为研究） | 本段 |
| **Space：** 哪些建筑空间策略可以在不完全依赖机械设备的情况下提供这些条件？ | 案例研究、kit-of-parts | 第 6 段 |
| **Decision：** 如何让建筑师在设计早期比较这些策略，并将环境性能转化为布局决策？ | 模拟（工具） | 第 7 段 |

这张表放在这一段开头，讲一次，后面三段各自开头指一下对应的那一行。

**时长提醒（2026-10-27 加了文献之后）：** 这一段的文献比 1:30 能讲完的多。讲的时候每个前提只念一到两条，其余放在幻灯片上作小字，或留着回答提问。

**P1 二分法不是必要的**
- **Kim 2019：** 阶段会改变人的期待。自然通风时，人比在空调下更能容忍温度变化；人调整衣着也比 ASHRAE 55 的衣着模型预测的更主动，说明人自己适应的能力被标准低估了。（A，澳洲亚热带办公楼）[^c7]
- **Hou 2025：** 能自由来去时，人能耐受的范围更宽。综述转引 Nakano 等的研究：半室外空间的耐受范围是 PPD 预测值的 2–3 倍。前提是人可以自由来去、停留较短。（A；Nakano 原文未读）[^c8]
- **Pérez-Fargallo 2025：** 人觉得冷或热时，先做个人调整（加衣服、喝热饮），然后才用暖气、开窗这类环境手段。说明中间阶段可以先靠人自己适应。（A；智利住宅，72 户）[^c22]
- → 规则：五段渐变取代二分；能自由来去的门厅、走廊放 buffered；久坐的功能冬季要 controlled（R3，依据 Mora & Bean）。[^c9]

**P2 舒适取决于活动和人**
- **Zhang 2024、Lau 2026：** 舒适随活动强度和人群而变。活动越剧烈，中性 PET 越低；75 岁以上的人中性 PET 高约 4℃。（A）[^c10]
- **剑桥、谢菲尔德的阈值：** 借来的数值。两城的季节平均气温与温哥华几乎相同；温哥华本地没有 PET 研究。（A，`Climate_Analog_PET_Readings.md`）[^c11]
- **Nikolopoulou & Lykoudis 2006 的另外两点：** 中性温度跟着前一个季节变，同样的天气，秋天和春天感觉不同；自愿来的人比路过、来工作、等人的人更能忍受不适。（A）[^c23]
- **Krüger 2017（格拉斯哥）：** 格拉斯哥的中性档（PET 10–18℃）整体低于原始 PET 分级的中性范围（18–23℃），说明冷气候城市的人能接受更低的温度。（A）[^c24]
- **City of Toronto 2025：** 按季节、按时段设可接受的 UTCI 范围；设计建议里区分了运动区（要遮阳、通风）和静坐区（要日照和阴影可选）。局限：只是定性建议，没有按活动给数值。（A）[^c25]
- **Kenawy & Elkadi 2018（墨尔本）：** 活动强度用代谢率表示：坐 1 met，站 1.2 met，走 2 met（论文称采用 ASHRAE 55 和 ISO 7730，原标准表我没看到）。（A）[^c26]
- → 规则：R4 剧烈活动 tempered 就够；R6 老人儿童提高一级；阈值做成标明来源、可替换的输入。

**P3 舒适影响使用，但不决定使用**
- **Zacharias 2001、Eliasson 2007：** 舒适影响人们是否使用空间，但不决定。蒙特利尔坐着的人的比例与气温高度相关（r = 0.92），但"在场不等于满意"；哥德堡天气大致解释一半的到场人数变化。Zacharias 还发现，约 20℃ 时坐在阳光里和坐在阴影里的人数差不多。（A）[^c12]
- **Nikolopoulou & Lykoudis 2006：** 使用目的会改变人对环境的容忍度：自愿来的人更能忍受，路过、来工作、等人的人忍受度更低。（A）[^c27]
- → 规则边界：工具只判断"这个空间能不能承接这个活动"，不声称能产生社交。

## 6. Space — 空间策略积累（case study，interpretive）（0:45）〔v2 新增〕
**你列的四类，我补了来源：**
- **乡土手法：** 檐廊 / 骑楼（遮雨加社交边缘）、庭院（微气候）、蓄热体、可开启的外围护。（A2、旧 PPT 第 7 页；Oliver、Turan）[^c13]
- **寒冷地区的半室外手法（Hou 2025 综述）：** 冬季日照优先、迎风面加围合挡冬季风、屋顶适度透光、落叶树。（A；寒冷地区只占综述里的少数研究）[^c14]
- **被动调节手法：冬季花园缓冲层、热辐射等。**
  - 冬季花园：Lacaton & Vassal。（B，书未拿到）[^c15]
  - 热辐射：Bouyer 2007 指出半户外空间的平均辐射温度主要来自结构表面而非直射阳光，屋顶材料很重要（A，`Bouyer_2007_Semi_Outdoor_PET.md`）。[^c16] Philippe Rahm 把辐射当作建筑材料（B，`Industry_Position_Scan.md`）。[^c16r]
  - 遮阳：Hartabela 2021（北九州公园）发现平均辐射温度对 PET 的影响最大，遮阳是最关键的手法。（A；日本温带公园，一个站点）[^c28]
- **心理调节（用户 2026-10-27 定：暂时只讲到心理调节，作为较小的一点，一句话带过）：**
  - Hou 2025：头顶是轻质屋顶或玻璃时，人觉得空间更像室外，期望降低（A）。[^c17]
  - 备用（被问到再说）：Yang 2026，热预期占适应性热感觉的 90% 以上（A，长沙，作者自报 R² = 0.954）；Eliasson 2007，在水边、公园这类自然环境里，人对风更宽容（A）。[^c18]
  - 只有定性依据，不说成可以替代热防护。

**〔补〕温哥华雨篷标准放这里：** 雨篷高 3.0–5.0 m，深度与高度之比约 7:10（A，`Vancouver_Documents_Round1.md`）。它是目前唯一一条处理"雨"、又有温哥华本地依据的空间策略，正好补上第 1 段说的"把雨算进去"的空白。[^c19]

**〔待定〕状态要讲清楚：** 这些策略还没整理成库（`STAGE_RULES.md` 第 7 节：工具库还没收集），工具现在也还没用到它们（工具只按围合分阶段）。讲成"已经开始积累，下一步接进工具"。

## 7. Decision — 规则 R1–R8 → 工具检验 → 结果与缺口（simulation）（2:00）
**目的（你的原文）：** 检验前面建立的理论能否产生真正有用的空间决策。

**工具做三件事（你的原文），配图和要点〔补〕：**
1. **根据活动需求和环境数据分配保护等级。**
   - **怎么用：** 每个功能在每个季节，把被触发的规则都找出来，取其中要求最高的阶段，这就是它的"最低阶段"，也就是"刚好够"。空间的阶段低于它，这个功能放不进去；高于它，就是过度调节。第一版先做冬季。（`STAGE_RULES.md` 第 2 节）
   - **R1–R8（`STAGE_RULES.md` 第 3 节）：**

     | 编号 | 规则 | 依据 | 依据类型 |
     |---|---|---|---|
     | R1 | 怕雨的功能，至少 protected | 温哥华导则把遮雨作为设计意图（雨篷高 3.0–5.0 m，深高比约 7:10）；常识 | 推断 |
     | R2 | 怕风的功能，至少 buffered | 多伦多行人风条款：坐 ≤ 10、站 ≤ 15、走 ≤ 20 km/h，各占 80% 的时间。把风速界限对应到阶段，是我们自己的对应 | 借用（风速界限）+ 推断（对应） |
     | R3 | 久坐的功能，冬季至少 controlled，夏季至少 tempered | Mora & Bean：适应性模型要求室外平均 ≥ 10℃，温哥华 11 月到 4 月不满足；Lau、Zhang：静态活动需要更暖 | 推断（冬）；假设（夏） |
     | R4 | 剧烈活动能耐受较凉，tempered 就够 | Zhang：活动越剧烈，中性 PET 越低；Lau | 文献方向支持 |
     | R5 | 有卫生、安全、精密要求的功能（厨房、展品、泳池），controlled | 常识，没有来源 | 假设 |
     | R6 | 老人、儿童使用的功能，在同类功能基础上提高一级，上限 controlled | Lau：75 岁以上的人中性温度偏高；Mora & Bean：ASHRAE 55 不直接涵盖弱势人群 | 推断 |
     | R7 | 中等强度以上的室内活动（体育馆、健身、青少年活动），冬季至少 tempered，夏季至少 buffered | 你 2026-10-17 的决定：要干燥的地面、器械、运动装 | 你的决定；季节写法是假设 |
     | R8 | 脱衣的功能：卫生间至少 tempered；更衣室、淋浴冬季至少 controlled，夏季至少 tempered | 你 2026-10-17 的决定 | 你的决定；具体写法是假设 |

     规则的依据见脚注。[^c29]
   - **依据类型小结：** 8 条里 5 条来自文献（R1–R4、R6，其中 R2 的风速界限是借来的，R3 的夏季一句是假设），R5 是假设，R7、R8 是你的决定。
   - **你 2026-10-17 的具体决定：** 咖啡按久坐处理（R3）；老年人活动空间夏季也是 controlled（R3 + R6）。
   - **讲的时候：** 幻灯片放整张表，用颜色区分依据类型；口头只举两条例子（R1 怕雨、R3 久坐），然后说"8 条里 5 条来自文献"。
2. **在基本几何约束下生成和比较布局方案。**
   - 载体：社区中心（Marpole 2021 任务书，Sunset Park 场地）。它是检验载体，不是研究对象。[^c20]
   - 平面按 buffered → tempered → controlled 分层，controlled 聚在冬季向阳的一侧。
   - A/B/C/D 四个体块方案对比，只讲成方案之间的相对值：
     | 方案 | 整体空白 | 受晒 | 渐变序列 |
     |---|---|---|---|
     | A | 14% | 66% | 70% |
     | B | 11% | 69% | 71% |
     | C | 15% | 57% | 69% |
     | D | 10% | 45% | 68% |
   - 配图：`04_Presentation/screenshots/2026-10-22_v01_sunset_mass_options_overview.jpg`、`2026-10-23_v01_dark_step5_axo.jpg`。
3. **解释某个空间为什么适合或不适合某项活动，并说明计算依据。**
   - 点房间，看到：贴哪面外墙、和谁相邻、属于哪个阶段 → 对应规则 → 规则的依据。图上只画工具真正用过的数。
   - 配图：30–40 秒录屏，不现场操作。

**结果与缺口〔补〕：**
- **能说的：** 论证可以写成规则并运行，产生可辨认的分层组织，每个决定都能追溯。
- **还不能说的：**
  - 渐变比"全部 controlled"省多少调节面积（**对照组是下一步**）；
  - 五个阶段是否对应真实的热防护（阶段是几何代理）；
  - 冬季 tempered 是否舒适。
- **一句带过：** 当前版本选方案时仍先看紧凑和受晒，渐变只显示、不参与选择，要改。
- 时长从 2:20 缩到 2:00，给新增的第 6 段让位。

## 8. 设计原则（kit-of-parts）（0:30）
**你的原文：** 每个案例转化为可以在新建筑设计中重复使用的空间原则。

**〔补〕手上已经有、但不在第 6 段的：** 流线规律（26 个社区中心平面）：
- 大件从门厅能看见；
- 穿越式门厅连接街道和公园；
- 有顶的室外长廊是室内街道的延伸，直接对应 buffered 的公共停留空间。

（`Circulation_Patterns.md` 第 2 节；A，部分由检索代理读图）

**第 6 段和第 8 段的分工（用户 2026-10-27 同意）：**
- 第 6 段是"收集"：从案例和文献里找手法；
- 第 8 段是"转化"：把手法写成可以重复使用的原则（kit-of-parts），也是工具检验之后的产出。

第 8 段讲成下一步的目标，配一张流线类型图作示意。

## 9. 想请评图人回答的问题（0:15）〔补，v2 没有，作业里的讨论环节用得上〕
挑一到两题：
- "Is the gradient convincing without local measurements?"
- "Should leftover space count as failure, or as buffered public space?"

---

## 评图时可能被问到的薄弱点（准备答案，不一定讲）
1. 阶段按围合几何定义，和实际热防护之间的对应没验证。
2. 冬季 tempered 没有舒适依据：ASHRAE 适应性模型在温哥华半年不适用；借用的 PET 范围你还没拍板。[^c21]
3. 雨只有温哥华的雨篷几何标准，没有任何舒适依据。
4. 面积只来自 Marpole 一份任务书。
5. 为什么从 A2 的室外公共空间转到社区中心：它是检验载体，不是研究对象。
6. "先定房间、再调环境"是你的观察，目前只有间接佐证。
7. 〔v2 新增〕心理调节只有定性依据，没有可用的数值。
8. 〔v2 新增〕"AI 辅助解释"和"检验实际性能"是以后的功能，现在还没做到。

## 时长
0:20 + 1:15 + 0:45 + 0:30 + 1:00 + 1:30 + 0:45 + 2:00 + 0:30 + 0:15 = **约 8:50**，很满。练习以 8:00 为目标。超时可以：
- 第 4 段删"愿景"一句，省约 0:10；
- 第 1 段的出发点文献只留三条（市政文件、Mora & Bean、Hou / Ma 空白），省约 0:20；
- 第 8 段并进第 6 段末尾，作为"下一步"一句话，省约 0:20。


## 引用说明（Chicago，notes-bibliography）
- 每个引用文献的段落后加一个脚注。英文版和中文版共用同一套脚注（同一出处用同一个编号）。第一次出现写全称，再次出现写简称。脚注和参考文献用英文，按 Chicago 第 17 版格式。
- 作者全名只在 PDF 首页核对过的才写全；没核对的用名字缩写。
- **〔待核〕**
  - Oliver 和 Turan 的书目照抄 A2 的写法（"*Vernacular Architecture*. Routledge, 1990"）。请对照你手上的书，核对书名全称、编者和出版社。
  - Eliasson 2007 的文章标题是我凭记忆写的，笔记里只有期刊、卷号和页码。
  - Rahm 那条只引了网页，标题是从网址推出来的，Rahm 的原著还没读。
  - Mora & Bean 只核对了月份和页码（40–46），没有核对卷号。
  - Lacaton & Vassal 的书没拿到，作者署名按出版社网页写。

### 中文版脚注
[^c1]: City of Vancouver, *Places for People Downtown: Hot Tea, Rain City Winter Engagement Summary* (Vancouver: City of Vancouver, 2018); City of Vancouver, *Downtown Public Space Strategy* (Vancouver: City of Vancouver, 2021), sec. 2.4.1.
[^c2]: Paul Oliver, "Vernacular Know-How," in *Vernacular Architecture* (Routledge, 1990); Mete Turan, "Vernacular Design and Environmental Wisdom," in *Vernacular Architecture* (Routledge, 1990).
[^c3]: Rodrigo Mora and Robert Bean, "Thermal Comfort: Designing for People," *ASHRAE Journal*, February 2018, 40–46.
[^c4]: G. Hou et al., "A Comprehensive Review of Thermal Comfort Related Design Strategy of Semi-Outdoor Transitional Spaces," *Energy and Buildings* 345 (2025): 116116, https://doi.org/10.1016/j.enbuild.2025.116116; X. Ma et al., "Spatial Thermal Comfort Autonomy (sTCA) for Corridor–Atrium Buildings in Cold-Climate High-Density Contexts: UTCI-Based Multi-Objective Optimisation and Sensitivity Analysis," *Frontiers of Architectural Research* (2026), https://doi.org/10.1016/j.foar.2026.03.018.
[^c5]: "My Top Five Favorite Features of Forma Site Design in 2025," *Autodesk Forma Blog*, January 19, 2026, https://blogs.autodesk.com/forma/2026/01/19/my-top-five-favorite-features-of-forma-site-design-in-2025/; J. Nwagwu Ume-Ezeoke, C. Gorlé, and R. K. Jain, "AURA: Automated Universal Floor Plan Replication for Airflow and Thermal Analysis" (preprint, SSRN 6791324, 2026); H. Li et al., "MCP-Enabled Agentic AI Workflow for Building Energy Modelling: Framework and Use Cases," *Journal of Building Performance Simulation* (2026), https://doi.org/10.1080/19401493.2026.2653969.
[^c6]: "Forma Site Design in 2025"; Nwagwu Ume-Ezeoke, Gorlé, and Jain, "AURA."
[^c7]: Jungsoo Kim et al., "Thermal Comfort in a Mixed-Mode Building: Are Occupants More Adaptive?" *Energy and Buildings* 203 (2019): 109436, https://doi.org/10.1016/j.enbuild.2019.109436.
[^c8]: Hou et al., "Comprehensive Review" (citing Nakano et al. on the two-to-threefold tolerance range).
[^c9]: Mora and Bean, "Thermal Comfort."
[^c10]: Y. Zhang et al., "Study on the Outdoor Thermal Comfort of College Students under Different Activity Intensities in a High-Altitude Climate Zone," *Frontiers in Public Health* 12 (2024): 1365470, https://doi.org/10.3389/fpubh.2024.1365470; Kevin Lau, Lingye Yao, and Edward Ng, "Designing for Mild Winters: Evidence-Based Thermal Comfort Benchmarks from Urban Parks in a Sub-Tropical City," *International Journal of Biometeorology* 70 (2026): 116, https://doi.org/10.1007/s00484-026-03190-9.
[^c11]: Marialena Nikolopoulou and Spyros Lykoudis, "Thermal Comfort in Outdoor Urban Spaces: Analysis across Different European Countries," *Building and Environment* 41 (2006): 1455–70, https://doi.org/10.1016/j.buildenv.2005.05.031; K. Pantavou et al., "Thermal Sensation and Climate: A Comparison of UTCI and PET Thresholds in Different Climates," *International Journal of Biometeorology* 62 (2018): 1695–1708, https://doi.org/10.1007/s00484-018-1569-4.
[^c12]: John Zacharias, Ted Stathopoulos, and Hanqing Wu, "Microclimate and Downtown Open Space Activity," *Environment and Behavior* 33, no. 2 (2001): 296–315; I. Eliasson et al., "Climate and Behaviour in a Nordic City," *Landscape and Urban Planning* 82 (2007): 72–84.
[^c13]: Oliver, "Vernacular Know-How"; Turan, "Vernacular Design."
[^c14]: Hou et al., "Comprehensive Review."
[^c15]: Anne Lacaton and Jean-Philippe Vassal, *It's Nice Today: On Climate, Comfort, and Pleasure* (Berlin: Ruby Press, 2024).
[^c16]: J. Bouyer et al., "Thermal Comfort Assessment in Semi-Outdoor Environments: Application to Comfort Study in Stadia," *Journal of Wind Engineering and Industrial Aerodynamics* 95 (2007): 963–76, https://doi.org/10.1016/j.jweia.2007.01.022.
[^c16r]: "Philippe Rahm: Thermodynamics Cities," *IAAC Blog*, April 29, 2014, https://www.iaacblog.com/2014/04/29/philippe-rahm-thermodynamics-cities/.
[^c17]: Hou et al., "Comprehensive Review."
[^c18]: Xinpeng Yang et al., "Quantifying the Effect of Psychological Adaptation: A New Model for Outdoor Thermal Comfort Evaluation in Urban Public Spaces — A Case Study in the Hot-Summer and Cold-Winter Zone," *Sustainable Cities and Society* 148 (2026): 107679, https://doi.org/10.1016/j.scs.2026.107679; Eliasson et al., "Climate and Behaviour."
[^c19]: City of Vancouver, *Design and Development Guidelines* (Vancouver: City of Vancouver, 2025; amended February 3, 2026), sec. 3.1.1.
[^c20]: Inform Planning, *Marpole Community Centre Functional Program: Final Report* (Vancouver: City of Vancouver, July 20, 2021).
[^c21]: Mora and Bean, "Thermal Comfort."
[^c22]: Alexis Pérez-Fargallo et al., "Relationship between the Architectural and Constructive Characteristics of Dwellings and the Adaptive Actions of Their Occupants," *Energy Efficiency* 18 (2025): 27, https://doi.org/10.1007/s12053-025-10312-6.
[^c23]: Nikolopoulou and Lykoudis, "Thermal Comfort in Outdoor Urban Spaces."
[^c24]: E. Krüger, F. Rossi, and P. Drach, "Calibration of the Physiological Equivalent Temperature Index for Three Different Climatic Regions," *International Journal of Biometeorology* 61 (2017): 1323–36, https://doi.org/10.1007/s00484-017-1310-8.
[^c25]: City of Toronto, *Thermal Comfort Guidelines 2025: For Large Area Studies, Public Realm Capital Projects & Large Site Developments* (Toronto: City of Toronto, January 2025).
[^c26]: Inji Kenawy and Hisham Elkadi, "The Outdoor Thermal Benchmarks in Melbourne Urban Climate," *Sustainable Cities and Society* 43 (2018): 587–600.
[^c27]: Nikolopoulou and Lykoudis, "Thermal Comfort in Outdoor Urban Spaces."
[^c28]: Dadang Hartabela, Bart Julien Dewancker, and Mochamad Donny Koerniawan, "A Relationship between Micro-Meteorological and Personal Variables of Outdoor Thermal Comfort: A Case Study in Kitakyushu, Japan," *Sustainability* 13 (2021): 13634.
[^c29]: City of Vancouver, *Design and Development Guidelines*, sec. 3.1.1 (R1); City of Toronto, *Pedestrian Level Wind Study: Terms of Reference Guide* (Toronto: City of Toronto, June 2022), table 3 (R2); Mora and Bean, "Thermal Comfort" (R3, R6); Zhang et al., "Outdoor Thermal Comfort of College Students" (R3, R4); Lau, Yao, and Ng, "Designing for Mild Winters" (R3, R4, R6).

---
---

# GP1 Progress Review #1 — Presentation Outline (v6, English)

Date: 2026-10-27. Review: 28 Oct 2026, 4:10 pm, Room 4 ANNEX Small. Reviewers: James Huemoeller, Xun Liu. Present for 9 minutes or less; the rest is discussion.

This English version follows the Chinese version above. Notes for myself (sources, open decisions) stay in the Chinese version.

## Overall logic

```
Problem (with the literature that revealed it) → Thesis statement + research question
→ Method and where I am → Claim (five-stage gradient)
→ Activity: premises P1–P3 (borrowed correlational studies, logical argument)
→ Space: collecting spatial strategies (case studies, interpretive)
→ Decision: rules R1–R8 → test with the tool (simulation) → results and gaps
→ Design principles (kit-of-parts)
```

The literature appears twice, in two roles. In the problem, it shows what is wrong with current practice and what has not been studied. In the premises, it supports each step of the argument. The literature does not prove the thesis. Proof will come from the tool test, together with the baseline comparison and measurements still to come.

## 0. Title and opening image (0:20)
- **Title:** "Just Enough: Conditioning as a Calibrated Gradient"
- **Opening image:** winter photos of empty parks under the Burrard and Cambie bridges, beside a summer crowd at W 18th Ave and Cambie St.

## 1. Problem (1:15)
**Narrative**
- Public life in Vancouver is strongly shaped by weather. Rain and cold in winter can make some public activities hard to sustain.
- At the same time, buildings usually organise environmental control around one clear boundary between inside and outside.
- **First observation: different activities need different environments.** A person running, a person having coffee and a person working at a laptop for hours do not need the same temperature, wind, rain shelter or stability.
- **Problem:** why does early-stage layout so rarely use the adaptive capacity of different activities to decide how much protection a space needs? Typically, we fix the location, size and use of rooms first, and only then work out how to reach the intended conditions.

**The literature that revealed the problem**
- **City of Vancouver documents:** the public is asking for sheltered, heated places to stay.
  - *Hot Tea, Rain City* (2018): about 1,200 participants and 96 feedback cards; qualitative.
  - *Downtown Public Space Strategy* (2021): calls for "year-round" and "rain-friendly" public spaces.[^c1]
- **Vernacular literature from Assignment 2 (Oliver, Turan):** buildings once mediated climate rather than shutting it out.[^c2]
- **Mora and Bean (2018):** ASHRAE 55 is itself a binary. Mechanically conditioned buildings use PMV; naturally conditioned buildings use the adaptive model; there is nothing in between. The adaptive model also requires an outdoor mean of at least 10 °C, which Vancouver does not meet from about November to April.[^c3]
- **Hou (2025), Ma (2026):** most research on semi-outdoor spaces is in hot, humid climates. Very little addresses a mild, wet winter. This is a gap.[^c4]
- **Tool literature (Forma, AURA, Li 2026):** existing tools go from form to performance, or from plan to airflow. None puts "how much protection an activity needs" into the layout. This is also a gap.[^c5]

## 2. Thesis statement and research question (0:45)
- **Opening question:**
  > What if conditioning is not a fixed property of a room, but a changing relationship between climate, activity, architecture, and season?
- **Thesis statement:**
  > Conditioned space can be reinterpreted as a calibrated gradient of climatic protection and exposure, where activity-specific environmental needs and microclimatic conditions guide spatial arrangement and protection strategies.
- **Research question:**
  > How can activity-specific environmental requirements inform early-stage spatial organization to reduce the potential for over-conditioning while maintaining acceptable comfort and usability?

## 3. Method and where I am (0:30)
- Logical argumentation is the backbone. Each sub-question uses its own method (see sections 5–7).
- Tactical sequence from Assignment 2:
  - 01 Climate: seasonal means from the Vancouver weather file; analogue cities. Done.
  - 03 Case studies: 26 community centre plans (21 with drawings), five circulation types. Done.
  - 05 Strategy extraction: rules R1–R8 and the five stages. Done.
  - 06/07 Prototyping and testing: the tool runs; testing has started. **I am here.**
  - 02 Vernacular analysis and 04 user analysis: still thin. The spatial strategies and the kit-of-parts are not yet compiled.

## 4. Claim (1:00)
- **Opportunity:** people doing different activities need different environmental conditions. This difference is a design opportunity that spatial organisation has not yet used.
  > Architecture often treats environmental comfort as something provided to space after its organization.
- **Claim:** conditioning is not "on or off" but a five-stage gradient from exposed to controlled, and each activity gets just enough protection. The relationship between activity and climate builds a conditioning gradient, which is then turned into principles for spatial organisation.
- **Five stages, defined by enclosure:**
  - **exposed:** no roof;
  - **protected:** roof, with fewer than two walls;
  - **buffered:** roof, with at least two walls;
  - **tempered:** fully enclosed, without mechanical conditioning;
  - **controlled:** mechanically conditioned.
- **Direction:** massing determines the level of protection; the level of protection determines which activities a space can host. Spatial strategies then adjust conditions further, helping the space host those activities.
- **How it is tested:** for now, rules and simulation are used to compare configurations. Next, I will add AI-assisted explanation, and test actual performance and the limits of use against a baseline and measurements.
- **Outcome:** not a single optimal answer, but a logic that brings environmental performance into design decisions earlier and lets them be compared and checked.
  > From performance evaluation to performance-informed spatial design.
- **Vision:** from fixed rooms with fixed settings, towards architecture that can change with climate and activity.

## 5. Activity — premises from the literature (logical argument) (1:30)
| Sub-question | Method | Section |
|---|---|---|
| **Activity:** what environmental conditions do different activities need, and how much variation can they tolerate? | Borrowed correlational studies (PET, behaviour) | 5 (this section) |
| **Space:** which spatial strategies can provide these conditions without relying fully on mechanical systems? | Case studies, kit-of-parts | 6 |
| **Decision:** how can architects compare these strategies early in design and translate environmental performance into layout decisions? | Simulation (the tool) | 7 |

**P1 The binary is not necessary**
- **Kim (2019):** the stage changes what people expect. Under natural ventilation, people tolerate more temperature variation than under air conditioning. People also adjust their clothing more actively than the ASHRAE 55 clothing model predicts, so standards underestimate how much people adapt by themselves.[^c7]
- **Hou (2025):** when people can come and go freely, they tolerate a wider range. The review cites Nakano et al.: in semi-outdoor spaces, people tolerate a range two to three times wider than PPD predicts, provided they can leave freely and stay for a short time.[^c8]
- **Pérez-Fargallo (2025):** when people feel too cold or too warm, they first adjust themselves (clothing, hot drinks) before using heating or opening windows. Intermediate stages can rely on people adapting first.[^c22]
- → Rules:
  - a five-stage gradient replaces the binary;
  - lobbies and corridors that people pass through can be buffered;
  - seated activities need a controlled space in winter (R3, based on Mora and Bean).[^c9]

**P2 Comfort depends on the activity and the person**
- **Zhang (2024), Lau (2026):** comfort varies with activity intensity and with the person. The more intense the activity, the lower the neutral PET; people over 75 have a neutral PET about 4 °C higher.[^c10]
- **Cambridge and Sheffield thresholds:** borrowed values. Their seasonal mean temperatures are almost the same as Vancouver's, and there is no local PET study for Vancouver.[^c11]
- **Nikolopoulou and Lykoudis (2006), two more findings:** neutral temperature follows the previous season, so the same weather feels different in autumn and in spring; and people who come by choice tolerate more discomfort than people passing through, working or waiting.[^c23]
- **Krüger (2017), Glasgow:** the neutral band (PET 10–18 °C) sits below the original PET neutral range (18–23 °C). People in a cool climate accept lower temperatures.[^c24]
- **City of Toronto (2025):** acceptable UTCI ranges are set by season and time of day. Its design advice separates active areas (shade and ventilation) from seating areas (a choice of sun and shade). It gives no values by activity.[^c25]
- **Kenawy and Elkadi (2018), Melbourne:** activity intensity is expressed as metabolic rate: sitting 1 met, standing 1.2 met, walking 2 met.[^c26]
- → Rules:
  - R4: vigorous activity can stay tempered;
  - R6: spaces for older adults and children go one stage up;
  - thresholds are labelled, replaceable inputs.

**P3 Comfort shapes use, but does not decide it**
- **Zacharias (2001), Eliasson (2007):** comfort affects whether people use a space, but does not decide it. In Montreal, the share of people sitting tracks air temperature closely (r = 0.92), but presence is not satisfaction. In Gothenburg, weather explains about half of the variation in attendance. Zacharias also found that at about 20 °C, as many people sit in the sun as in the shade.[^c12]
- **Nikolopoulou and Lykoudis (2006):** the purpose of a visit changes how much discomfort people accept. Those who come by choice tolerate more; those passing through, working or waiting tolerate less.[^c23]
- → Limit: the tool only judges whether a space can host an activity. It does not claim to create social life.

## 6. Space — collecting spatial strategies (case study, interpretive) (0:45)
- **Vernacular strategies:** veranda or arcade (rain shelter and social edge), courtyard (microclimate), thermal mass, operable envelope.[^c13]
- **Semi-outdoor strategies for colder climates (Hou 2025):** prioritise winter sun, enclose the windward side against winter wind, use a moderately translucent roof, plant deciduous trees.[^c14]
- **Passive strategies:**
  - winter garden as a buffer (Lacaton and Vassal);[^c15]
  - radiant heat: in semi-outdoor spaces, radiant temperature comes mainly from the surrounding surfaces, so the roof material matters (Bouyer 2007).[^c16]
  - shade: mean radiant temperature has the largest effect on PET, so shading is the key strategy (Hartabela 2021).[^c28]
- **Psychological adjustment:** a light or glazed roof makes a space feel more like outdoors and lowers expectations (Hou 2025).[^c14]
- **Rain shelter (City of Vancouver guidelines):** canopies 3.0–5.0 m high, with a depth-to-height ratio of about 7:10.[^c19]
- Status: collecting has started. The strategies are not yet compiled or connected to the tool.

## 7. Decision — rules R1–R8 → test with the tool → results and gaps (simulation) (2:00)
**Purpose:** to test whether the theory can produce spatial decisions that are actually useful.

**The tool does three things**
1. **Assigns a level of protection from activity needs and environmental data.**
   - **How the rules work:** for each activity in each season, all the rules it triggers are found, and the highest stage they ask for becomes its minimum stage, which is "just enough". A space below that stage cannot host the activity; a space above it is over-conditioned. The first version covers winter.
   - **Rules R1–R8:**

     | Rule | Statement | Basis | Type of evidence |
     |---|---|---|---|
     | R1 | Activities that must stay dry: at least protected | City of Vancouver guidelines treat rain shelter as a design intent (canopies 3.0–5.0 m high, depth-to-height about 7:10) | Inferred |
     | R2 | Activities sensitive to wind: at least buffered | Toronto pedestrian wind criteria: sitting ≤ 10, standing ≤ 15, walking ≤ 20 km/h, each 80% of the time. Matching these limits to a stage is my own step | Borrowed (limits) + inferred (matching) |
     | R3 | Seated activities: at least controlled in winter, at least tempered in summer | Mora and Bean: the adaptive model needs an outdoor mean of at least 10 °C, which Vancouver misses from November to April; Lau, Zhang: static activities need more warmth | Inferred (winter); assumption (summer) |
     | R4 | Vigorous activities tolerate cooler conditions: tempered is enough | Zhang: the more intense the activity, the lower the neutral PET; Lau | Supported in direction by the literature |
     | R5 | Activities with hygiene, safety or precision needs (kitchen, exhibits, pool): controlled | Common sense; no source | Assumption |
     | R6 | Activities for older adults and children: one stage higher, up to controlled | Lau: people over 75 prefer warmer conditions; Mora and Bean: ASHRAE 55 does not directly cover vulnerable groups | Inferred |
     | R7 | Indoor activities of medium intensity or above (gym, fitness, youth): at least tempered in winter, at least buffered in summer | My decision: dry floors, equipment, sportswear | My decision; seasonal wording is an assumption |
     | R8 | Undressing: washrooms at least tempered; changing rooms and showers at least controlled in winter, at least tempered in summer | My decision | My decision; exact wording is an assumption |

     Sources for the rules are in the note.[^c29]
   - In short: five of eight come from the literature (R1–R4, R6); R5 is an assumption; R7 and R8 are my own decisions.
2. **Generates and compares layouts within basic geometric constraints.**
   - Test bed: a community centre (Marpole 2021 functional program, Sunset Park site). It is the test bed, not the subject.[^c20]
   - The plan layers from buffered through tempered to controlled; controlled spaces gather on the winter-sun side.
   - Four massing options, compared with each other only (relative values):
     | Option | Unassigned space | Sun exposure | Gradient sequence |
     |---|---|---|---|
     | A | 14% | 66% | 70% |
     | B | 11% | 69% | 71% |
     | C | 15% | 57% | 69% |
     | D | 10% | 45% | 68% |
3. **Explains why a space suits or does not suit an activity, and shows the basis.**
   - Click a room to see which façade it uses and what it is next to.
   - It also shows which stage the room needs, the rule behind that stage, and the evidence behind the rule.

**Results and gaps**
- **What it shows:**
  - the argument can be written as rules and run;
  - it produces a recognisable layered organisation;
  - every decision can be traced.
- **What it does not yet show:**
  - how much mechanically conditioned area the gradient saves compared with an all-controlled layout (the baseline comparison is the next step);
  - whether the five stages match real levels of thermal protection;
  - whether a tempered space is comfortable in a Vancouver winter.
- **One caveat:** the current version still weighs compactness and sun before the gradient when choosing a layout; this will change.

## 8. Design principles (kit-of-parts) (0:30)
Each case is turned into a spatial principle that can be reused in new buildings.
- **Circulation patterns from 26 community centre plans:**
  - the large rooms are visible from the lobby;
  - a through-lobby links street and park;
  - a covered outdoor promenade extends the interior street, which corresponds directly to buffered public space.
- **Next step:** turn the strategies from section 6 into a reusable kit-of-parts.

## 9. Questions for the reviewers (0:15)
- Is the gradient convincing without local measurements?
- Should leftover space count as failure, or as buffered public space?

## Timing
0:20 + 1:15 + 0:45 + 0:30 + 1:00 + 1:30 + 0:45 + 2:00 + 0:30 + 0:15 ≈ 8:50. Aim for 8:00 in practice.

## Notes
The English version uses the same footnotes as the Chinese version (same sources, same numbers).

## Bibliography

Bouyer, J., J. Vinet, P. Delpech, and S. Carré. "Thermal Comfort Assessment in Semi-Outdoor Environments: Application to Comfort Study in Stadia." *Journal of Wind Engineering and Industrial Aerodynamics* 95 (2007): 963–76. https://doi.org/10.1016/j.jweia.2007.01.022.

City of Toronto. *Pedestrian Level Wind Study: Terms of Reference Guide*. Toronto: City of Toronto, June 2022.

City of Toronto. *Thermal Comfort Guidelines 2025: For Large Area Studies, Public Realm Capital Projects & Large Site Developments*. Toronto: City of Toronto, January 2025.

City of Vancouver. *Design and Development Guidelines*. Vancouver: City of Vancouver, 2025. Amended February 3, 2026.

City of Vancouver. *Downtown Public Space Strategy*. Vancouver: City of Vancouver, 2021.

City of Vancouver. *Places for People Downtown: Hot Tea, Rain City Winter Engagement Summary*. Vancouver: City of Vancouver, 2018.

Eliasson, I., I. Knez, U. Westerberg, S. Thorsson, and F. Lindberg. "Climate and Behaviour in a Nordic City." *Landscape and Urban Planning* 82 (2007): 72–84.

Hartabela, Dadang, Bart Julien Dewancker, and Mochamad Donny Koerniawan. "A Relationship between Micro-Meteorological and Personal Variables of Outdoor Thermal Comfort: A Case Study in Kitakyushu, Japan." *Sustainability* 13 (2021): 13634.

Hou, G., Y. Kuai, L. Yin, Y. Li, and P. Shu. "A Comprehensive Review of Thermal Comfort Related Design Strategy of Semi-Outdoor Transitional Spaces." *Energy and Buildings* 345 (2025): 116116. https://doi.org/10.1016/j.enbuild.2025.116116.

Inform Planning. *Marpole Community Centre Functional Program: Final Report*. Vancouver: City of Vancouver, July 20, 2021.

Kenawy, Inji, and Hisham Elkadi. "The Outdoor Thermal Benchmarks in Melbourne Urban Climate." *Sustainable Cities and Society* 43 (2018): 587–600.

Kim, Jungsoo, Federico Tartarini, Thomas Parkinson, Paul Cooper, and Richard de Dear. "Thermal Comfort in a Mixed-Mode Building: Are Occupants More Adaptive?" *Energy and Buildings* 203 (2019): 109436. https://doi.org/10.1016/j.enbuild.2019.109436.

Krüger, E., F. Rossi, and P. Drach. "Calibration of the Physiological Equivalent Temperature Index for Three Different Climatic Regions." *International Journal of Biometeorology* 61 (2017): 1323–36. https://doi.org/10.1007/s00484-017-1310-8.

Lacaton, Anne, and Jean-Philippe Vassal. *It's Nice Today: On Climate, Comfort, and Pleasure*. Berlin: Ruby Press, 2024.

Lau, Kevin, Lingye Yao, and Edward Ng. "Designing for Mild Winters: Evidence-Based Thermal Comfort Benchmarks from Urban Parks in a Sub-Tropical City." *International Journal of Biometeorology* 70 (2026): 116. https://doi.org/10.1007/s00484-026-03190-9.

Li, H., L. Zhang, H. Zhou, and T. Hong. "MCP-Enabled Agentic AI Workflow for Building Energy Modelling: Framework and Use Cases." *Journal of Building Performance Simulation* (2026). https://doi.org/10.1080/19401493.2026.2653969.

Ma, X., H. Chen, T. Li, et al. "Spatial Thermal Comfort Autonomy (sTCA) for Corridor–Atrium Buildings in Cold-Climate High-Density Contexts: UTCI-Based Multi-Objective Optimisation and Sensitivity Analysis." *Frontiers of Architectural Research* (2026). https://doi.org/10.1016/j.foar.2026.03.018.

Mora, Rodrigo, and Robert Bean. "Thermal Comfort: Designing for People." *ASHRAE Journal*, February 2018, 40–46.

"My Top Five Favorite Features of Forma Site Design in 2025." *Autodesk Forma Blog*, January 19, 2026. https://blogs.autodesk.com/forma/2026/01/19/my-top-five-favorite-features-of-forma-site-design-in-2025/.

Nikolopoulou, Marialena, and Spyros Lykoudis. "Thermal Comfort in Outdoor Urban Spaces: Analysis across Different European Countries." *Building and Environment* 41 (2006): 1455–70. https://doi.org/10.1016/j.buildenv.2005.05.031.

Nwagwu Ume-Ezeoke, J., C. Gorlé, and R. K. Jain. "AURA: Automated Universal Floor Plan Replication for Airflow and Thermal Analysis." Preprint, SSRN 6791324, 2026.

Oliver, Paul. "Vernacular Know-How." In *Vernacular Architecture*. Routledge, 1990.

Pantavou, K., S. Lykoudis, M. Nikolopoulou, and I. X. Tsiros. "Thermal Sensation and Climate: A Comparison of UTCI and PET Thresholds in Different Climates." *International Journal of Biometeorology* 62 (2018): 1695–1708. https://doi.org/10.1007/s00484-018-1569-4.

Pérez-Fargallo, Alexis, Paula Gacitúa-Ferrada, Laura Marín-Restrepo, and David Bienvenido-Huertas. "Relationship between the Architectural and Constructive Characteristics of Dwellings and the Adaptive Actions of Their Occupants." *Energy Efficiency* 18 (2025): 27. https://doi.org/10.1007/s12053-025-10312-6.

"Philippe Rahm: Thermodynamics Cities." *IAAC Blog*, April 29, 2014. https://www.iaacblog.com/2014/04/29/philippe-rahm-thermodynamics-cities/.

Turan, Mete. "Vernacular Design and Environmental Wisdom." In *Vernacular Architecture*. Routledge, 1990.

Yang, Xinpeng, Diyu Yang, Ying Song, and Weiwei Liu. "Quantifying the Effect of Psychological Adaptation: A New Model for Outdoor Thermal Comfort Evaluation in Urban Public Spaces — A Case Study in the Hot-Summer and Cold-Winter Zone." *Sustainable Cities and Society* 148 (2026): 107679. https://doi.org/10.1016/j.scs.2026.107679.

Zacharias, John, Ted Stathopoulos, and Hanqing Wu. "Microclimate and Downtown Open Space Activity." *Environment and Behavior* 33, no. 2 (2001): 296–315.

Zhang, Y., X. Zhang, J. Han, and X. Liu. "Study on the Outdoor Thermal Comfort of College Students under Different Activity Intensities in a High-Altitude Climate Zone." *Frontiers in Public Health* 12 (2024): 1365470. https://doi.org/10.3389/fpubh.2024.1365470.
