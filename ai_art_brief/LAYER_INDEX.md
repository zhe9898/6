# 小型图层索引

这些图层是给 Gemini / GPT / Kimi 看结构用的轻量层，不是完整数据包。

## 水系

- 文件：`layers/zz_ns_hydro_calibrated_v16.geojson`
- 数量：7 条
- 用途：确定黄河、汴河/通济渠、淮河、汉水、长江中游、江南运河、蜀中水运骨架的视觉层级。
- 限制：这是北宋游戏参考层，不是最终定年水系。

## 道路/漕运/边防道

- 文件：`layers/zz_ns_transport_routes_calibrated_v16.geojson`
- 数量：9 条
- 用途：确定驿路、漕运、边防通道如何画。
- 限制：路线是游戏原型层，不是完整史实路网。

## 交通节点

- 文件：`layers/zz_ns_transport_nodes_calibrated_v16.geojson`
- 数量：52 个
- 用途：城池、关隘、转运节点、区域枢纽的视觉标记。
- 限制：不是全量城池/渡口/驿站清单。

## 山脉/地貌

- 文件：`layers/zz_ns_named_mountains_calibrated_v16.geojson`
- 数量：16 条
- 用途：确定太行、秦岭、大别、南岭、燕山、吕梁、武夷等骨架如何与 DEM 结合。
- 限制：山口、岭路、军事用途仍需后续细校。

## 谭图线稿升格队列

- 文件：`layers/zz_tan_linework_promotion_queue_v16.geojson`
- 数量：230 条
- 用途：给边界修形和历史质感参考。
- 限制：`PROMOTION_QUEUE`，不能当最终边界。

## 游戏 zoom 切片

- 文件：`layers/zz_game_zoom_slice_manifest_v16.json`
- 用途：告诉美术和 UI 哪些层在 z7、z8-z9、z10-z11 显示。
