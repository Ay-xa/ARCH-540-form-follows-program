# 研究策略（Research Strategy）— thesis 的方向标

日期：2026-10-22。状态：**用户确认的方向文件**。凡是阅读或处理 thesis 内容（Assignment 2、ARCH 548 GP1、文献、规则、工具逻辑）的人和 agent，先读这一份。

分类框架：建筑研究常用的七种策略（Interpretive-Historical、Qualitative、Correlational、Experimental & Quasi-Experimental、Simulation、Logical Argumentation、Case Studies），与 Groat & Wang《Architectural Research Methods》的分类一致。本文按通用理解对照，没有逐章核对原书；引用原书定义前先查原文。

---

## 1. 一句话

thesis 的核心是一个**概念系统**：把"有空调 / 无空调"的二分改写成五段渐变（exposed → protected → buffered → tempered → controlled），再用规则把活动配进"刚好够"的那一段。这个系统通过**一个工具**来运转和检验。

所以：**主干是 Logical Argumentation（逻辑论证），检验手段是 Simulation（模拟），Case Studies（案例研究）给规则供料，Correlational（相关性研究）的成果只借用、不自己做。**

命题（用户原话，2026-10-15）："Conditioned space can be reinterpreted as a calibrated gradient between climatic protection and environmental exposure, supporting year-round public occupation in Vancouver."

因果方向（用户坚持）：体块和策略决定防护程度 → 防护程度决定能承接的活动。不是反过来。

---

## 2. 七种策略逐条对照

| 策略 | 和 thesis 的关系 | 角色 |
|---|---|---|
| **6 Logical Argumentation（逻辑论证）** | 命题、五段阶段的定义（按围合方式推导）、活动配对规则 R1–R8、"刚好够"原则、因果方向，全是在搭一个自洽的逻辑系统。Groat & Wang 举的例子正是 Alexander 的 pattern language 和 Hillier 的 space syntax：规则系统 + 工具 | **主干** |
| **5 Simulation（模拟）** | `02_Prototypes/Version_01` 本身就是模拟器：EPW 气候 → 体块 → 受晒 / 围合阶段 → 功能排布 → 空白、受晒、渐变序列等指标。方案 A/B/C/D 的对比表已经是 simulation 的产出 | **验证** |
| **7 Case Studies（案例研究）** | 21 张社区中心平面归纳的流线规则（`Circulation_Patterns.md`）、Marpole 2021 任务书、Rahm 和 Lacaton & Vassal 的先例（`Industry_Position_Scan.md`），都是用案例给规则找依据 | 辅助 |
| **3 Correlational（相关性研究）** | 读过的 PET 文献（Zhang、Lau、Cambridge / Sheffield、Glasgow）全是别人做的现场相关性研究。不在温哥华自己做；只借阈值，并标注来源和适用限制 | 只借用 |
| **2 Qualitative（质性研究）** | 后期可用于小范围的使用者反馈（几位设计师或评图者用工具、谈体验），回应"设计师看不懂 AI 理由就不信任"的行业难题 | 可选，后期 |
| **1 Interpretive-Historical（诠释—历史）** | 只在 vernacular 工具库（被动调节手法的来历）那一小块可能用到 | 很小 |
| **4 Experimental & Quasi-Experimental（实验）** | 需要控制变量和真实被试，与时间、对象都不匹配 | 不用 |

---

## 3. 为什么主干是逻辑论证而不是模拟

Simulation 只回答"这个体块、这个排布得多少分"。**分数怎么定义，是由逻辑系统决定的。** 2026-10-22 留下的四个未决问题（WORK_LOG 续 3）里，三个都在论证层面：

1. 渐变和紧凑冲突时先保哪个；
2. 空白算排布失败，还是算潜在的 buffered / tempered 公共停留空间；
3. 用什么作主指标（候选：controlled 的外墙长度）。

这些答不清，模拟跑出来的数字就没有意义。论文的重心是把这套逻辑讲清楚、讲自洽；工具是它的证据。

---

## 4. 推进路线

1. **先把逻辑系统写成论文骨架。** 命题 → 五段阶段的定义 → 规则 R1–R8 → "刚好够"原则 → 主指标。每条规则标来源：任务书、案例归纳、文献阈值，还是用户设定。
2. **把工具定位为"论证的可运行版本"，设计对照。** 模拟最有说服力的用法是比较，不是单个结果：
   - 同一体块，"全部 controlled"的传统排法 vs 按渐变排法，比较 controlled 外墙长度和需要主动调节的面积（回答板上的 "could it be minimized"）；
   - 同一功能清单，A/B/C/D 四种体块，看渐变序列和空白的差异；
   - 冬季 vs 夏季，同一空间能承接的活动如何变化（尚未做）。
3. **案例研究继续作规则来源，但写明方法。** 21 张平面怎么选、归纳了什么、哪些规则来自案例而不是任务书。Lacaton & Vassal《It's Nice Today》的实测数据若拿到原书，是 buffered 阶段唯一的实测依据。
4. **借来的相关性数据要有"替换接口"。** 阈值作为带来源标签的可替换输入；论文坦白写"温哥华没有本地 PET 研究，借用相似气候城市的中性范围"。这是诚实的方法论陈述，不是弱点。
5. **最后留一小块质性研究。** 评图或同学试用的反馈，补"设计师能否读懂工具的理由"。

---

## 5. 要当心的地方

- 模拟里很多数字是假设（面积、净高、评分权重 1 / 0.7 / 0.3 等）。论文里说明它们是**比较用的相对值**，口径与 Assignment 1 README 一致。
- 逻辑论证的弱点是"自洽但不一定对"。案例和文献就是用来堵这个缺口的，三者要一起出现，不能只有规则。
- 不编造数值、规范或阈值；每个数字带"谁、在哪、季节、强度"。

---

## 6. 对 agent 的要求（处理 thesis 内容时）

- 评价或修改任何规则、评分、排布逻辑时，先问：这改动服务于**逻辑论证**（渐变、刚好够、因果方向）吗？只为紧凑、受晒或少空白而偏离渐变，要先提出来讨论，不直接改（用户 2026-10-22："先不改，先讨论"）。
- 新增的数值要说明属于哪一类来源：任务书 / 案例归纳 / 借用的相关性文献 / 用户设定 / 假设。
- 做模拟或测试时，优先设计**对照**（传统 vs 渐变、方案之间、季节之间），而不是只报一个分数。
- 文献笔记要保留"适用限制"一栏（气候、对象、季节），因为它们都是借用的。

相关文件：`../Tool_Logic_Draft_v2.md`（命题与已确认逻辑）、`../Literature_To_Tool_Decisions.md`（文献如何支撑决定）、`../02_Prototypes/_shared/Rules/`（规则与功能库）、`../../WORK_LOG.md` 2026-10-22（续 3）（四个未决问题）。
