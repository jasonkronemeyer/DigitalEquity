
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

'provider_id', integer - Unique identifier for the fixed service provider.

'brand_name', string Acme - Name of the entity or service advertised or offered to
consumers.

'technology', integer - Code for the technology used for the deployed service.

- Value is one of the following codes:
- 10 – Copper Wire
- 40 – Coaxial Cable / HFC
- 50 – Optical Carrier / Fiber to the Premises
- 60 – Geostationary Satellite
- 61 – Non-geostationary Satellite
- 70 – Unlicensed Terrestrial Fixed Wireless
- 71 – Licensed Terrestrial Fixed Wireless
- 72 – Licensed-by-Rule Terrestrial Fixed Wireless
- 0 – Other

'technology_name',

'max_advertised_download_speed', Integer - Maximum advertised download speed offered at the location in Mbps

'max_advertised_upload_speed', Integer - Maximum advertised upload speed associated with the maximum advertised download speed offered at the location in Mbps.

'low_latency', boolean integer - Boolean integer flag indicating whether or not the offered service is low latency, defined as having round-trip latency of less than or equal to 100 ms based on the 95th percentile of measurements.

- Value is one of the following codes:
- 0 – False
- 1 – True

'business_residential_code', Enumerated String - Enumerated character identifying whether the service at the location is offered only to business customers, only to residential customers, or to both business and residential customers.

- Value is one of the following codes:
- B – Business-only location
- R – Residential-only location
- X – Business and Residential location

'up_down_ratio', float, calculated at upload / download

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

## Netstats from OOKLA

- MI_Netstats.gpkg - This file contains the OOKLA speedtest public data for 2023 Q3, 2023 Q4, and 2024 Q1 for the whole state of michigan. There is a notebook in the practice folder based on a tutorial used from OOKLA git-hub.