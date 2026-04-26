北宋行政规划校准数据包 v16
==========================

本包把上一轮仍缺的几类层继续补齐到“可用于沙盘/游戏原型”的状态：

1. v13 缺面清单中 2780 个官方府州面外点，已全部解析进 v15 规划面，v16 未覆盖为 0。
2. 华北、西北、西南、开封中原等区域继续使用全域县级/府州级规划面补齐显示。
3. 新增北宋水系、驿路/漕运/边防道路、交通节点、命名山脉、谭图线稿升格队列和游戏 zoom 层切片。
4. 所有推定层都保留 `AUTHORITY`、`CONFIDENCE`、`PROMOTION_RULE` 等字段，避免把规划层误当成 CHGIS 官方边界。

优先使用
--------
- layers/zz_ns_game_layers_reference_map_v16.png：v16 综合参考图，含 DEM、行政面、水系、道路、山脉、节点。
- layers/zz_ns_admin_gap_points_resolved_v16.geojson：2780 个缺面点的规划面归属结果。
- layers/zz_ns_admin_gap_worklist_v16.geojson：v16 剩余缺面清单，当前为 0。
- layers/zz_ns_county_full_planning_surfaces_v15.geojson：县级规划面，共 1919 面。
- layers/zz_ns_prefecture_full_planning_surfaces_v15.geojson：府州级规划面，共 639 面。
- layers/zz_chgis_official_song_prefecture_polygons_v7.geojson：CHGIS 官方北宋府州面，共 434 面，仍为权威边界层。
- layers/zz_ns_hydro_calibrated_v16.geojson：北宋命名水系校准层，共 7 条。
- layers/zz_ns_transport_routes_calibrated_v16.geojson：驿路、漕运、边防道路校准层，共 9 条。
- layers/zz_ns_transport_nodes_calibrated_v16.geojson：城池、关隘、转运、渡口等交通节点，共 52 个。
- layers/zz_ns_named_mountains_calibrated_v16.geojson：命名山脉/地貌骨架校准层，共 16 条。
- layers/zz_tan_linework_promotion_queue_v16.geojson：谭图线稿升格队列，共 230 条，仍不是最终边界。
- layers/zz_game_zoom_slice_manifest_v16.json：z7、z8-z9、z10-z11 游戏层级规则。

已经校正
--------
- 行政点名空缺：主工作点层已统一简体中文；残余缺面点已通过上级行政区/最近规划面归属补入。
- v13 缺面点：2780 个全部补入规划显示面，剩余 0。
- DEM：已使用 AWS Open Data Terrain Tiles / Mapzen Terrarium z8，覆盖 94E-126E、17N-43N，共 528 张瓦片。
- 华北、西北、西南、开封中原：不再只显示点，已有全域规划面承托。
- 河流水系：黄河、汴河/通济渠、淮河、汉水、长江中游、江南运河/两浙水网、蜀中水运骨架已进入 v16 参考层。
- 道路/漕运：东京-西京-关中、河北边防、河东-麟府、秦凤-泾原、川陕、淮南漕运、江南运河、江南西-广南、荆襄江汉等路线已进入 v16 参考层。
- 山脉/地貌：太行、燕山、吕梁、秦岭、大别、南岭、武夷等命名骨架已进入 v16 校准层。
- 游戏切片：z7 全国层、z8-z9 路州层、z10-z11 县乡层已拆分。

边界说明
--------
- `AUTHORITY=CHGIS_OFFICIAL`：CHGIS 官方边界。
- `AUTHORITY=INFERRED_FROM_ADMIN_POINT_VORONOI`：由行政点推定的规划面，不是官方边界。
- `AUTHORITY=HISTORICAL_GAME_REFERENCE`：为游戏/沙盘使用的历史参考线或节点，不是最终史实几何。
- `NOT_CHGIS_ORIGINAL_BOUNDARY=1` 或 `NOT_FINAL_GEOMETRY=1`：明确标记该层不能当成官方边界。
- `PROMOTION_RULE`：说明后续怎样用谭图、CHGIS 原始资料、地方志、实测地形和拓扑检查升格。

来源
----
- CHGIS 官方数据：Harvard Dataverse CHGIS，https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/I0Q7SM
- CHGIS 项目说明：https://chgis.fas.harvard.edu/
- DEM：AWS Open Data Terrain Tiles / Mapzen Terrarium，https://registry.opendata.aws/terrain-tiles/
