# 小型图层索引

这些图层给 Gemini / GPT / Kimi 看结构用。不要把所有图层同时摊开做全国图。

## 主参考

- `STYLE_TARGET.md`
- 作用：全国大图主方向，华夷禹迹式山川州郡堪舆总图。
- 限制：不要从程序渲染图定画风。

## 数据参考图

- `images/01_full_game_layers_v16.jpg`
- 作用：看海陆、水系、点位、交通、地形数据关系。
- 限制：不能照画风；不能当最终美术图。

## 行政点

- `package_v16_primary_layers/layers/zz_ns_admin_gap_points_resolved_v16.geojson`
- 作用：州府、县乡、补点的全量位置参考。
- 限制：全国层只取主要州府和关键节点；县乡密点进入局部层。

## CHGIS 官方府州面

- `package_v16_primary_layers/layers/zz_chgis_official_song_prefecture_polygons_v7.geojson`
- 作用：官方行政面参考。
- 限制：全国美术层不强制铺满，不拿来做主视觉。

## 规划补面

- `package_v16_primary_layers/layers/zz_ns_prefecture_full_planning_surfaces_v15.geojson`
- `package_v16_primary_layers/layers/zz_ns_county_full_planning_surfaces_v15.geojson`
- 作用：游戏局部沙盘和缺面诊断参考。
- 限制：不是 CHGIS 官方边界；不能拿来覆盖全国层。

## 海陆 / 海岸

- `package_v16_primary_layers/layers/zz_ne_50m_land_clipped_v21.geojson`
- `package_v16_primary_layers/layers/zz_ne_50m_coastline_clipped_v21.geojson`
- 作用：解决海边陆地分不清的问题。
- 限制：现代海岸参考，服务视觉清晰度，不等于宋代精确海岸。

## 水系

- `package_v16_primary_layers/layers/zz_ns_hydro_calibrated_v16.geojson`
- 作用：黄河、汴河/通济渠、淮河、汉水、长江中游、江南运河等主水系层级。
- 限制：北宋游戏参考层，不是最终定年水系。

## 道路 / 漕运 / 边防

- `package_v16_primary_layers/layers/zz_ns_transport_routes_calibrated_v16.geojson`
- 作用：驿路、漕运、边防通道的视觉骨架。
- 限制：候选路网，不是完整史实路网。

## 交通节点

- `package_v16_primary_layers/layers/zz_ns_transport_nodes_calibrated_v16.geojson`
- 作用：城池、关隘、转运节点、渡口、驿站的标记参考。
- 限制：不是全量清单。

## 山脉 / 地貌

- `package_v16_primary_layers/layers/zz_ns_named_mountains_calibrated_v16.geojson`
- 作用：太行、秦岭、大别、南岭、燕山、吕梁、武夷等命名山脉与 DEM 山势结合。
- 限制：这是山体和山名位置参考；全国层不要做成 DEM 浮雕。

## 谭图线稿

- `package_v16_primary_layers/layers/zz_tan_linework_promotion_queue_v16.geojson`
- 作用：修形和历史地图语言参考。
- 限制：`PROMOTION_QUEUE`，不是最终边界。

## 游戏 zoom 切片

- `package_v16_primary_layers/layers/zz_game_zoom_slice_manifest_v16.json`
- 作用：说明 z7、z8-z9、z10-z11 分别显示什么。
