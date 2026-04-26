# 最终交付说明 v16

## 主成果
- 综合参考图：`layers/zz_ns_game_layers_reference_map_v16.png`
- 行政缺面解析结果：`layers/zz_ns_admin_gap_points_resolved_v16.geojson`
- 剩余缺面清单：`layers/zz_ns_admin_gap_worklist_v16.geojson`
- 县级规划面：`layers/zz_ns_county_full_planning_surfaces_v15.geojson`
- 府州级规划面：`layers/zz_ns_prefecture_full_planning_surfaces_v15.geojson`
- CHGIS 官方府州面：`layers/zz_chgis_official_song_prefecture_polygons_v7.geojson`
- 北宋水系：`layers/zz_ns_hydro_calibrated_v16.geojson`
- 驿路/漕运/边防道路：`layers/zz_ns_transport_routes_calibrated_v16.geojson`
- 交通节点：`layers/zz_ns_transport_nodes_calibrated_v16.geojson`
- 命名山脉/地貌：`layers/zz_ns_named_mountains_calibrated_v16.geojson`
- 谭图线稿升格队列：`layers/zz_tan_linework_promotion_queue_v16.geojson`
- 游戏 zoom 切片清单：`layers/zz_game_zoom_slice_manifest_v16.json`

## 数量
- CHGIS 官方府州面：434
- 府州规划面：639
- 县级规划面：1919
- v13 官方面外点：2780
- v16 已解析缺面点：2780
- v16 剩余缺面点：0
- 北宋命名水系：7
- 驿路/漕运/边防道路：9
- 交通节点：52
- 命名山脉/地貌骨架：16
- 谭图线稿升格队列：230
- z7 主府州点：65
- z8-z9 路州点：84
- z10-z11 县级焦点种子点：9

## DEM 状态
- DEM 不缺，v15 起已接入主地形底图。
- 使用 `layers/zz_travel_friction_z8_seed.png` 和 `layers/zz_dem_z8_hillshade.png` 作为地形底图。
- 源数据：AWS Open Data Terrain Tiles / Mapzen Terrarium z8。
- 覆盖范围：94E-126E、17N-43N。
- 瓦片数：528。

## 权威边界
- `layers/zz_chgis_official_song_prefecture_polygons_v7.geojson` 是本包内的 CHGIS 官方府州面。
- `layers/zz_ns_county_full_planning_surfaces_v15.geojson` 和 `layers/zz_ns_prefecture_full_planning_surfaces_v15.geojson` 是补齐显示用规划面，不是 CHGIS 原始边界。
- v16 的水系、道路、山脉、节点属于历史游戏参考层，已写入来源依据、置信度和升格规则。

## 游戏层级
- z7 全国层：主要府州、主水系、命名山脉，不显示县乡细节。
- z8-z9 路州层：府州、主路线、漕运/边防通道、谭图修边参考。
- z10-z11 县乡层：县级规划面、当前选中区域内县乡点、交通节点。

## 仍需人工升格的部分
- 谭图线稿仍在 `PROMOTION_QUEUE`，不能直接当最终边界。
- 水系与道路已从参考层升到游戏校准层，但黄河决徙、汴河/通济渠、江南运河等仍需要按具体年代继续细校。
- 命名山脉已对齐主要骨架，但山口、岭路、关隘与军事使用还需要后续按区域精修。

## 审查命令
- `node review_all_data.js`
- `node review_sandbox_layers.js`
- `node build_v16_historical_game_layers.js`
