# Rhino.Compute（Rhino 后台计算服务）的探索笔记

研究日期：2026-10-17。整理日期：2026-10-21（原来只写了一小段在被取代的旧稿 `Tool_Logic_Draft.md` 第六节，优缺点的比较从没有写进文件，这里补全）。
证据强度：**B**。下面关于 Rhino.Compute 的说法来自网络搜索的摘要和论坛帖子标题，我没有打开原文，也没有在这台电脑上试过。

## 1. 它是什么
- 一个在后台运行 Rhino 和 Grasshopper（Rhino 的参数化插件）的服务：外部程序通过网络请求发来参数，它求解 Grasshopper 定义，再把结果传回去。
- **Hops** 是 Grasshopper 里调用它的插件；安装 Hops 时会自动启动一个本机的 Rhino.Compute 实例。
- 本地个人电脑上使用 Rhino 自己的许可，不另收费；放到 Windows 或 Linux 服务器上（如云虚拟机）按核心小时计费（McNeel 常见问题）。Windows Server 本身不被 Rhino 支持。

## 2. 这台电脑的现状（2026-10-17 查文件夹的结果）
- 装有 Rhino 7 和 Rhino 8。
- Ladybug Tools 已安装（用户目录下的 `ladybug_tools` 里有自己的 Python 环境）。
- Rhino 8 的包目录里只有 Rhino-MCP-Platform，**没有看到 Hops**。
- 当时 Rhino 没有打开。

## 3. 和现有的 `Rhino_Live_Link` 的区别
| | `Rhino_Live_Link`（第一次作业的做法） | Rhino.Compute |
|---|---|---|
| 怎么运行 | 在**打开的** Rhino 里运行脚本，网页读取几何并移动滑块 | 后台按请求求解 Grasshopper，**不需要 Rhino 窗口开着** |
| 忙的时候 | Rhino 一忙就超时（脚本里有“Rhino is busy”的处理） | 独立进程 |

## 4. 优势
1. 能从几何自动得到空间卡的数字（天空开敞度、每小时的遮阳比例），设计师改了体块，结果跟着变。
2. 不用开着 Rhino 窗口。
3. 用的是已有的 Grasshopper 定义，包括 Ladybug 的组件，原则上不用重写成别的语言。
4. 本地使用不另收费。
5. 和多伦多《热舒适指南》附录里的做法一致（Rhino、Grasshopper、Ladybug Tools 的工具链）。
6. Python 可以调用。

## 5. 劣势和风险
1. **Ladybug 组件能不能在 Compute 里无窗口运行，没有确认。** McNeel 的人说过很多插件没有在 Compute 环境里测试过，有的在无窗口运行时会让 Grasshopper 加载失败。搜索没有找到 Ladybug 成功或失败的明确记录。**这是最大的不确定。**
2. 启动慢（个别开发者报告第一次请求要等约 45 秒）。
3. 有些功能不支持（迭代类工具如 Kangaroo、Galapagos）；Arup 的 InForm 平台限制一次运算最长 5 分钟（不一定适用于本地）。
4. 安装插件的步骤繁琐：要停服务、装插件、开一次 Rhino 验证、再重启服务；服务如果用另一个 Windows 账户运行，会找不到装在你账户下的插件。
5. 只能在装有 Rhino 的电脑上跑：GitHub Pages 这种静态网页放不下它，别人用要有一台开着 Rhino 的机器；放到服务器上要付费，而且服务器不能是 Windows Server。
6. 项目的维护状态有争议（论坛里有人说开发活动很少，也有维护者说都在积极开发；帖子日期没看到）。论坛里有不少未解决的问题标题，状态未确认。
7. 出错信息常常模糊，排查难。
8. Rhino 8、Hops 和 Compute 的版本要配套。

## 6. 关键判断
- **计算核心（Tmrt、PET、UTCI）是纯 Python，不依赖 Rhino。** Rhino 或 Compute 只用来从几何得到空间卡的数字。第一版可以手填这些数字，或在工具里用简单几何推算。
- 如果只是在课程里本地展示，现有的 `Rhino_Live_Link` 做法可能就够用，不一定需要 Compute。

## 7. 决定（用户 2026-10-17）
**先做本地，最后再考虑自动化。** 顺序：先用手填的空间卡数字跑通“空间卡 → 计算 → 涂色”；同时用 Rhino 里已有的 Ladybug（不经过 Compute）验证几何数字怎么取；最后才决定要不要用 Compute 自动化。

## 8. 试验计划（需要用户同意后才做，至今没有做）
1. 在 Rhino 8 里装 Hops（会改动 Rhino 软件）。
2. 做一个最小的 Grasshopper 定义，对一个示例体块算天空开敞度（需要 Rhino 打开）。
3. 用 Python 通过 Compute 调用它。
4. 看 Ladybug 的组件能不能无窗口运行。

## 9. 和后来决定的关系（2026-10-18 之后）
- 工具后来在网页里自己算空间、日照和辐射（`Version_01/index.html`，见 `Architecture_Massing_Level_Space_Program.md`），没有用到 Rhino.Compute。
- 2026-10-20 讨论外部工具时（`Tool_Logic_Draft_v2.md` 第十五节），Infrared.City 的可能路径是“工具里的体块 → Rhino（已有 `Rhino_Live_Link/`）→ Infrared.City 插件 → 舒适地图 → 按区取平均 → 回到工具”，走的是 `Rhino_Live_Link`，不需要 Compute。所以 Rhino.Compute 目前不是优先事项。

## 来源（搜索摘要，未读原文）
- [Rhino.Compute FAQ](https://developer.rhino3d.com/guides/compute/compute-faq/)
- [Licensing of a local Rhino.Compute server](https://discourse.mcneel.com/t/licensing-of-a-local-rhino-compute-server/136795)
- [Rhino Compute: using a plugin](https://discourse.mcneel.com/t/rhino-compute-using-a-plugin/114867)
- [Rhino Compute not showing all installed plugins](https://discourse.mcneel.com/t/rhino-compute-not-showing-all-installed-plugins/182826)
- [Status of Rhino.Compute](https://discourse.mcneel.com/t/status-of-rhino-compute/147807)
- [InForm (Arup) limitations](https://docs.inform.arup.com/docs/getting-started/limitations/)
- [Hops on Food4Rhino](https://www.food4rhino.com/en/app/hops)
