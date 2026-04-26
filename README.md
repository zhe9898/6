# Northern Song 2.5D Sandtable Reference

这个仓库给 Gemini / GPT / Kimi / 美术同学看的，不是把北宋行政 GIS 原样端上画面。

主方向已经改成：全国大地图按宋代《华夷图》《禹迹图》的石刻堪舆总图语言来做。全国层看海陆、山脉、水系、州府、关隘、驿站、漕运和边防通道；不要做现代 DEM 浮雕，也不要铺县界。2.5D 沙盘只进入区域/局部可操作层。

## Start Here

- `ai_art_brief/README.md`
- `ai_art_brief/STYLE_TARGET.md`
- `ai_art_brief/VISUAL_QUALITY_BAR.md`
- `ai_art_brief/HISTORICAL_LABEL_ERRATA.md`
- `ai_art_brief/ART_DIRECTION.md`
- `ai_art_brief/REQUIREMENTS_AND_LIMITS.md`
- `ai_art_brief/MODEL_HANDOFF_PROMPT.md`
- `ai_art_brief/images/00_primary_pressure_network_kanyu_reference.png`
- `ai_art_brief/images/01_style_target_pressure_network_concept.png`
- `ai_art_brief/images/01_full_game_layers_v16.jpg`

Preview:

![Northern Song pressure network kanyu reference](ai_art_brief/images/00_primary_pressure_network_kanyu_reference.png)

## Scale Rule

- `z7 全国层`：华夷图 / 禹迹图式堪舆总图，海陆硬分，名山大川、州府、关隘、驿站、水陆交通清楚；不做 DEM 浮雕，不铺县界，不铺行政补面。
- `z8-z9 区域层`：开始进入 2.5D 沙盘，路、州、转运、边防、漕运、山口和渡口成为主体；府州区域感可以弱显示。
- `z10-z11 局部层`：县乡、城池、军寨、渡口、驿站、市场和关隘进入可操作沙盘；县级边界可以露硬边。

## Data Package

轻量拆分层在：

- `package_v16_primary_layers/`

完整大包仍在 GitHub Release：

- Release page: https://github.com/zhe9898/6/releases/tag/northern-song-v16
- Direct asset: https://github.com/zhe9898/6/releases/download/northern-song-v16/northern_song_filled.zip

## Source Roles

- CHGIS：行政点和官方府州几何的权威参考，但不强制决定全国层视觉。
- 谭图：山川形势、边界修形和历史地图语言参考，不直接替代 CHGIS。
- DEM：只作为地貌位置校准和局部沙盘参考；不要把全国图做成 DEM 浮雕。
- 1820 / Natural Earth 水系：提供水网密度和海岸陆地分离参考，后续再校北宋定年水系。
