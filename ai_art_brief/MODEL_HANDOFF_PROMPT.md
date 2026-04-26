# 可直接给 Gemini / GPT / Kimi 的提示词

## 中文提示词

你是游戏美术总监和历史地图视觉设计师。请阅读仓库里的 `ai_art_brief` 目录，尤其先看：

- `ai_art_brief/STYLE_TARGET.md`
- `ai_art_brief/VISUAL_QUALITY_BAR.md`
- `ai_art_brief/images/01_style_target_pressure_network_concept.png`
- `ai_art_brief/ART_DIRECTION.md`
- `ai_art_brief/REQUIREMENTS_AND_LIMITS.md`

任务：为一款北宋地理压力路网游戏制定大地图美术基调。

核心方向：

全国大地图按宋代《华夷图》《禹迹图》的视觉语言来做。它是山川州郡堪舆总图，也是压力路网的底座，不是现代行政地图，不是县界图，不是 GIS 拼接图，也不是 2.5D DEM 浮雕图。全国层必须把海陆、山脉、水系、州府、关隘、驿站、漕运、边防路网分清楚。山脉要用古代舆图式山川符号表达，不能用几条长线当山脉。县界硬边只允许出现在 z10-z11 局部沙盘。

美术质量要求：不能像工程调试图，不能像简单 GIS 截图加古风滤镜。它必须有统一符号系统、克制色彩、清楚文字层级、漂亮的古代舆图气质，并且能让 Unity 继续叠加路线状态、节点状态和压力覆盖层。

可参考 `01_style_target_pressure_network_concept.png` 的气质和层级，但不要照抄里面的地名、年份、边界和路线。

请输出：

1. 总体美术方向。
2. z7 全国华夷禹迹式堪舆总图、z8-z9 区域路州/漕运/边防沙盘、z10-z11 局部县乡沙盘的三层规则。
3. 全国层构图方案：海陆、山脉、水系、州府、关隘、驿站如何组织。
4. 压力路网方案：粮路、商路、官文路线、私货路线、军务路线如何作为覆盖层显示状态。
5. 区域层构图方案：道路、漕运、转运、渡口、山口、军寨如何组织。
6. 局部层构图方案：县界硬边、县乡点、城池和功能节点如何组织。
7. 色彩板：纸底、陆地、海域、山势、主河、支流、道路、节点、压力覆盖层、局部县界。
8. ComfyUI / SDXL / Midjourney 可用的正向提示词和反向提示词。
9. 不能画错的历史、地图和美术质量限制。

外部参照：

- `Hua yi tu`：https://www.loc.gov/item/gm71005081/
- `Yu ji tu`：https://www.loc.gov/item/gm71005080/

硬性限制：

- 全国大地图不显示县界。
- 全国大地图不显示大块行政补面。
- 全国大地图不显示算法拼接三角面。
- 全国大地图必须海陆硬分。
- 全国大地图必须有名山大川、州府、关隘、驿站、水陆交通。
- 全国大地图不要做 2.5D DEM 浮雕。
- 全国大地图必须美术完成度高，不能像程序调试图。
- 底图不能烙死所有玩法信息，要能叠加压力覆盖层。
- 县界只允许出现在 z10-z11 局部沙盘。
- 不要现代地图、省界、国界、高速、铁路、机场、现代城市天际线。
- 不要把规划面当 CHGIS 官方边界。
- 不要把谭图线稿当最终边界。
- 必须使用简体中文说明。

## 给出图模型的正向提示词

北宋华夷禹迹式山川州郡堪舆总图，北朝上，中国古代石刻舆图与纸本堪舆图气质，浅米黄纸底，硬海岸线，海陆分明，渤海黄海东海南海分区清楚，太行山秦岭吕梁山燕山大别山南岭武夷山巴蜀山地以古代舆图式山川符号表现，不能用几根长线条代替山脉，黄河汴河通济渠淮河汉水长江中游江南运河主次清楚，州府名密集但克制，开封洛阳大名太原京兆成都江宁杭州广州桂州等节点以小朱点和短中文注记表示，关隘驿站渡口漕运边防通道以细赭线和小标记表示，计里画方感，刻线感，历史地理游戏地图美术基调，层次清楚，克制，不是现代地图，不是 DEM 浮雕图

## 反向提示词

现代地图，现代省界，现代国界，县界铺满，全国行政区块，彩色政区图，Voronoi 三角拼接，算法缝，谭图瓦片矩形框，错误三角陆地，卫星图，现代 DEM 浮雕，现代 DEM 彩色地形，高速路，铁路，机场，现代城市天际线，奇幻大陆，泛古风海报，装饰性山水画，水墨插画，几根线条当山脉，机械排线山脉，海陆模糊，河流随意蓝线，稀疏节点，文字铺满，南北颠倒，旋转地图，硬行政补面

## English Brief

Create art direction for a Northern Song geography sandbox game. The national map should translate the visual logic of the Song stone maps `Huayi Tu` and `Yu Ji Tu` into a 2.5D sandtable. It must read as an ancient Chinese landform and hydrography map, not a modern GIS administrative map.

Show hard coastlines, separated sea and land, named mountain ranges, major river systems, prefectural nodes, passes, relay stations, ferries, canal routes, and frontier routes. Do not make the national map a modern DEM relief map. Do not show county boundaries or filled administrative polygons at national scale. County boundaries may appear only in local z10-z11 sandbox views.
