# Connecticut 2010 and 2020 Census Block to Town Crosswalk

This repository contains crosswalks between CT census blocks (smallest geographical units used by the US Census) and towns in Connecticut for 2010 and 2020 Census. Files are available in CSV and Excel formats.

* The 2010 crosswalk (`2010/block2town-2010.csv`) contains 67,578 blocks.
* The 2020 crosswalk (`2020/block2town-2020.csv`) contains 49,926 blocks.

|block_fips|block_name|town|county|town_fips
|--|--|--|--|--|
|090076802001017|Block 1017|Middletown|Middlesex|0900747360
|090010431002040|Block 2040|Norwalk|Fairfield|0900156060
|090012201001014|Block 1014|New Fairfield|Fairfield|0900150860
|090010431002026|Block 2026|Norwalk|Fairfield|0900156060
|090093511001000|Block 1000|Waterbury|New Haven|0900980070
|090076101001036|Block 1036|Clinton|Middlesex|0900715350


To prevent Excel from transforming FIPS codes to numbers automatically
(which leads to missing leading 0s), do the following:

1. Open Excel, New workbook
1. Go to File > Import > CSV file
1. Choose file, and select "text" as type of block_fips and town_fips columns


### How it was generated
In QGIS, open census block boundaries, calculate their centroids, and perform nearest neighbor spatial join
(NNJoin plugin) to assign the "nearest" town.

### Source datasets
* 2020 TIGER/Line Shapefiles: https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.2020.html

### License
Released under MIT license. Feel free to use for any project. We will appreciate if you credited CTData Collaborative, although this is not required.
