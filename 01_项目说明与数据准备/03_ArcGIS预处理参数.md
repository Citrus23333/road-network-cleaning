# ArcGIS Pro 基础预处理

## 1. JSON转要素

使用 ArcGIS Pro 将原始 JSON 数据转换为线要素，并检查坐标系和几何类型。

## 2. Integrate

- XY Tolerance：0.5 m
- 目的：处理局部微小错位、近邻顶点和轻微相交偏差
- 限制：不用于修复数米以上道路缺口

## 3. Dissolve

- 不勾选 Create multipart features
- 目的：合并可连续表达的线要素，同时尽量维持单部件线结构

## 4. 投影与导出

- 目标坐标系：EPSG:4547
- 最终转换为 GeoParquet，供 Python 读取
