# Metadata

## Capacity by Fuel Type

| | | 
|:-|:-|
| Filename |  |
| Original Source | The original data was collected from _____ from the yearly Alaska energy stats workbooks hosted at: https://github.com/acep-uaf/ak-energy-statistics-2011_2021/tree/main/workbooks |
| Time Horizon | Calendar Years, 2011 through 2021 |
| General Notes ||

### Data Dictionary


## Plant-Level Net Generation by Fuel Type

| | | 
|:-|:-|
| Filename | `net-generation-by-fuel-type.csv` |
| Original Source | The original data was collected from Table 2.3b from the yearly Alaska energy stats workbooks hosted at: https://github.com/acep-uaf/ak-energy-statistics-2011_2021/tree/main/workbooks |
| Time Horizon | Calendar Years, 2011 through 2021 |
| General Notes | Not every workbook had the same column organization. Data years 2012 and 2013 did not include AEA Energy Regions, so the user will need to map the AEA Regions to the plant name using other years as the key (an example of this can be found in `../net-generation.ipynb`). 2013 was the first year to include the "other" fuel type category. 2014 was the first year to include solar and storage data. I collected this data in this format because it is the most updated version of the data. In particular, other versions of the notebooks do not include manual entries for solar data.|

### Data Dictionary

|  |  | 
|:-|:-|
| `year`              | Year of the source data. Indicates the workbook that it was derived from as well 
| `plant_name`       | The name of the generator.                                                                                                                                                        |
| `oil`               | Generation from Diesel/Distillate (EIA type DFO), Naphtha (EIA type WO), and Jet fuel (EIA type JF)                                                                                         |
| `gas`               | Generation from Natural Gas (EIA fuel type NG) and Landfill gas (EIA type LFG)                                                                                                              |
| `coal`              | Generation from Subbituminous Coal (EIA type SUB), Lignite (EIA type LIG), Waste Coal (EIA type WC)                                                                                         |
| `hydro`             | Generation from  water at a conventional hydroelectric turbine (EIA type WAT)                                                                                                               |
| `wind`              | Generation from Wind (EIA type WND)                                                                                                                                                         |
| `solar`     | Generation from Solar energy (EIA type SUN). Excludes customer-sited (="behind-the-meter" or BTM) solar.                                                                                    |
| `storage`     | Generation by batteries (EIA type BA) and flywheels (EIA type FW). The amount typically shows as negative, reflecting more energy injected while charging than withdrawn while discharging. |
| `other`             | No idea.                                                                                                                                                                                    |
| `source` | Can be EIA923, PCE, AEA, or missing. Missing values are common when a plant reports no generation for that year. |
| `data_version` | Either final or early release. |
| `aea_energy_region` | AEA designated energy region (11 possible). 2012 and 2013 did not have this data and needs to be downfilled. |