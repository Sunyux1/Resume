# Data Cleaning Project
Use the public datasets and crime research provided by the NSW Government to clean, analyze, and visualize crime data and police station CSV files for the community.
构建一个端到端数据管道，分析来源于 BOCSAR（新南威尔士州犯罪统计与研究局）及新南威尔士州客户服务部的犯罪事件数据，整合警察局位置与邮政编码信息，用来为新南威尔士州警察的资源调配提供地理空间洞察。
Key Contributions
•	Data Wrangling: Ingested and cleaned three heterogeneous datasets (CSV, JSON) using pandas — handling bad rows, asterisk artefacts, type coercion, and duplicate removal without modifying source files.
•	ETL / Data Reshaping: Reshaped a wide-format crime dataset (300+ monthly columns) into a tidy long-format using pd.melt, producing a five-column DataFrame (suburb, category, sub_category, date, crime_count).
•	Geospatial Analysis: Performed coordinate system transformation (EPSG:3857 → WGS84) using GeoPandas and gpd.sjoin_nearest to assign every NSW suburb its nearest police station with correct latitude/longitude.
•	Analytical Reporting: Designed and produced a year-on-year summary pivot table (crime_count + offence_rate per police station per category) for senior police executives — balancing completeness with readability.
•	Data Visualisation: Created three-panel Matplotlib/Seaborn dashboards showing (1) Sydney seasonal crime trends, (2) top-10 crime category breakdown, and (3) Inner vs Outer Sydney crime comparison using postcode-based geographic segmentation.
•	Trend Analysis: Investigated offence growth 2020–2025: identified a 34% overall decline in NSW crime yet flagged specific upward trends (e.g. Transport regulatory offences at Hurstville +36%; justice procedure offences at Belmont) to support targeted policing decisions.
