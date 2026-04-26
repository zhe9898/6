# 可直接复制给 Gemini / GPT / Kimi 的提示词

## 中文提示词

你是游戏美术总监和历史地图视觉设计师。请阅读这个仓库的 `ai_art_brief` 目录，尤其是：

- `ai_art_brief/ART_DIRECTION.md`
- `ai_art_brief/REQUIREMENTS_AND_LIMITS.md`
- `ai_art_brief/images/00_contact_sheet.jpg`
- `ai_art_brief/images/01_full_game_layers_v16.jpg`

任务：为一款北宋行政地理 2.5D 沙盘游戏制定美术基调。

请输出：

1. 一段总体美术方向。
2. 3 套可选视觉方案，但都必须保持北朝上、行政/水系/道路/地貌分层可读。
3. 每套方案的色彩板，写出 6-10 个颜色和用途。
4. 全国层 z7、路州层 z8-z9、县乡层 z10-z11 的显示规则。
5. ComfyUI / SDXL / Midjourney 可用的正向提示词和反向提示词。
6. 不能画错的历史和地图限制。
7. 一张主视觉应该如何构图。

硬性限制：

- 不要做现代地图。
- 不要做泛古风海报。
- 不要把规划面当 CHGIS 官方边界。
- 不要把谭图线稿当最终边界。
- 不要让水系、道路、山脉变成装饰线。
- 不要使用现代省界、现代高速路、铁路、机场、现代城市天际线。
- 必须使用简体中文说明。

## English Prompt

You are an art director and historical map visual designer for a strategy game. Read the `ai_art_brief` directory first, especially:

- `ai_art_brief/ART_DIRECTION.md`
- `ai_art_brief/REQUIREMENTS_AND_LIMITS.md`
- `ai_art_brief/images/00_contact_sheet.jpg`
- `ai_art_brief/images/01_full_game_layers_v16.jpg`

Create an art direction guide for a Northern Song dynasty 2.5D administrative geography sandbox map.

Output:

1. Overall visual direction.
2. Three visual approaches.
3. A palette for each approach.
4. Layer rules for z7, z8-z9, and z10-z11.
5. Positive and negative prompts for ComfyUI / SDXL / Midjourney.
6. Historical and cartographic constraints.
7. Composition guidance for the main visual.

Hard constraints:

- North-up geography.
- Do not make a modern navigation map.
- Do not make a generic fantasy or poster-style ancient map.
- Do not treat inferred planning surfaces as official CHGIS boundaries.
- Do not treat Tan atlas linework as final boundaries.
- Keep hydrography, roads, terrain, administrative areas, and nodes visually distinct.
