VERPAT contains 34 input files and 5 parameter files, some of which the user must change and others which typically remain unchanged. This page walks the end user through these files and specifies which files must be updated to implement VERPAT in a new region.

# Inputs and Parameters for VERPAT

## Input Files

[**Built Environment**](#built-environment)
  - [bzone_pop_emp_prop.csv](#bzone_pop_emp_propcsv)
  
[**Demand**](#demand)
  - [region_trips_per_cap.csv](#region_trips_per_capcsv)
  - [employment.csv](#employmentcsv)
  - [azone_hh_pop_by_age.csv](#azone_hh_pop_by_agecsv)
  - [azone_per_cap_inc.csv](#azone_per_cap_inccsv)
  - [region_truck_bus_vmt.csv](#region_truck_bus_vmtcsv)
  - [marea_lane_miles.csv](#marea_lane_milescsv)
  - [marea_rev_miles_pc.csv](#marea_rev_miles_pccsv)
  
[**Policy**](#policy)
  - [model_commute_options.csv](#model_commute_optionscsv)
  - [azone_its_prop.csv](#azone_its_propcsv)
  - [model_light_vehicles.csv](#model_light_vehiclescsv)
  - [marea_parking_growth.csv](#marea_parking_growthcsv)
  - 
  - model_tdm_transit.csv
  - model_tdm_transitlevels.csv
  - model_tdm_vanpooling.csv
  - model_tdm_workschedule.csv
  - model_tdm_workschedulelevels.csv
  - region_accident_rates.csv
  - region_fuel_co2.csv
  - region_fuel_composition_prop.csv
  - region_fuel_prop_by_veh.csv
  - region_gt1_veh_prop.csv
  - region_lt1_veh_prop.csv
  - region_place_type_elasticities.csv
  - region_place_type_relative_values.csv
  - region_transportation_costs.csv
  - region_veh_cumprop_by_vehage.csv
  - region_veh_mpg_by_year.csv
  - region_veh_mpg_dvmt_prop.csv
  - region_veh_prop_by_vehage_vehtype_inc.csv
  - azone_gq_pop_by_age.csv
  - azone_hhsize_targets.csv
  - azone_relative_employment.csv
  - marea_parking_growth.
  - 
  - model_tdm_ridesharing.csv

## Input Parameter Files

  - model_parameters.json
  - run_parameters.json
  - units.csv
  - deflators.csv
  - geo.csv

# Input Files to Change

The user should change the input files described here. All files are ```*.csv```.

## Built Environment

### bzone_pop_emp_prop.csv

**Population and Jobs by Place Type**: This file contains the distribution of  population and employment among the 13 place types for base and future year. See [this](https://github.com/gregorbj/VisionEval/wiki/VERPAT-Inputs-and-Outputs#geocsv) explanation for more infomation regarding place types. Each column, for each year, must sum to one (1). It is acceptable to have no land use (i.e. a value of 0) in certain categories.
   The yearly TAZ employment and population totals were summed by the 13 place type and then scaled to total one for both employment and population.
   Here is a snapshot of the file:

   | Geo   | Year | Pop  | Emp  |
   | ----- | ---- | ---- | ---- |
   | Rur   | 2005 | 0.05 | 0.1  |
   | Sub_R | 2005 | 0.3  | 0    |
   | Sub_E | 2005 | 0    | 0.2  |
   | Sub_M | 2005 | 0.1  | 0.1  |
   | Sub_T | 2005 | 0    | 0    |
   | CIC_R | 2005 | 0.15 | 0    |
   | CIC_E | 2005 | 0    | 0.2  |
   | CIC_M | 2005 | 0.1  | 0.1  |
   | CIC_T | 2005 | 0    | 0    |
   | UC_R  | 2005 | 0.1  | 0    |
   | UC_E  | 2005 | 0    | 0.1  |
   | UC_M  | 2005 | 0.1  | 0.1  |
   | UC_T  | 2005 | 0.1  | 0.1  |
   | Rur   | 2035 | 0.05 | 0.1  |
   | Sub_R | 2035 | 0.3  | 0    |
   | Sub_E | 2035 | 0    | 0.2  |
   | Sub_M | 2035 | 0.1  | 0.1  |
   | Sub_T | 2035 | 0    | 0    |
   | CIC_R | 2035 | 0.15 | 0    |
   | CIC_E | 2035 | 0    | 0.2  |
   | CIC_M | 2035 | 0.1  | 0.1  |
   | CIC_T | 2035 | 0    | 0    |
   | UC_R  | 2035 | 0.1  | 0    |
   | UC_E  | 2035 | 0    | 0.1  |
   | UC_M  | 2035 | 0.1  | 0.1  |
   | UC_T  | 2035 | 0.1  | 0.1  |

[Top](#input-files)

## Demand

### region_trips_per_cap.csv
**Auto and transit trips per capita**: This file contains regional averages for auto and transit trips per capita per day for the base year.

   - **Auto** is the regional average of auto trips per capita, including drive alone and shared ride travel. This data can be derived from the [National Household Travel Survey](https://nhts.ornl.gov/) by region or from a local household travel survey or regional travel demand forecasting model.
   - **Transit** is the regional average of transit trips per capita, including walk and drive access to transit. This data can be derived from the [National Transit Database](https://www.transit.dot.gov/ntd/ntd-data) where the annual database contains a “service” table that has annual transit trip data for each transit operator or from a local household travel survey or regional travel demand forecasting model.

   Here is a snapshot of the files:

   | Mode    | Trips |
   | ------- | ----- |
   | Auto    | 3.2   |
   | Transit | 0.4   |

[Top](#input-files)


### employment.csv

**Employment**: This file contains employment data for each of the counties that make up the region. The file is derived from County Business Pattern ([CBP](http://www.census.gov/econ/cbp/)) data by county. Industries are categorized by the North American Industrial Classification System (NAICS) 6 digit codes. Firm size categories are:

   - **n1_4**: 1- 4 employees
   - **n5_9**: 5-9 employees
   - **n10_19**: 10-19 employees
   - **n20_99**: 20-99 employees
   - **n100_249**: 100-249 employees
   - **n250_499**: 250-499 employees
   - **n500_999**: 500-999 employees
   - **n1000**: 1,000 or More Employee Size Class
   - **n1000_1**: 1,000-1,499 employees
   - **n1000_2**: 1,500-2,499 employees
   - **n1000_3**: 2,500 to 4, 999 Employees
   - **n1000_4**: Over 5,000 employees

   While the county field is required to be present, the business synthesis process does not require a meaningful value and therefore users may simply enter “region”. The consistency in the naming of the "region" should be maintained across all the files that contains the label *"county"* or *"Geo"*. It is also not necessary to use such detailed NAICS categories if those are not available; the current business synthesis model and subsequent models do not use this level of detail (although future versions of the model may) – at minimum, the number of establishments for all employment types can be provided by size category. Regions with significant employment in industries such as government and public administration that are not covered by the CBP may need to add records to the file that cover this type of employment to more accurately match employment totals in their region. The two additional fields contained in the file are:

   - **emp**: Total number of employees
   - **est**: Total number of establishments

   Here is the snapshot of the file:

   | county    | year | naics  | emp  | est  | n1_4 | n5_9 | n10_19 | n20_49 | n50_99 | n100_249 | n250_499 | n500_999 | n1000 | n1000_1 | n1000_2 | n1000_3 | n1000_4 |
   | --------- | ---- | ------ | ---- | ---- | ---- | ---- | ------ | ------ | ------ | -------- | -------- | -------- | ----- | ------- | ------- | ------- | ------- |
   | Multnomah | 2005 | 113110 | 0    | 5    | 2    | 1    | 0      | 2      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 113310 | 0    | 3    | 2    | 0    | 0      | 1      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 114111 | 0    | 1    | 0    | 1    | 0      | 0      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 114112 | 0    | 1    | 1    | 0    | 0      | 0      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 115114 | 0    | 1    | 0    | 0    | 0      | 0      | 0      | 0        | 1        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 115210 | 0    | 4    | 3    | 1    | 0      | 0      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 115310 | 0    | 5    | 2    | 0    | 1      | 1      | 1      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 212319 | 0    | 1    | 1    | 0    | 0      | 0      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |
   | Multnomah | 2005 | 212321 | 0    | 4    | 1    | 1    | 1      | 1      | 0      | 0        | 0        | 0        | 0     | 0       | 0       | 0       | 0       |

[Top](#input-files)

### azone_hh_pop_by_age.csv

**Household population**: This file contains population estimates/forecasts by county and age cohort for each of the base and future years. The file format includes six age categories used by the population synthesis model:

   - **0-14**
   - **15-19**
   - **20-29**
   - **30-54**
   - **55-64**
   - **65 Plus**

   Future year data must be developed by the user; in many regions population forecasts are available from regional or state agencies and/or local academic sources. As with the employment data inputs the future data need not be county specific. Rather, regional totals by age group can be entered into the file with a value such as “region” entered in the county field.

   Here is a snapshot of the file:

   | Geo       | Year | Age0to14 | Age15to19 | Age20to29 | Age30to54 | Age55to64 | Age65Plus |
   | --------- | ---- | -------- | --------- | --------- | --------- | --------- | --------- |
   | Multnomah | 2005 | 129869   | 41133     | 99664     | 277854    | 71658     | 72648     |
   | Multnomah | 2035 | 169200   | 48800     | 144050    | 327750    | 116100    | 162800    |

[Top](#input-files)

###azone_per_cap_inc.csv

**Regional income**: This file contains information on regional average per capita  household and group quarters income by forecast year in year 2000 dollars. The data can be obtained from the U.S. Department of [Commerce Bureau of Economic Analysis](http://www.bea.gov/regional/index.htm) for the current year or from regional or state sources for forecast years. In order to use current year dollars just replace ***2000*** in column labels with current year. For example, if the data is obtained in year 2005 dollars then the column labels in the file shown below will become **HHIncomePC.2005** and **GQIncomePC.2005**.
   Here is a snapshot of the file:

   | Geo       | Year | HHIncomePC.2000 | GQIncomePC.2000 |
   | --------- | ---- | --------------- | --------------- |
   | Multnomah | 2005 | 32515           | 0               |
   | Multnomah | 2035 | 40000           | 0               |

[Top](#input-files)

### region_truck_bus_vmt.csv

**Truck and bus vmt**: This file contains the region’s proportion of VMT by truck and bus as well as the distribution of that VMT across functional classes (*freeway*, *arterial*, *other*). The file includes one row for bus VMT data and one row for Truck VMT data. It should be noted that it is not necessary to enter values in the **PropVmt** column for **BusVmt** as this is calculated using the values in the ***transportation_supply.csv*** #EDIT (marea_rev_miles_pc.csv?) user input file. The truck VMT proportion (PropVMT column, TruckVMT row) can be obtained from [Highway Performance Monitoring System](http://www.fhwa.dot.gov/policyinformation/hpms.cfm) data and local sources or the regional travel demand model if one exists.
   The proportions of VMT by functional class can be derived from the Federal Highway Cost Allocation Study and data from transit operators. The Federal Highway Cost Allocation Study (Table II-6, 1997 Federal Highway Cost Allocation Study Final Report, [Chapter II](http://www.fhwa.dot.gov/policy/hcas/final/two.cfm) is used to calculate the average proportion of truck VMT by functional class. Data from transit authorities are used to calculate the proportions of bus VMT by urban area functional class.
   Here is a snapshot of the file:

   | Type     | PropVmt | Fwy      | Art      | Other    |
   | -------- | ------- | -------- | -------- | -------- |
   | BusVmt   | 0       | 0.15     | 0.591854 | 0.258146 |
   | TruckVmt | 0.08    | 0.452028 | 0.398645 | 0.149327 |

[Top](#input-files)

### marea_lane_miles.csv

**Road lane miles**: This file contains the amount of transportation supply by base year in terms of lane miles of freeways and arterial roadways in the region. The base year data is duplicated for future year.
   **Freeway** and **Arterial** are total lane miles for those functional classes in the region. These data can be derived from the Federal Highway Administration’s (FHWA) Highway [Statistics data](http://www.fhwa.dot.gov/policy/ohim/hs05/roadway_extent.cfm).
   Here is a snapshot of the file:

   | Geo       | Year | FwyLaneMi | ArtLaneMi |
   | --------- | ---- | --------- | --------- |
   | Multnomah | 2005 | 250       | 900       |
   | Multnomah | 2035 | 250       | 900       |

[Top](#input-files)

### marea_rev_miles_pc.csv

**Transit revenue miles**: This file contains the amount of transportation supply by base year in terms of the revenue miles operating by the transit system in the region. The base year data is duplicated for future year.
   **Bus** and **Rail** are annual bus and rail revenue miles per capita for the region. These data can be derived from the [National Transit Database](https://www.transit.dot.gov/ntd/ntd-data), where the annual database contains a “service” table that has annual revenue mile data by mode for each transit operator.
   Here is a snapshot of the file:

   | Geo       | Year | BusRevMiPC | RailRevMiPC |
   | --------- | ---- | ---------- | ----------- |
   | Multnomah | 2005 | 19         | 4           |
   | Multnomah | 2035 | 19         | 4           |

[Top](#input-files)


## Policy


### model_commute_options.csv

**Percentage of employees offered commute options**: This file contains assumptions about the availability and participation in work based travel demand management programs. The policies are ridesharing programs, transit pass programs, telecommuting or alternative work schedule programs, and vanpool programs. For each, the user enters the proportion of workers who participate (the data items with the “Participation” suffix). For one program, the transit subsidy, the user must also enter the subsidy level in dollars for the TransitSubsidyLevel data item.
   Here is a snapshot of the file:

   | TDMProgram     | DataItem                        | DataValue |
   | -------------- | ------------------------------- | --------- |
   | Ridesharing    | RidesharingParticipation        | 0.05      |
   | TransitSubsidy | TransitSubsidyParticipation     | 0.1       |
   | TransitSubsidy | TransitSubsidyLevel             | 1.25      |
   | WorkSchedule   | Schedule980Participation        | 0.01      |
   | WorkSchedule   | Schedule440Participation        | 0.01      |
   | WorkSchedule   | Telecommute1.5DaysParticipation | 0.01      |
   | Vanpooling     | LowLevelParticipation           | 0.04      |
   | Vanpooling     | MediumLevelParticipation        | 0.01      |
   | Vanpooling     | HighLevelParticipation          | 0.01      |

[Top](#input-files)

### azone_its_prop.csv

**Percent road miles with ITS treatment**: This file is an estimate of the proportion of road miles that have improvements which reduce incidents through ITS treatments in both the base and future years. Values entered should be between 0 and 1, with 1 indicating that 100% of road miles are treated.
   The ITS policy measures the effects of incident management supported by ITS. The ITS table is used to inform the congestion model and the travel demand model. The model uses the mean speeds with and without incidents to compute an overall average speed by road type and congestion level providing a simple level of sensitivity to the potential effects of incident management programs on delay and emissions.
   The ITS treatments are evaluated only on freeways and arterials. The ITS treatments that can be evaluated are those that the analyst considers will reduce non-recurring congestion due to incidents. This policy does not deal with other operational improvements such as signal coordination, or temporary capacity increases such as allowing shoulder use in the peak.
   Here is a snapshot of the file:

   | Geo       | Year | ITS  |
   | --------- | ---- | ---- |
   | Multnomah | 2005 | 0    |
   | Multnomah | 2035 | 0    |
   
[Top](#input-files)


### model_light_vehicles.csv

**Bicycling/light vehicles targets)**: This file contains input data for the non-motorized vehicle model. In VERPAT, non-motorized vehicles are bicycles, and also electric bicycles, segways, and similar vehicles that are small, light-weight and can travel at bicycle speeds or slightly higher. The parameters are as follows:

   - **TargetProp**: non-motorized vehicle ownership rate (average ratio of non-motorized vehicles to driver age population)
   - **Threshold**: single-occupant vehicle (SOV) tour mileage threshold used in the SOV travel proportion model. This is the upper limit for tour lengths that are suitable for reallocation to non-motorized modes.
   - **PropSuitable**: proportion of SOV travel suitable for non-motorized vehicle travel. This variable describes the proportion of SOV tours within the mileage threshold for which non-motorized vehicles might be substituted. This variable takes into account such factors as weather and trip purpose.

   The non-motorized vehicle model predicts the ownership and use of non-motorized vehicles (where non-motorized vehicles are bicycles, and also electric bicycles, segways and similar vehicles that are small, light-weight and can travel at bicycle speeds or slightly higher than bicycle speeds). The core concept of the model is that non-motorized vehicle usage will primarily be a substitute for short-distance SOV travel. Therefore, the model estimates the proportion of the household vehicle travel that occurs in short-distance SOV tours. The model determines the maximum potential for household VMT to be diverted to non-motorized vehicles, which is also dependent on the availability of non-motorized vehicles.
   Note that bike share programs (BSP) serve to increase the availability of non-motorized vehicles and can be taken into account by increasing the **TargetProp** variable. Use national estimates of non-motorized ownership if regional estimates of non-motorized ownership are not available (unless the region has notably atypical levels of bicycle usage). See [Bicycle Ownership in the United States](http://www.academia.edu/1839374/Bicycle_Ownership_in_the_United_States_Empirical_Analysis_of_Regional_Differences) for an analysis of regional differences.
   Here is a snapshot of the file:

   | DataItem     | DataValue |
   | ------------ | --------- |
   | TargetProp   | 0.2       |
   | Threshold    | 2         |
   | PropSuitable | 0.1       |
   
[Top](#input-files)

### marea_parking_growth.csv

**Increase in parking cost and supply**: This file contains information that allows the effects of policies such as workplace parking charges and "*cash-out buy-back*" programs to be tested. The input parameters are as follows and should be entered for both the base and future year:

   - **PropWrkPkg**: proportion of employees that park at work
   - **PropWrkChrgd**: proportion of employers that charge for parking
   - **PropCashOut**: proportion of employment parking that is converted from being free to pay under a "*cash-out buy-back*" type of program
   - **PrkOthChrgd**: proportion of other parking that is not free
   - **PkgCost**: average daily parking cost. This variable is the average daily parking cost for those who incur a fee to park. If the paid parking varies across the region, then the "*PkgCost*" value should reflect the average of those parking fees, but weighted by the supply – so if most parking is in the Center City, then the average will be heavily weighted toward the price in the Center City.

   Here is a snapshot of the file:

   | Geo       | Year | PropWorkParking | PropWorkCharged | PropCashOut | PropOtherCharged | ParkingCost.2000 |
   | --------- | ---- | --------------- | --------------- | ----------- | ---------------- | ---------------- |
   | Multnomah | 2005 | 1               | 0.1             | 0           | 0.05             | 5                |
   | Multnomah | 2035 | 1               | 0.1             | 0           | 0.05             | 5                |
   
[Top](#input-files)