# form follows program

**ARCH 540 · Assignment 2 · milestone submission (29 October 2026)**
A browser-based design tool that lays out a community centre in Vancouver as a *gradient of climatic protection* rather than a binary of conditioned / unconditioned space.

中文说明见 [README.zh.md](README.zh.md).

## The idea

> Conditioned space can be reinterpreted as a calibrated gradient between climatic protection and environmental exposure, supporting year-round public occupation in Vancouver.

The thesis replaces the air-conditioned / not-air-conditioned split with five stages of protection:

**exposed → protected → buffered → tempered → controlled**

Massing and enclosure decide how much protection a space offers; that protection decides which activities the space can host. A set of rules (R1–R8, in `02_Prototypes/_shared/Rules/STAGE_RULES.md`) assigns each activity the stage that is *just enough* for it, so that active conditioning is used only where it is needed. The tool is the instrument that runs and tests this argument: the thesis is a logical argument, the tool is its simulation, precedents feed the rules, and correlational literature is only borrowed for thresholds (see `01_Research/Research_Strategy.md`).

## The tool

**Live:** https://ay-xa.github.io/ARCH-540-form-follows-program/02_Prototypes/Version_01/
**Local:** open `02_Prototypes/Version_01/index.html` in a browser. It is a single file with no installation; it needs an internet connection for the 3D library, the animation library and Vancouver Open Data (site boundaries). Climate data (CWEC2020 for Vancouver) is embedded.

Six steps, in the order a designer works:

| Step | What happens |
|---|---|
| 1 Choose functions | Tick the functions from a library of 23 (based on the Marpole Community Centre brief, 2021, and Vancouver’s Community Centre Strategy); a gap check compares the list with the strategy and 14 precedents. |
| 2 Areas and heights | Confirm net areas and minimum clear heights; totals show how much floor area is needed. |
| 3 Choose site | Pick a park or parcels on a map of Vancouver’s 22 local areas; context buildings within about 200 m are loaded. |
| 4 Massing | Push and pull blocks in 3D, set roof and walls (which fix each block’s stage), levels and the circulation skeleton; four generated massing options to start from. |
| 5 Confirm | The tool lays the functions out on each level by sun exposure, adjacency, stage and the gradient sequence. Click a room and a decision card explains why it is there, with the rules it triggered and their sources. Axonometric and plan views; English / Chinese; light / dark. |
| 6 Show | Presentation view: the building and its context bleed in, with sun, enclosure stages and seasonal wind. |

Colours on plans and in 3D are the stages, from cool and pale (exposed) to warm and solid (controlled).

## Where things are

| Folder / file | Contents |
|---|---|
| `02_Prototypes/Version_01/` | The tool (`index.html`) and its own README (what each step does, what changed when). |
| `02_Prototypes/_shared/Rules/` | Stage rules, placement criteria and the function library, with the status of every number (verified / borrowed / inferred / assumed / user decision). |
| `01_Research/` | Research strategy, literature notes (PET / UTCI thresholds, climate analogues, Vancouver documents), the Marpole brief, and the circulation patterns drawn from 21 precedent plans. |
| `03_Data/` | Data sources and the scripts that convert the EPW climate file into the embedded JavaScript. |
| `04_Presentation/screenshots/` | Dated screenshots of the tool as it developed. |
| `Tool_Logic_Draft_v2.md`, `Architecture_Massing_Level_Space_Program.md` | The tool’s logic and a step-by-step build record. |
| `Function_Area_Assumptions.md`, `Function_Stage_Skeleton.md`, `Literature_To_Tool_Decisions.md` | How areas, stages and literature became rules in the tool. |

## Notes

- Precedent drawings (three PDFs and 41 plan images) are **not** in this repository for copyright reasons; they are cited by source in `01_Research/Circulation_Patterns.md`.
- Literature PDFs are kept outside the repository (see the Chinese README).
- Many numbers are assumptions and are labelled as such in the function library and the rules; nothing here is a building-code or planning requirement unless its source says so.
- This repository is a snapshot of the `Assignment_2` folder of the working repository [Ay-xa/ARCH-540](https://github.com/Ay-xa/ARCH-540), split out with its commit history. Tag: `submission-2026-10-29`.

ARCH 540, UBC School of Architecture and Landscape Architecture, 2026. Built with Claude Code as a design and coding assistant. Libraries: three.js (MIT), anime.js (MIT). Data: City of Vancouver Open Data (Open Government Licence – Vancouver); climate file from Climate.OneBuilding.Org (CWEC2020).
