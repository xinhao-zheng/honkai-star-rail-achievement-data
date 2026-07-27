# honkai-star-rail-achievement-data

A bilingual, formula-driven achievement register for *Honkai: Star Rail*
version 4.4. It consolidates 1,869 source IDs into 1,806 countable rows:
mutually exclusive outcomes share one row, while completion and Stellar Jade
remain formula-bound. The register tracks progress; it is not an official game
database.

《崩坏：星穹铁道》4.4 版双语成就登记册。项目将 1,869 个源 ID 合并为
1,806 个可计数行：互斥结果共用一行，完成进度与星琼统计由公式约束。
本项目用于记录进度，并非官方游戏数据库。

---

## Files | 文件

```text
.
├── LICENSE
├── README.md
├── hsr-achievement-register_en_v4.4.xlsx
├── hsr-achievement-register_zh_v4.4.xlsx
└── stardb-achievements_en_20260727.json
```

| Path | Role |
|------|------|
| `hsr-achievement-register_en_v4.4.xlsx` | English baseline; every status starts as `Not completed` · 英文基准表 |
| `hsr-achievement-register_zh_v4.4.xlsx` | Chinese baseline; every status starts as `未完成` · 中文基准表 |
| `stardb-achievements_en_20260727.json` | unmodified StarDB English API response · StarDB 英文 API 原始响应 |

---

## Dataset | 数据集

| Measure | Value | Rule |
|---------|------:|------|
| Countable rows · 可计数行 | 1,806 | one row per achievement or mutually exclusive outcome group · 单项成就或一组互斥结果计为一行 |
| Source IDs · 源 ID | 1,869 | raw records before consolidation · 合并前的原始记录 |
| Alternative groups · 互斥组 | 50 | 38 two-way, 11 three-way, one four-way · 38 组二选一、11 组三选一、1 组四选一 |
| Total Stellar Jade · 总星琼 | 10,685 | live formula in both workbooks · 两份工作簿均由公式计算 |

---

## Sources | 来源

| Scope | Source | Use |
|-------|--------|-----|
| English text · 英文文本 | [StarDB English Achievements API](https://stardb.gg/api/achievements?language=en) | category, name, condition, and archived raw response · 成就集、名称、条件与原始快照 |
| Chinese text · 中文文本 | working Chinese checklist · 整理前中文清单 | Chinese register and first-obtainable version convention · 中文登记册与首次可获取版本口径 |
| Choice branches · 互斥分支 | [StarRailRes CN](https://github.com/Mar-7th/StarRailRes/blob/b95e75c7e1273d819d20c530c0b7e13a3ef19fb4/index_new/cn/achievements.json) · [StarRailRes EN](https://github.com/Mar-7th/StarRailRes/blob/b95e75c7e1273d819d20c530c0b7e13a3ef19fb4/index_new/en/achievements.json) | cross-check of mutually exclusive names and conditions · 核对互斥名称与条件 |

The JSON snapshot is retained as primary evidence; a CSV duplicate would add
format, not information.

保留 JSON 作为原始证据；CSV 只增加格式，不增加信息。

---

## Use | 使用

Open one workbook and edit `Status` / `状态`. The six headline metrics
recalculate from status and Stellar Jade; no external script is required.

打开任一工作簿并修改 `Status` / `状态`。顶部六项指标随状态与星琼数据自动计算，
无需外部脚本。

---

## Limits | 边界

StarDB and StarRailRes are third-party community sources, not HoYoverse
publications. The working Chinese checklist is not redistributed, so the Chinese
workbook is a release artifact rather than a fully reproducible build surface.
Its `Version` field follows the first-obtainable convention; a small number of
values therefore postdate StarDB's introduction version.

StarDB 与 StarRailRes 均为第三方社区来源，并非 HoYoverse 官方发布。整理前中文
清单不随仓库分发，因此中文工作簿是发布工件，而非可由本仓库完整重建的数据集。
其 `版本` 字段采用首次可获取口径，少量条目因此晚于 StarDB 记录的加入版本。

---

## Encoding | 编码

Text files use UTF-8 without BOM. · 文本文件采用 UTF-8，无 BOM。

---

## License | 许可

MIT License (see `LICENSE`). Game text, names, marks, and third-party metadata
remain with their respective rights holders. This project is independently
maintained and is not endorsed by HoYoverse, StarDB, or StarRailRes.

本项目采用 MIT 许可证（见 `LICENSE`）。游戏文本、名称、商标与第三方元数据的
权利归各自权利人所有。本项目独立维护，未获 HoYoverse、StarDB 或 StarRailRes
背书。

---

*The register records progress; the sources bound its claims. · 登记册记录进度；来源限定主张。*
