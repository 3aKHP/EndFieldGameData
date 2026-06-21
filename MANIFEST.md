# Release Manifest

Records what each Release contains, for traceability.

## v0.2.0 (2026-06-22)

**Asset**: `endfield-tables.zip` (23.3 MB)
**SHA-256**: `f36942c203637611b0ae41bc7d5c50a912daea364ac289f8ab74b88cbf55c926`

**Source**: endfield_research_kit export dated 2026-06-22

**Contents**:

| File | Size (bytes) | Description |
|------|-------------|-------------|
| tables/CharacterTable.json | 9,076,161 | 29 playable characters |
| tables/EnemyTable.json | 140,811 | Enemy instances |
| tables/EnemyTemplateTable.json | 5,116 | Enemy stat templates |
| tables/EnemyDisplayInfoTable.json | 70,866 | Enemy display metadata |
| tables/EquipTable.json | 522,185 | Equipment stats |
| tables/EquipItemTable.json | 28,708 | Equipment item entries |
| tables/CharProfessionTable.json | 1,377 | 6 professions (近卫/重装/辅助/术师/先锋/突击) |
| tables/CharTypeTable.json | 1,006 | 5 element types (物理/结晶/火/自然/脉动) |
| tables/CharacterTagTable.json | 16,239 | Character tags |
| tables/ItemTable.json | 2,314,342 | Items & materials |
| i18n/CN.json | 9,319,568 | Simplified Chinese strings |
| i18n/EN.json | 10,231,513 | English strings |
| i18n/JP.json | 11,619,156 | Japanese strings |
| i18n/TC.json | 9,319,636 | Traditional Chinese strings |
| i18n/KR.json | 11,628,715 | Korean strings |

**Character ID format**: `chr_NNNN_slug` (e.g. `chr_0002_endminm` = 管理员/Endministrator)

**Localization key format**: int64 hashes stored as strings in i18n files, referenced as numbers in table `{id, text}` fields (consumers must use int64-safe JSON parsing).
