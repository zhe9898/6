# v16 拆分主图层 + 美术数据参考

这里是从完整包 `northern_song_filled.zip` 拆出的主成果文件，方便 GitHub、Gemini、GPT、Kimi 或人工直接浏览。

## 当前说明

全国大图的美术主目标在：

- `../ai_art_brief/STYLE_TARGET.md`

本目录里的 PNG / GeoJSON 是数据参考，不是最终画风。全国层不要做成 2.5D DEM 浮雕图。

## 关键图层

- `layers/zz_ns_game_layers_reference_map_v16.png`：综合参考图，不要照搬成全国美术图。
- `layers/zz_ns_full_admin_planning_map_v15.png`：行政规划补面图，用于理解数据缺面，不是全国层美术方向。
- `layers/zz_chgis_official_song_prefecture_polygons_v7.geojson`：CHGIS 官方北宋府州面。
- `layers/zz_ns_county_full_planning_surfaces_v15.geojson`：县级规划面，只用于局部沙盘和数据诊断。
- `layers/zz_ns_prefecture_full_planning_surfaces_v15.geojson`：府州级规划面，只作辅助。
- `layers/zz_ns_admin_gap_points_resolved_v16.geojson`：缺面点的补入结果。
- `layers/zz_ns_admin_gap_worklist_v16.geojson`：剩余缺面清单。
- `layers/zz_ne_50m_land_clipped_v21.geojson`：海陆硬分参考。
- `layers/zz_ne_50m_coastline_clipped_v21.geojson`：海岸线参考。
- `layers/zz_ns_hydro_calibrated_v16.geojson`：水系参考层。
- `layers/zz_ns_transport_routes_calibrated_v16.geojson`：道路 / 漕运 / 边防路线。
- `layers/zz_ns_transport_nodes_calibrated_v16.geojson`：交通和战略节点。
- `layers/zz_ns_named_mountains_calibrated_v16.geojson`：命名山脉 / 地貌骨架。
- `layers/zz_tan_linework_promotion_queue_v16.geojson`：谭图线稿升格队列。
- `layers/zz_game_zoom_slice_manifest_v16.json`：游戏 zoom 层切片规则。

## 使用规则

- 全国层：看 `STYLE_TARGET.md`，不铺行政面，不显示县界，不做 DEM 浮雕。
- 区域层：进入 2.5D 沙盘，水系、道路、漕运、边防、关隘成为主体。
- 局部层：县界硬边、县乡点、城池、军寨、渡口、驿站和市场才进入操作沙盘。

完整大包仍在 Release：

https://github.com/zhe9898/6/releases/tag/northern-song-v16
