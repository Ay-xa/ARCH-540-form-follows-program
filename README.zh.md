# form follows program — ARCH 540 Assignment 2 · 阶段性提交（2026-10-29）

**Milestone submission** of the Assignment 2 folder from the ARCH-540 working repository, with its commit history (18 commits, 2026-10-14 → 10-29).
这是 ARCH-540 工作仓库里 `Assignment_2` 文件夹的阶段性提交版，连同它的提交历史一起拆出来；之后的修改继续在工作仓库里做。英文介绍见 `README.md`。

## 从哪里看起 / Where to start

| 要看什么 | 位置 |
|---|---|
| **工具本身**（form follows program，六步：选功能 → 面积与净高 → 选场地 → 体块推演 → 确认体块与功能 → 效果展示） | `02_Prototypes/Version_01/index.html`。直接用浏览器打开即可；需要联网（three.js、anime.js 从 CDN 加载，场地数据查温哥华开放数据）。在线版（GitHub Pages）：https://ay-xa.github.io/ARCH-540-form-follows-program/02_Prototypes/Version_01/ |
| 工具的用法和每一步做了什么 | `02_Prototypes/Version_01/README.md` |
| 规则与功能库（阶段规则、排布准则、功能库） | `02_Prototypes/_shared/Rules/` |
| 研究策略（thesis 的方向标） | `01_Research/Research_Strategy.md` |
| 文献笔记、案例流线归纳 | `01_Research/`（`Circulation_Patterns.md` 等） |
| 过程截图 | `04_Presentation/screenshots/` |
| 工具逻辑草稿、逐步记录 | `Tool_Logic_Draft_v2.md`、`Architecture_Massing_Level_Space_Program.md` |

## 说明 / Notes

- 案例的图纸（3 份 PDF、41 张平面图）**没有放进这个仓库**（版权），留在本地；它们在 `01_Research/Circulation_Patterns.md` 里按来源引用。
- 气候数据（温哥华 CWEC2020，EPW）已转成 JavaScript 嵌在工具里；转换脚本在 `03_Data/`。
- 文献 PDF 不进仓库，见 `README.md` 下方"文献的存放"。
- 工作仓库：github.com/Ay-xa/ARCH-540（`Assignment_2/`）。本次提交的标签：`submission-2026-10-29`。

---

# Assignment 2

ARCH 540 第二次作业的工作文件夹。建于 2026-10-14，作业题目与方向待定，结构随设计推进再调整。

Assignment 1 的工具（MassShadeLight 及之前的原型）仍留在仓库根目录的 `Openning_Shade_Relation_Tool/`、`Passivehouse_Tool/` 等文件夹里，不搬动——GitHub Pages 的演示链接依赖那些路径。

## 文件夹分工

| 文件夹 | 放什么 |
|---|---|
| `00_Brief/` | 作业要求、评分标准、老师发的资料、课堂笔记。原件照原样放进来，不改名也可以。 |
| `01_Research/` | 调研与先例：参考项目、论文、网页截图、现场照片、自己的草图和想法记录。 |
| `02_Prototypes/` | 工具本身。每一版一个文件夹 `Version_01`、`Version_02`……，旧版不删、不覆盖，方便回头比较。 |
| `02_Prototypes/_shared/` | 几个版本共用的部分（比如计算引擎、公用样式）。只放确实被两个以上版本用到的东西。 |
| `02_Prototypes/Version_XX/rhino/` | 这一版配套的 Rhino / Grasshopper 文件和脚本（`.3dm`、`.gh`、`.py`、`state.json`），跟网页放在同一版文件夹里，搬家时一起搬。 |
| `03_Data/` | 数据：气候文件（EPW）、地图、底图、参考模型。大文件（几十 MB 以上）先问一下要不要进仓库。 |
| `04_Presentation/` | 对外展示：展板、汇报稿、最终提交稿。 |
| `04_Presentation/screenshots/` | 过程截图、GIF、渲染图，按日期或版本命名，例如 `2026-10-20_v01_plan.png`。 |

## 方向标（先读）
研究策略文件：`01_Research/Research_Strategy.md`（用户确认，2026-10-22）。thesis 以 Logical Argumentation（逻辑论证：渐变、刚好够、因果方向）为主干，工具是 Simulation（模拟）用来检验，案例给规则供料，相关性文献只借用阈值。凡处理 thesis 内容的人和 agent 先读它，改规则、评分、数值之前对照它的第 6 节。

## 规则与功能库
工具的规则和功能库放在 `02_Prototypes/_shared/Rules/`（`README.md` 说明状态词汇和 skill 的开放问题；`STAGE_RULES.md` 阶段与分配规则；`FUNCTION_LIBRARY.md` 功能库；`PLACEMENT_CRITERIA.md` 排布的评判准则）。逻辑草稿：`Tool_Logic_Draft_v2.md`（研究命题、已确认的逻辑、外部工具与 AI 代理的方向；`Tool_Logic_Draft.md` 是被取代的旧稿）。工具本身的逐步记录：`Architecture_Massing_Level_Space_Program.md`。文献如何支撑决定：`Literature_To_Tool_Decisions.md`（截至 10-17）。文献笔记在 `01_Research/`（PET / UTCI、相似气候城市、多伦多与墨尔本阈值、温哥华文件、Marpole 任务书、行业扫描、Rhino.Compute）。数据来源：`03_Data/README_data_sources.md`。工具的用法：`02_Prototypes/Version_01/README.md`。

## 文献的存放（2026-10-15 决定）
PDF 不进仓库，放 Google Drive：`G:\My Drive\A - UBC - SALA\M3 Fall 2026\ARCH 548 GP1\Assignment 3  - Progress Review\Supporting_Literature\`，七个文件夹 `01_Problem_Context`、`02_Binary`、`03_Gradient`、`04_Climate_Infrastructure`、`05_Comfort_Thresholds`、`06_Behavior`、`07_Precedents_and_Vernacular`，编号与 Zotero 分类 1–7 一致；文件名 `Author_Year_ShortTitle.pdf`。Zotero（本地接口只读，需保持打开）纳入 ARCH 548 Assignment 1 与 Assignment 3 的分类，外加 Social Catalist & Biophilia、Vernacular；Adaptive Reuse 已过时不用。Miro 板 ARCH 548 GP1：https://miro.com/app/board/uXjVEd_mcn0=/ 。

## 几条习惯

- **一版一个文件夹**：改动大就新开 `Version_02`，不要在 `Version_01` 里反复覆盖。小修可以在当前版本里改。
- **工作记录**仍写在仓库根目录的 `WORK_LOG.md`，每次结束工作时追加一段，不另开记录文件。
- **`.gitkeep`** 是空文件夹里的占位文件，Git 不记录空文件夹，有了它文件夹才会被上传。文件夹里有真东西之后可以删掉它，留着也无妨。
- 命名用英文、下划线、首字母大写（`Version_01`、`Site_Plan.png`），避免空格和中文文件名，Rhino 和网页读路径更稳。

## 待定

- 作业题目、交付要求（放 `00_Brief/` 后在这里补一句摘要和截止日期）。
- 是否沿用 Assignment 1 的共享引擎（`Passivehouse_Tool/01_Prototypes/_shared/`）：沿用就在 `_shared/` 里放一个说明指过去，不复制。
