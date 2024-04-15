
## Dataset: BDC_fixed.gpkg

Open with: 
BDC_fixed_gdf = gp.read_file(gitrepo_data_loc + 'BDC_fixed.gpkg')

BDC: Broadband Data Collection conducted by the FCC - Providers report by location their service available at that location. 

Source of Data: https://broadbandmap.fcc.gov/data-download/nationwide-data?version=jun2023 (We are using the March 2024 update)
Data dictionary: https://us-fcc.app.box.com/v/bdc-data-downloads-output

### Three data sets concatenated and columns removed and added to create one data set for fixed internet types:
- EUP_BDC_cable_fixed_jul23mar24.csv
- EUP_BDC_copper_fixed_jul23mar24.csv
- EUP_BDC_fiber_fixed_jul23mar24.csv


Columns in data:

'building_type_code',
'land_use_code',
'provider_id',
'brand_name',
'technology',
'technology_name',
'max_advertised_download_speed',
'max_advertised_upload_speed',
'low_latency',
'business_residential_code',
'up_down_ratio',
'geometry'

## Dataset: EUPOSMgraph.gpkg

Contains the roads extracted using OSMNX for the roads - edges and nodes for the the county area.

Open the edge layer to get the roads.



## Meaning of EUP:

Eastern Upper Pensinsula of Michigan and reflects the geographical boundaries of Chippewa, Mackinac and Luce county which is our model development area.

## ESRI Shapefiles with the polygons for various boundaries in the EUP

- EUPCounties.shp.zip
- EUPPlanning_Region.shp.zip
- EUPTowns.shp.zip