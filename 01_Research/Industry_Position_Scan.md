# 行业定位扫描：环境如何影响建筑布局

日期：2026-10-20。目的：了解这个领域现在的难题和新技术，并找出本 thesis 方向在行业里的位置。

**证据强度：** 本文所有条目都是 **B**（只看到网络搜索摘要，原文没有读）。引用之前要先下载原文核对。

**⭐ 标记：** 使用者确认对研究特别有帮助的条目，优先读原文。

---

## 一、定位（一句话）

行业里的工具多在做两件事：一是"形体 → 性能评分"，比如 Forma、Infrared.City；二是"布局 → 能耗"，比如 EPSAP、EnergAI、多智能体 LLM 布局。本研究做的是第三条链：形体产生**分级的气候保护**，再按季节把**活动**配进合适的区，场地是寒冷多雨的温哥华。目前没有找到把这条链做成工具的先例。

---

## 二、⭐ 重点先例

### ⭐ Philippe Rahm：气象建筑（meteorological architecture）
- 要点：把温度、湿度、光、气压当作建筑的材料。室内被理解为一个有不同温度层的"体积"，家具和活动按温度层布置，人可以在空间里做"热迁徙"（thermal transhumance）。被动策略用对流、传导、辐射、蒸发、热惰性。
- 对本研究的意义：**概念层面的先例**。"按热条件安排活动"这个思路在建筑学里有来历，可以作为五段梯度和活动匹配的理论起点。不同之处在于：Rahm 讲的是概念和装置，本研究要做成规则化、能计算的工具，并按季节匹配。
- 来源：[area-arch](https://www.area-arch.it/en/?p=17422)、[IAAC blog](https://www.iaacblog.com/2014/04/29/philippe-rahm-thermodynamics-cities/)、[worldarchitecture.org](https://worldarchitecture.org/architecture-news/emene/philippe-rahm-describes-meteorological-architecture-as-a-harmonization-of-culture-and-nature.html)、书目 *Philippe Rahm architectes: Constructed Atmospheres*。
- 强度：B。
- 待做：找 Rahm 的书或文章原文，确认"thermal transhumance"的出处和原话，看他有没有给过具体的温度分层或活动分配的例子。

### ⭐ Lacaton & Vassal：《It's Nice Today: On Climate, Comfort, and Pleasure》（Ruby Press, 2024）
- 要点：与环境设计顾问 Atmos Lab 合作，在四个项目里长期实测（从 Latapie 住宅到日内瓦的公寓和办公楼），称这是第一次用科学数据证明冬季花园和温室可以作为高效的热缓冲。冬季关闭时，它们是太阳能集热器，也是外部和采暖室内之间一层预热过的空气。
- 对本研究的意义：
  1. 给"缓冲层（buffered）"提供**实测依据**，而不只是推理。
  2. 可以放进**工具库（tool bucket）**，作为一种调节手法：冬季花园 / 温室缓冲。
  3. "Pleasure"这个立场与热愉悦（alliesthesia）一致，即舒适不等于恒温。
- 注意：研究对象是住宅和办公，不是社区中心；地点是法国和瑞士，气候与温哥华不同。书里的数字不能直接搬用，要先核对。
- 来源：[Ruby Press](https://ruby-press.com/shop/lacaton-vassal-its-nice-today-on-climate-comfort-and-pleasure/)、[lacatonvassal.com](https://lacatonvassal.com/index.php?idp=113)。
- 强度：B。
- 待做：取得书（UBC 图书馆或购买）；摘出四个项目的实测温差、季节和测量方法；记下哪些数字可以作为缓冲层的参考，以及适用条件。

---

## 三、其他相关先例（未标重点）

| 先例 | 要点 | 与本研究的区别 | 来源 |
|---|---|---|---|
| 包含式热分区 / "热洋葱"（thermal zoning by inclusion / "thermal onion"），UCLouvain | 同一栋楼里不同温度的区并存，对舒适要求较低的区可以省能；功能性辅助空间可以做缓冲 | 目标是节能，不是活动匹配；没有做成工具 | [UCLouvain](https://research.dial.uclouvain.be/handle/2078.5/227233) |
| 环境等级（environmental grade） | 按用途给空间设定热环境的控制等级，半户外是室内和室外之间的一级 | 与五段梯度很像，需要对照原文的分级方式 | [MDPI Buildings 15(21):3808](https://www.mdpi.com/2075-5309/15/21/3808) |
| 热愉悦 / 热多样性（thermal alliesthesia） | 不均匀、有变化的热环境可能比恒温更让人满意 | 理论支撑，不是工具 | [Columbia Natural Materials Lab](https://www.arch.columbia.edu/research/labs/17-natural-materials-lab/comfort-well-being) |
| 热缓冲区（thermal buffer zone），McMaster | 环绕建筑的通道把南侧太阳热重新分配到北侧 | 单一构造手法，可以进工具库 | [McMaster](https://macsphere.mcmaster.ca/handle/11375/24216) |

---

## 四、行业难题

1. **性能分析仍是"事后检查"。** Forma 2025–2026 的更新重点就是把分析变成早期的比较输入。[Forma blog](https://blogs.autodesk.com/forma/2026/01/19/my-top-five-favorite-features-of-forma-site-design-in-2025/)
2. **按图像出方案的生成式 AI 不懂性能，也接不上 CAD/BIM。** [ScienceDirect 2026 立面生成综述](https://www.sciencedirect.com/science/article/pii/S0360132326008450)
3. **黑箱：** 设计师看不懂 AI 的理由，就不信任、也不采用。[EC3 2024](https://ec-3.org/publication/ec32024_277/)
4. **半户外过渡空间的研究集中在暖热或温和气候**，冬季温和多雨、且把雨纳入的研究是空白。（2026-10-26 改：原写“寒冷、季节差异大的地区是空白”。依据 [Ma 2026](Ma_2026_sTCA_Corridor_Atrium.md)：西安寒冷地区的中庭走廊已有研究，但西安冬季冷而干，且没有考虑雨。）[MDPI Buildings 15(15):2777](https://www.mdpi.com/2075-5309/15/15/2777)、[Energy & Buildings 综述](https://www.sciencedirect.com/science/article/abs/pii/S0378778825008461)（2026-10-26 已读 Hou 2025 原文核对：支持这一说法，研究地点以东亚、东南亚为主，大多数在湿热气候；笔记见 [Hou_2025_Semi_Outdoor_Transitional_Spaces.md](Hou_2025_Semi_Outdoor_Transitional_Spaces.md)。MDPI 那篇仍只看过摘要）
5. **寒冷城市不能只看日照、风、温度**，还要考虑雪、雨、湿滑地面和能见度。舒适指数仍不含降雨（对应 Literature_To_Tool_Decisions 的 D16）。[Springer IJB 2019](https://link.springer.com/article/10.1007/s00484-019-01852-5)
6. **气候变化让历史天气文件过时。** UVic PCIC 已经做出温哥华的未来天气文件，结论是供暖需求下降、制冷需求上升。规范是否会要求使用未来气候文件**未核实**。[UVic](https://dspace.library.uvic.ca/items/5e8e6684-c704-4d2e-8480-2c81bdbafde9)

---

## 五、新技术

| 类别 | 代表 | 做什么 | 与本研究的关系 | 来源 |
|---|---|---|---|---|
| 云端即时分析 | Autodesk Forma | 日照、风、微气候、噪声，几秒到几分钟出结果 | 只评估形体外部，不分配室内功能 | [Forma blog](https://blogs.autodesk.com/forma/2026/01/19/my-top-five-favorite-features-of-forma-site-design-in-2025/)；扩展接口：[APS blog](https://aps.autodesk.com/blog/exploring-possibilities-forma-extensions-api)、AU 2024 课程 |
| AI 代理模型（surrogate model） | Infrared.City | 用上千次 CFD 训练，1 秒内出风、热、日照结果，接 Rhino/Revit | 将来可以替代本研究的气候输入 | [datadrivenaec](https://datadrivenaec.com/tools/infrared-city)；Salzburg Research 介绍页 |
| 体素城市模型（开源） | VoxCity（kunifujiwara，MIT） | Python 体素城市模型 + 日照 / 天空可见度 / 绿视率分析；数据来自 OSM、Microsoft Footprints、全球 1 m 树冠图、FABDEM | 不是温哥华本地数据；需 Google Earth Engine 账号、Python 3.10–3.13，不能嵌进网页；无 CFD。用户 2026-10-19 决定不合并，只参考其思路在工具内自实现（日照时数 → 辐射 → 替代分带，已做）；以后若做 Colab 对比需先加 OBJ 导出。只读了文档，未运行 | GitHub kunifujiwara/VoxCity |
| LLM + 布局 | 多智能体 LLM 布局系统（ASCE 2025）；EnergAI（Energies 2025） | 气泡图再到平面；以能耗为目标优化 | 最接近本研究的"AI 代理"部分，但不涉及舒适梯度和活动匹配 | [ASCE](https://doi.org/10.1061/JCCEE5.CPENG-7723)、[MDPI Energies](https://www.mdpi.com/1996-1073/18/22/5921) |
| 平面图转通风模型（开源） | AURA（Stanford，2026 预印本） | 在平面图图片或 PDF 上画框 → 自动修正几何 → 带 Airflow Network 的 EnergyPlus 模型；三套公寓的案例显示布局对通风和温度的影响与窗户、材料相当或更大 | 走到“平面 → 通风和温度”就停了，不判断活动需要的防护，也不排功能；住宅、夏季、温和气候。2026-10-26 已读全文，笔记见 [NwagwuUmeEzeoke_2026_AURA_Floor_Plan_Airflow.md](NwagwuUmeEzeoke_2026_AURA_Floor_Plan_Airflow.md)（这一行的证据强度是 A，本文其他条目仍是 B） | SSRN 6791324；[GitHub](https://github.com/juliet29/aura) |
| AI 代理接模拟软件（MCP） | EnergyPlus-MCP + 对话式 / 多代理工作流（LBNL，2026，*J. Building Performance Simulation*） | AI 调用 EnergyPlus 的工具检查、修改、模拟、读结果；判断交给语言模型，确定性步骤交给规则代码；决定权留在人手里 | 只做能耗，不涉及活动匹配和排布；借用的是“AI 判断 + 规则执行”的分工和“白名单”约束。2026-10-26 已读全文（证据强度 A），笔记见 [Li_2026_MCP_Agentic_Energy_Modelling.md](Li_2026_MCP_Agentic_Energy_Modelling.md) | doi 10.1080/19401493.2026.2653969 |
| 进化算法布局 | EPSAP / FPOP | 生成平面，再按热性能优化 | 节能效果只有约 5.5% | [arXiv](https://arxiv.org/abs/1410.0948v1) |
| 城市尺度舒适代理模型 | UHTC-NN 等 | 即时预测城市热舒适地图 | 城市尺度，不是单体建筑 | 见搜索结果，未单独记录 |

---

## 六、本研究的空白（草稿表述）

> 已有研究要么把温度梯度当作节能手段（thermal onion），要么在暖热气候里研究单个半户外空间的舒适阈值，要么让 AI 以能耗为目标排布局。还没有工具把"形体 → 分级气候保护 → 按季节匹配活动"串起来，并放在寒冷多雨的温哥华。概念上可以接续 Rahm 的气象建筑；缓冲层可以用 Lacaton & Vassal 的实测作依据。

**优势：** 冬季温和多雨、且把雨纳入的研究是文献空白（2026-10-26 依据 Ma 2026 修正，原写“寒冷多雨气候”）；规则可解释，回应黑箱问题；以活动匹配取代能耗作为目标。
**弱点：** 没有温哥华阈值（只能借用）；降雨没有依据；气候区目前只是相对排序，还不是计算结果。

---

## 七、待读清单（按优先级）

1. ⭐ Lacaton & Vassal《It's Nice Today》（2024）
2. ⭐ Philippe Rahm 原著（找 thermal transhumance 的出处）
3. UCLouvain "Thermal zoning by inclusion"
4. MDPI Buildings 15(21):3808（environmental grade）
5. Energy & Buildings 2025 半户外过渡空间综述
6. ASCE 2025 多智能体 LLM 布局论文

---

## 八、对工具的影响

三样新技术（Forma、Infrared.City、LLM 布局）如何接入本工具，以及用户的决定，见 `Tool_Logic_Draft_v2.md` 第十五节。
