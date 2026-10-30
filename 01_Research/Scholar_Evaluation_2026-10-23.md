# Scholar Evaluation：Tool_Logic_Draft_v2 与 Research_Strategy

日期：2026-10-23。评审工具：skill `scientific-thinking-scholar-evaluation`（九项评审表，1–5 分）。评审人：Claude，依据 `Research_Strategy.md` 第 6 节的方法论立场评，不按实证论文的标准扣分。
范围：**comparative + comprehensive**，两份文件各评一遍，再合并"必须解决的问题"。
文件类型：`Research_Strategy.md` = 研究提案 / 方法论章节草稿；`Tool_Logic_Draft_v2.md` = 技术设计报告（工作文档，带多层"已取代"标注）。

**读法说明：** 分数只是定位，不代替具体意见；N/A 表示这一项不在文件范围内，不算失分。

---

## A. Research_Strategy.md

### Overall Assessment
- Overall score：**3 / 5**
- Confidence：medium（我是该文件的起草者，自评有偏；文献原文未在本次重读）
- Summary：方向清楚、策略分工合理、局限写得具体，作为"方向标"够用。但它还是一份**立场陈述**，不是**可检验的研究设计**：没有写出研究问题，没有说什么结果会推翻命题，主指标未定，论证的核心概念"阶段"与"热防护"之间的对应关系没有证据支撑。这些缺口都已被文件自己点到，但没有给出解决的路径和时间。

### Dimension Scores

| Dimension | Score | Evidence | Revision priority |
|---|---:|---|---|
| Problem and question | 3 | 命题句清楚（第 1 节），因果方向明确。但没有**研究问题**，"calibrated（校准）"和"year-round public occupation"都没有可观测的定义；"刚好够"是原则不是量 | 高 |
| Literature and context | 3 | 指向了文献笔记和行业扫描，承认 Groat & Wang 未重读。把 Alexander、Hillier 作为逻辑论证的例子是凭通用印象，未核对；没有说明"没有人做过这条链"这一判断的依据（行业扫描只是 B 级） | 中 |
| Methodology | 3 | 一主一验两辅的分工合理，与 Groat & Wang 的"组合策略"一致。缺：逻辑论证的**有效性标准**（怎样算论证成立、怎样算失败）；对照实验的变量（自变量 = 排法 / 体块 / 季节，因变量 = ？）只提了候选 | 高 |
| Data and evidence | 3 | 明确借用相关性文献并要求来源标签，这是对的。但 Cambridge / Sheffield 的中性范围是"从图上读的"，Glasgow 是 2.8 met 的走动数据，用在静坐功能上需要说明 | 中 |
| Analysis | 2 | 第 4 节第 2 条提出三组对照，是正确方向，但基线（"全部 controlled 的传统排法"）如何生成没有定义；评分权重 1 / 0.7 / 0.3 的敏感性没有计划；"渐变序列 70%"这类百分比的含义没有解释 | 高 |
| Results and interpretation | N/A | 文件不含结果 | — |
| Limitations | 3 | 第 5 节具体、不敷衍（相对值、自洽不等于正确）。缺最大的一条：**阶段由围合几何推出，是热防护的代理变量，未验证**；也没提工具的"区域热条件只是相对排序"（WORK_LOG 10-19） | 高 |
| Writing and structure | 4 | 结构清楚，表格好读，第 6 节对 agent 的要求可操作。小问题：第 2 节表格把分类框架的名字和作者混在一起，正式写作要分开 | 低 |
| Citations | 2 | 全文没有一条正式引用，只有文件指针。Groat & Wang、Alexander、Hillier、Lacaton & Vassal 都是转述。作为内部方向标可以，进论文前必须补 | 中 |

### Critical Issues
1. **没有研究问题，也没有可证伪的子命题。** 命题句说"可以被重新诠释为"，这在逻辑上永远成立。需要一个能输、能赢的版本，例如："在同一功能清单和同等活动舒适要求下，按五段渐变排布的社区中心，其需要机械调节的面积（或 controlled 外墙长度）比传统全调节排布少多少；若差异不显著，命题的设计价值不成立。"
2. **"阶段"与"热防护程度"之间没有证据链。** 五段阶段按屋顶、墙数、机械调节推出（Tool_Logic_Draft_v2 第五节第 0 条）。论证说的是热防护，模拟算的是围合几何。温哥华冬季一个"有屋顶加两面墙"的空间比露天暖多少，目前没有任何数据。Lacaton & Vassal 的实测是唯一候选，书还没拿到。
3. **主指标未定。** 没有因变量，第 4 节第 2 条的三组对照就无法解释结果。

### Recommended Revisions
- 在第 1 节命题句下面加一段"研究问题与可检验的子命题"（1 个主问题，2–3 个子命题，每条写明用什么指标、什么结果算支持 / 不支持）。
- 第 4 节第 2 条改成一张表：对照组 × 自变量 × 因变量 × 怎么生成基线。把"controlled 外墙长度"写成**暂定**主指标，并列出备选（controlled 面积占比、需要机械调节的小时数）。
- 第 5 节加一条："阶段是热防护的代理变量；代理是否成立，靠 Lacaton & Vassal 实测和（若可行）Ladybug / Infrared.City 对 buffered 空间的计算来检验。"
- 第 2 节表格加一栏"依据"：哪些判断来自 Groat & Wang 原文、哪些是通用印象。
- 文末加"引用待补"清单（见下 Evidence Checks）。

---

## B. Tool_Logic_Draft_v2.md

### Overall Assessment
- Overall score：**3 / 5**
- Confidence：medium（规则文件和 WORK_LOG 没有逐条交叉核对）
- Summary：作为工具的设计记录，它诚实、可追溯，每条决定都标了日期和决策人，未解决的问题单独列出，这是优点。作为论文的方法依据，它有三个问题：被标为"核心"的阶段 × 活动 × 季节适配表（第五节第 2 条）仍未建立；tempered 阶段在冬季没有任何舒适依据（ASHRAE 适应性模型不适用、PET 范围未批准）；文件被多层"已取代"标注覆盖，读者分不清哪条现在有效。

### Dimension Scores

| Dimension | Score | Evidence | Revision priority |
|---|---:|---|---|
| Problem and question | 3 | 第〇、一节把命题和工具定义讲清楚了。但命题层（thesis）和工具层（功能怎么摆）之间缺一句话说明"工具回答命题的哪一部分、不回答哪一部分" | 中 |
| Literature and context | 3 | 第四、五节把已有部件和来源列出，第五节第 2 条对 ASHRAE 适应性模型适用范围的判断是本稿最好的综合（用项目天气文件算出半年低于 10℃）。但综合到此为止，没有说"那 tempered 用什么" | 高 |
| Methodology | 3 | 流程（第三节）和规则位置（`_shared/Rules/`）足以让另一个人复现工具。缺的是方法层的论证：为什么用围合方式定义阶段、为什么"冬季最低阶段"自动指派、为什么大件优先。这些是设计判断，可以，但要写成"选择及理由"，不是"决定" | 中 |
| Data and evidence | 3 | 天气是机场站、面积只用 Marpole 一个先例、风界限借多伦多、雨不进计算，这些都**标注了**，是好的做法。问题在覆盖：面积库来源单一；活动代谢率两套数值并存（Kenawy 的 1 / 1.2 / 2 与 Zhang 的 1.65 / 4.75 / 8.5）没有说用哪套、为何 | 中 |
| Analysis | 2 | 评分是优先级排序加若干假设权重（1 / 0.7 / 0.3、0.5），没有敏感性检查。更重要的：WORK_LOG 10-22 自己记录了"首层优先排在渐变序列之前""调整后重排只看空白"，即**工具当前优化的不是论证说的东西**。这是 construct validity（构念效度）的偏移，本稿未提 | 高 |
| Results and interpretation | N/A | A–D 方案的数值在 WORK_LOG，不在本稿。若要进论文，需要单独的结果文件 | — |
| Limitations | 3 | 第五节的七条开放问题具体。但只列"还没做的"，没列"做了但可能错的"：阶段 = 几何代理；三带是外接矩形划分；Ladybug 只算直射小时、不算辐射；自遮挡不含邻房 | 中 |
| Writing and structure | 2 | 章节编号跳过"六"；第二、三、七、九、十节各带"已取代"标注，有的决定三处重复（阶段指派）。读者需要自己拼出"现在有效的版本"。建议写一份"当前有效逻辑（一页）"放在最前面，历史保留在后 | 高 |
| Citations | 3 | 来源有标签（A / B / C 强度在别的文件），借用都注明了。待核：Sport England 场地尺寸只来自搜索摘要；Zhang 2024 数值内部不一致（已在其笔记里记录）；多伦多 PLW 风限的文件名和年份 | 中 |

### Critical Issues
1. **tempered 阶段在冬季没有舒适依据。** 第五节第 2 条已证明 ASHRAE 适应性模型半年不适用，借用的 PET 范围（Cambridge / Sheffield）用户未批准，"tempered 冬天有多冷"没有来源（WORK_LOG 10-20）。而 tempered 是五段里承接最多功能的一段。整张适配表的中间一截是空的。
2. **"核心"适配表未建立。** 本稿自己说阶段 × 活动 × 季节表是工具的核心（第五节第 2 条），现在只有 `Function_Stage_Skeleton.md` 的草稿和 STAGE_RULES 的 R1–R8。规则能推出最低阶段，但"每种活动在每个季节能在哪些阶段使用"仍没有成表。
3. **工具当前检验的不是论证。** 见 Analysis 一栏。要么把渐变序列和 controlled 聚团提回评分主序，要么在论文里明写"当前版本的排布以紧凑和受晒为先，渐变只作显示"，二选一，不能悬着。

### Recommended Revisions
- 文件最前面加"当前有效逻辑（2026-10-23）"一节，一页以内，只写现在成立的：阶段定义、指派方式、评分优先序、更新规则、约束。旧节保留，标"历史"。
- 第五节第 2 条下面加"tempered 的舒适依据路线"：候选 a) 借 PET 中性范围（待批准）；b) Lacaton & Vassal 冬季花园实测温差；c) 用 EPW 月均温加围合折减做粗估（标为假设）。写明现在选哪条、什么时候换。
- 第四节活动卡：二选一说明代谢率用哪套，另一套怎么处理。
- 新增"做了但可能错的"小节（limitations），列：阶段为几何代理、三带外接矩形、Ladybug 直射小时、无邻房遮挡、机场气象站。
- 补齐章节编号，或改成日期顺序。

---

## C. 合并后的优先次序（两份文件一起看）

| 优先 | 事项 | 影响哪一份 |
|---|---|---|
| 1 | 写出研究问题和 2–3 条可检验子命题，定暂定主指标 | Research_Strategy 第 1、4 节 |
| 2 | tempered 阶段的冬季舒适依据：选一条路线，标注强度 | Tool_Logic_Draft_v2 第五节第 2 条；STAGE_RULES |
| 3 | 决定工具评分主序是否回到渐变优先（WORK_LOG 10-22 四个问题的第 1、3 题） | PLACEMENT_CRITERIA；工具 |
| 4 | 建立阶段 × 活动 × 季节适配表（哪怕第一版全是假设，先成表） | Function_Stage_Skeleton → 正式表 |
| 5 | 阶段作为热防护代理的检验计划（Lacaton & Vassal / 计算） | Research_Strategy 第 5 节 |
| 6 | Tool_Logic_Draft_v2 前置"当前有效逻辑"一页 | 写作 |
| 7 | 补正式引用 | 两份 |

## D. Evidence Checks Needed
- Groat & Wang《Architectural Research Methods》逻辑论证一章：七种策略的原始定义；Alexander、Hillier 是否确为该章例子。
- Lacaton & Vassal《It's Nice Today》（2024）：四个项目冬季缓冲空间的实测温差、测量方法、气候条件。
- Cambridge / Sheffield 的 PET 中性范围：从图上读的数值需回到原文表格或作者数据。
- Zhang 2024 图 6–8：解决其笔记里记录的数值不一致后才能引用。
- Sport England 场地尺寸（30.1 × 21.1 m）：找原文件，不用搜索摘要。
- 多伦多 PLW Terms of Reference：文件全名、年份、页码。
- Marpole 2021 任务书作为唯一面积来源：至少再找一份温哥华社区中心任务书对照。
- Mora & Bean 2018 图 2 的适用范围数值（文献笔记自述"未逐项核对"）。
