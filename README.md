# honkai-star-rail-achievement-data

A bilingual, formula-driven achievement register for *Honkai: Star Rail*
versions 4.4, 4.5, and 4.6. The 4.6 release consolidates 1,950 source IDs into
1,885 countable rows; the 4.4 and 4.5 workbooks remain unchanged. Mutually exclusive
outcomes share one row, while completion and Stellar Jade remain formula-bound.
The register tracks progress; it is not an official game database.

《崩坏：星穹铁道》4.4、4.5 与 4.6 版双语成就登记册。4.6 版将 1,950 个源 ID
合并为 1,885 个可计数行，并原样保留 4.4 与 4.5 工作簿。互斥结果共用一行，完成进度
与星琼统计由公式约束。本项目用于记录进度，并非官方游戏数据库。

---

## Files | 文件

```text
.
├── LICENSE
├── README.md
├── hsr-achievement-register_en_v4.4.xlsx
├── hsr-achievement-register_en_v4.5.xlsx
├── hsr-achievement-register_en_v4.6.xlsx
├── hsr-achievement-register_zh_v4.4.xlsx
├── hsr-achievement-register_zh_v4.5.xlsx
├── hsr-achievement-register_zh_v4.6.xlsx
├── stardb-achievements_en_20260727.json
├── stardb-achievements_en_20260826.json
└── stardb-achievements_en_20260929.json
```

| Path | Role |
|------|------|
| `hsr-achievement-register_en_v4.4.xlsx` | unchanged English 4.4 release · 原样保留的英文 4.4 版 |
| `hsr-achievement-register_en_v4.5.xlsx` | English 4.5 baseline; every status starts as `Not completed` · 英文 4.5 基准表 |
| `hsr-achievement-register_en_v4.6.xlsx` | English 4.6 baseline; every status starts as `Not completed` · 英文 4.6 基准表 |
| `hsr-achievement-register_zh_v4.4.xlsx` | unchanged Chinese 4.4 release · 原样保留的中文 4.4 版 |
| `hsr-achievement-register_zh_v4.5.xlsx` | Chinese 4.5 baseline; every status starts as `未完成` · 中文 4.5 基准表 |
| `hsr-achievement-register_zh_v4.6.xlsx` | Chinese 4.6 baseline; every status starts as `未完成` · 中文 4.6 基准表 |
| `stardb-achievements_en_20260727.json` | unmodified StarDB English API response for the 4.4 release · 4.4 版 StarDB 英文 API 原始响应 |
| `stardb-achievements_en_20260826.json` | unmodified StarDB English API response for the 4.5 release · 4.5 版 StarDB 英文 API 原始响应 |
| `stardb-achievements_en_20260929.json` | unmodified StarDB English API response for the 4.6 release · 4.6 版 StarDB 英文 API 原始响应 |

---

## Dataset | 数据集

| Measure | 4.4 | 4.5 | 4.6 | Rule |
|---------|----:|----:|----:|------|
| Countable rows · 可计数行 | 1,806 | 1,858 | 1,885 | one row per achievement or mutually exclusive outcome group · 单项成就或一组互斥结果计为一行 |
| Source IDs · 源 ID | 1,869 | 1,921 | 1,950 | raw records before consolidation · 合并前的原始记录 |
| Alternative groups · 互斥组 | 50 | 50 | 51 | 38 two-way, one four-way; three-way groups increase from 11 to 12 in 4.6 · 38 组二选一、1 组四选一；4.6 三选一由 11 组增至 12 组 |
| Total Stellar Jade · 总星琼 | 10,685 | 10,995 | 11,155 | live formula in each workbook · 每份工作簿均由公式计算 |
| Snapshot date · 快照日期 | 2026-07-27 | 2026-08-26 | 2026-09-29 | date of the archived StarDB response · StarDB 原始响应的归档日期 |

---

## Sources | 来源

| Scope | Source | Use |
|-------|--------|-----|
| English text and base metadata · 英文文本与基础元数据 | [StarDB English Achievements API](https://stardb.gg/api/achievements?language=en) | category, name, condition, base reward, and archived raw responses · 成就集、名称、条件、基础奖励与原始快照 |
| 4.4 Chinese text · 4.4 中文文本 | working Chinese checklist · 整理前中文清单 | 4.4 Chinese register and first-obtainable version convention · 4.4 中文登记册与首次可获取版本口径 |
| Choice branches · 互斥分支 | [StarRailRes CN](https://github.com/Mar-7th/StarRailRes/blob/b95e75c7e1273d819d20c530c0b7e13a3ef19fb4/index_new/cn/achievements.json) · [StarRailRes EN](https://github.com/Mar-7th/StarRailRes/blob/b95e75c7e1273d819d20c530c0b7e13a3ef19fb4/index_new/en/achievements.json) | cross-check of the 50 inherited mutually exclusive groups · 核对继承的 50 个互斥组 |
| 4.5 client data · 4.5 客户端数据 | [AchievementData](https://github.com/DimbreathBot/TurnBasedGameData/blob/768daeb9d791dbe4854dcfe2bc0b1335a87f8722/ExcelOutput/AchievementData.json) · [TextMapCHS](https://github.com/DimbreathBot/TurnBasedGameData/blob/768daeb9d791dbe4854dcfe2bc0b1335a87f8722/TextMap/TextMapCHS.json) · [TextMapEN](https://github.com/DimbreathBot/TurnBasedGameData/blob/768daeb9d791dbe4854dcfe2bc0b1335a87f8722/TextMap/TextMapEN.json) · [QuestData](https://github.com/DimbreathBot/TurnBasedGameData/blob/768daeb9d791dbe4854dcfe2bc0b1335a87f8722/ExcelOutput/QuestData.json) · [RewardData](https://github.com/DimbreathBot/TurnBasedGameData/blob/768daeb9d791dbe4854dcfe2bc0b1335a87f8722/ExcelOutput/RewardData.json) | Chinese text and auditable order for the 52 additions in 4.5; reward cross-check · 4.5 新增 52 条记录的中文文本、可审计排序与奖励核对 |
| 4.6 Chinese text · 4.6 中文文本 | [StarRailRes CN](https://github.com/Mar-7th/StarRailRes/blob/541e1100dcfe9a299c6bd500c6d3c4115e0451e4/index_new/cn/achievements.json) | Chinese text for the 29 additions in 4.6 · 4.6 新增 29 条记录的中文文本 |
| 4.6 client data · 4.6 客户端数据 | [AchievementData](https://github.com/DimbreathBot/TurnBasedGameData/blob/6b2bc17ebf461e497ba0dd0ffd44875f1866762b/ExcelOutput/AchievementData.json) · [QuestData](https://github.com/DimbreathBot/TurnBasedGameData/blob/6b2bc17ebf461e497ba0dd0ffd44875f1866762b/ExcelOutput/QuestData.json) · [RewardData](https://github.com/DimbreathBot/TurnBasedGameData/blob/6b2bc17ebf461e497ba0dd0ffd44875f1866762b/ExcelOutput/RewardData.json) · [FinishWay](https://github.com/DimbreathBot/TurnBasedGameData/blob/6b2bc17ebf461e497ba0dd0ffd44875f1866762b/ExcelOutput/FinishWay.json) | auditable order and reward cross-check for the 29 additions in 4.6; inherited choice-group cross-check · 4.6 新增 29 条记录的可审计排序与奖励核对；既有互斥组核对 |

The dated JSON snapshots are retained unmodified as primary evidence; CSV
duplicates would add format, not information.

按日期归档的 JSON 快照保持原样，作为原始证据；CSV 副本只增加格式，不增加信息。

---

## Use | 使用

Open the workbook for the desired version and language, then edit `Status` /
`状态`. The six headline metrics recalculate from status and Stellar Jade; no
external script is required.

打开所需版本与语言的工作簿，再修改 `Status` / `状态`。顶部六项指标随状态与星琼
数据自动计算，无需外部脚本。

---

## Limits | 边界

StarDB, StarRailRes, and TurnBasedGameData are third-party community sources,
not HoYoverse publications. The working Chinese checklist is not redistributed,
so the 4.4 Chinese workbook is a release artifact rather than a fully
reproducible build surface. Existing rows retain its category order and
first-obtainable `Version` convention; a small number of values therefore
postdate StarDB's introduction version. With no equivalent 4.5 or 4.6 checklist,
additions in these versions retain the existing category blocks and follow
AchievementData Priority descending within each category, equivalent here to
ID ascending.

StarDB、StarRailRes 与 TurnBasedGameData 均为第三方社区来源，并非 HoYoverse
官方发布。整理前中文清单不随仓库分发，因此 4.4 中文工作簿是发布工件，而非可由
本仓库完整重建的数据集。既有条目保留其分类顺序与首次可获取版本口径，少量版本值
因此晚于 StarDB 记录的加入版本。因无对应的 4.5 与 4.6 中文清单，这两个版本的新增
记录沿用既有分类块，并在各分类内按 AchievementData 的 Priority 降序排列（本次等同于 ID 升序）。

---

## New in 4.5 | 4.5 新增

Reward basis: the 4.5 workbooks use 10 Stellar Jade for IDs 4035501–4035509
from client reward data; the unmodified 2026-08-26 StarDB snapshot records 5 Stellar Jade.
This changes the 52-addition subtotal from StarDB's 265 to the client-aligned
310, producing a workbook total of 10,995.

奖励口径：4.5 工作簿依据客户端奖励数据，将 ID 4035501–4035509 记为 10 星琼；
未修改的 2026-08-26 StarDB 快照记为 5 星琼。由此，52 条新增记录的小计从 StarDB 的 265
调整为与客户端一致的 310，工作簿总计为 10,995 星琼。

---

## New in 4.6 | 4.6 新增

Grouping basis: the 4.6 workbooks consolidate the 4.5 IDs 4055507–4055509
into one three-way group based on StarDB groups and client FinishWay data.
The 29 additions add 170 Stellar Jade; consolidating the three inherited rows
removes two countable rows and 10 Stellar Jade, producing 1,885 rows and
11,155 Stellar Jade. The 4.5 workbooks remain unchanged.

分组口径：4.6 工作簿依据 StarDB 分组与客户端 FinishWay 数据，将 4.5 的
ID 4055507–4055509 合并为一组三选一结果。29 条新增记录增加 170 星琼；
合并三条既有记录减少 2 个可计数行与 10 星琼，工作簿总计为 1,885 行、
11,155 星琼。原 4.5 工作簿不变。

---

## Encoding | 编码

Text files use UTF-8 without BOM. · 文本文件采用 UTF-8，无 BOM。

---

## License | 许可

MIT License (see `LICENSE`). Game text, names, marks, and third-party metadata
remain with their respective rights holders. This project is independently
maintained and is not endorsed by HoYoverse, StarDB, StarRailRes, or
TurnBasedGameData.

本项目采用 MIT 许可证（见 `LICENSE`）。游戏文本、名称、商标与第三方元数据的
权利归各自权利人所有。本项目独立维护，未获 HoYoverse、StarDB、StarRailRes 或
TurnBasedGameData 背书。

---

*The register records progress; the sources bound its claims. · 登记册记录进度；来源限定主张。*
