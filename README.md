# Data Cleaning Project
Use the public datasets and crime research provided by the NSW Government to clean, analyze, and visualize crime data and police station CSV files for the community.

利用新南威尔士州政府提供的公共数据集及犯罪研究资料，对犯罪数据与警察局 CSV 文件进行清洗、分析与可视化，为社区提供数据支持。

构建一个端到端数据管道，分析来源于 BOCSAR（新南威尔士州犯罪统计与研究局）及新南威尔士州客户服务部的犯罪事件数据，整合警察局位置与邮政编码信息，用来为新南威尔士州警察的资源调配提供地理空间洞察。

Key Contributions

•	Data Wrangling: Ingested and cleaned three heterogeneous datasets (CSV, JSON) using pandas — handling bad rows, asterisk artefacts, type coercion, and duplicate removal without modifying source files.

•	ETL / Data Reshaping: Reshaped a wide-format crime dataset (300+ monthly columns) into a tidy long-format using pd.melt, producing a five-column DataFrame (suburb, category, sub_category, date, crime_count).

•	Geospatial Analysis: Performed coordinate system transformation (EPSG:3857 → WGS84) using GeoPandas and gpd.sjoin_nearest to assign every NSW suburb its nearest police station with correct latitude/longitude.

•	Analytical Reporting: Designed and produced a year-on-year summary pivot table (crime_count + offence_rate per police station per category) for senior police executives — balancing completeness with readability.

•	Data Visualisation: Created three-panel Matplotlib/Seaborn dashboards showing (1) Sydney seasonal crime trends, (2) top-10 crime category breakdown, and (3) Inner vs Outer Sydney crime comparison using postcode-based geographic segmentation.

•	Trend Analysis: Investigated offence growth 2020–2025: identified a 34% overall decline in NSW crime yet flagged specific upward trends (e.g. Transport regulatory offences at Hurstville +36%; justice procedure offences at Belmont) to support targeted policing decisions.

数据整理： 

使用 pandas 读取并清洗三个异构数据集（CSV、JSON）——处理坏行、星号字符、类型转换及重复值，全程不修改源文件。

ETL / 数据重塑： 使用 pd.melt 将宽格式犯罪数据集（300+ 个月份列）转换为整洁的长格式，生成包含五列的 DataFrame（suburb、category、sub_category、date、crime_count）。

地理空间分析： 使用 GeoPandas 和 gpd.sjoin_nearest 完成坐标系转换（EPSG:3857 → WGS84），为新南威尔士州每个郊区匹配最近的警察局及其正确的经纬度坐标。

分析报告： 为警察高层管理人员设计并生成年度对比汇总数据透视表（按警察局和犯罪类别统计 crime_count 与 offence_rate），在数据完整性与可读性之间取得平衡。

数据可视化： 使用 Matplotlib/Seaborn 创建三图面板仪表板，分别展示：(1) 悉尼全年犯罪季节性趋势，(2) 前十大犯罪类别分布，(3) 基于邮政编码地理分区的悉尼内城与外城犯罪对比。

趋势分析： 调查 2020–2025 年犯罪增长情况：发现新南威尔士州整体犯罪下降 34%，同时标记出特定上升趋势（如 Hurstville 的交通违规类犯罪上升 36%、Belmont 的妨碍司法类犯罪上升），为精准警务决策提供数据支撑。
