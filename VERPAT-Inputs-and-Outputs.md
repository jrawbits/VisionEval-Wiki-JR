# Contents
This page describes the VERPAT inputs (including definitions) and outputs by module.
  - [Definitions](#definitions)
  - [Inputs and Outputs](#inputs-and-outputs)

# Definitions
The following five files need to be configured in the "defs" directory:
  - [run_parameters.json](#run_parametersjson)
  - [model_parameters.json](#model_parametersjson)
  - [deflators.csv](#deflatorscsv)
  - [geo.csv](#geocsv)
  - [units.csv](#unitscsv)

## run_parameters.json

The "run_parameters.json" file contains parameters that define key attributes of the model run and relationships to other model runs. A more detailed description of the file can be found [here](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#61-model-directory-structure). The format of the VERPAT *run_parameters.json* file is as follows:

```json
{
    "Model": ["RPAT"],
    "Scenario": ["RPAT Pilot"],
    "Description": ["Pilot RPAT module in VisionEval"],
    "Region": ["Multnomah County Oregon"],
    "BaseYear": ["2005"],
    "Years": ["2005", "2035"],
    "DatastoreName": ["Datastore"],
    "DatastoreType": ["RD"],
    "Seed": [1],
    "RunTypes": ["E", "ELESNP"]
}
```

[Top](#contents)

## model_parameters.json

The "model_parameters.json" can contain global parameters for a particular model configuration that may be used by multiple modules. A more detailed description of the file and its structure can be found [here](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#61-model-directory-structure). The description about the variables, required for **VERPAT**, listed in the file are documented by the modules that uses them in the [inputs](#inputs) section. The format of the VERPAT *model_parameters.json* file is as follows:

```json
[
  {"NAME": "EmploymentGrowth",
   "VALUE": "1.5",
   "TYPE": "double",
   "UNITS": "multiplier",
   "PROHIBIT": "",
   "ISELEMENTOF": ""},
  {
    "NAME": "FwyLaneMiGrowth",
    "VALUE": "1",
    "TYPE" : "double",
    "UNITS" : "multiplier",
    "PROHIBIT" : "c('NA', '< 0')",
    "ISELEMENTOF" : ""
  },
  {
    "NAME" : "ArtLaneMiGrowth",
    "VALUE": "1",
    "TYPE" : "double",
    "UNITS" : "multiplier",
    "PROHIBIT" : "c('NA', '< 0')",
    "ISELEMENTOF" : ""
  },
  .
  .
  .
  {
    "NAME" : "AutoCostGrowth",
    "VALUE": "1.5",
    "TYPE" : "double",
    "UNITS" : "multiplier",
    "PROHIBIT" : "c('NA', '< 0')",
    "ISELEMENTOF" : ""
  }
]
```

[Top](#contents)

## deflators.csv
The **deflators.csv** file defines the annual deflator values, such as the consumer price index, that are used to convert currency values between different years for currency denomination. The format of the file is as follows:

|              Year              |  Value   |
| :----------------------------: | :------: |
|              1999              |  172.6   |
|              2000              |   178    |
|              2001              |  182.4   |
| ![](./VERPAT_images/vdots.gif) | ![](./VERPAT_images/vdots.gif) |

[Top](#contents)

## geo.csv

The "geography.csv" file describes all of the geographic relationships for the model and the names of geographic entities in a [CSV-formatted](https://en.wikipedia.org/wiki/Comma-separated_values) text file. The format of the file is as follows:

| [Azone](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#62-model-geography) | [Bzone](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#62-model-geography) | [Czone](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#62-model-geography) | [Marea](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#62-model-geography) |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|                          Multnomah                           |                             Rur                              |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            Sub_R                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            Sub_E                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            Sub_M                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            Sub_T                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            CIC_R                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            CIC_E                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            CIC_M                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                            CIC_T                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                             UC_R                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                             UC_E                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                             UC_M                             |                              NA                              |                          Multnomah                           |
|                          Multnomah                           |                             UC_T                             |                              NA                              |                          Multnomah                           |

The geography is described by 13 place types as shown below. One emerging school of thought in land use planning is to consider land uses in terms of place types instead of simply residential or commercial or high density compared to low density. A place type refers to all of the characteristics of a developed area including the types of uses included, the mix of uses, the density and intensity of uses.

|                                  | URBAN <br />CORE | CLOSE-IN <br />COMMUNITY |   SUBURBAN   |    RURAL     |
| :------------------------------- | :--------------: | :----------------------: | :----------: | :----------: |
| **Residential**                  |   ![](./VERPAT_images/checkmark.gif)   |       ![](./VERPAT_images/checkmark.gif)       | ![](./VERPAT_images/checkmark.gif) |              |
| **Commercial**                   |   ![](./VERPAT_images/checkmark.gif)   |       ![](./VERPAT_images/checkmark.gif)       | ![](./VERPAT_images/checkmark.gif) |              |
| **Mixed-Use**                    |   ![](./VERPAT_images/checkmark.gif)   |       ![](./VERPAT_images/checkmark.gif)       | ![](./VERPAT_images/checkmark.gif) |              |
| **Transit-Oriented Development** |   ![](./VERPAT_images/checkmark.gif)   |       ![](./VERPAT_images/checkmark.gif)       | ![](./VERPAT_images/checkmark.gif) |              |
| **Rural/Greenfield**             |                  |                          |              | ![](./VERPAT_images/checkmark.gif) |

An initial typology or system to organize place types can be traced to the Smart Growth Transect, which contained six zones in its original configuration including:

- Rural Preserve
- Rural Reserve
- Edge
- General
- Center
- Core

This approach to classifying place types was further refined in the Caltrans Smart Mobility which defined the following seven place types including:

- Urban Centers
- Close-In Compact Communities
- Compact Communities
- Suburban Communities
- Rural and Agricultural Lands
- Protected Lands
- Special Use Areas

Several of these place type categories provided additional options such as the Close-In Compact Communities which had three sub-definitions including Close-In-Centers, Close-In Corridors, and Close-In Neighborhoods.

An alternative view of place types was provided by Reconnecting America, which developed a performance based place type approach for describing areas proximate to transit stations. Station areas would vary in terms of their relative focus between residential units, employees or a mix of the two. Station areas are also characterized on their relative intensity as well as shown below.

![PERFORMANCE BASED TYPOLOGY FOR TRANSIT STATION AREAS](./VERPAT_images/performancebasedtypology.png)

The approach employed for the place types in RPAT is therefore an amalgam of these approaches, in that the terminology is borrowed from the Smart Growth Transect and Caltrans Smart Mobility Study, while the relative performance of each place type is taken from the Reconnecting America approach but applied to a region instead of transit station sites.

Four general area types are defined in RPAT including:

- The **Urban Core** is the high-density mixed-use places with high jobs-housing ratios, well connected streets and high levels of pedestrian activities. It is anticipated that for many regions, the Urban Core will be the traditional downtown area of which there likely would be only one.
- The **Close-in Community** would be those areas located near to the Urban Cores and would consist primarily of housing with scattered mixed-use centers and arterial corridors. Housing would be varied in terms of density and type. Transit would be available with a primary focus on commute trips. These areas may be classified by their residents as suburban would be considered to be close-in communities given their adjacency to the Downtown and therefore the higher levels of regional accessibility.
- The **Suburban** place type is anticipated to represent the majority of development within regions. These communities are characterized by low level of integration of housing with jobs, retail, and services, poorly connected street networks, low levels of transit service, large amounts of surface parking, and limited walk ability.
- The **Rural** place type is defined as settlements of widely spaced towns separated by firms, vineyards, orchards, or grazing lands. These areas would be characterized by widely dispersed residential uses, little or no transit service, and very limited pedestrian facilities.

Further definition of the place types is allowed through the use of development types within the Urban Core, Close-in Community, and Suburban area types including:

- **Residential** includes all place types that are predominantly residential in character with limited employment and retail opportunities. Examples of this development type might include typical Suburban Residential or areas of the Downtown which are primarily residential as well. It is anticipated that this development type may be found in all of the area types except for rural.
- **Employment** includes those areas which are focused on employment with limited retail and residential. An example of this might include a Suburban Office Complex or a large cluster of office buildings within a Close-in Community or Urban Core. As with the residential development type, it is anticipated that this type of use would be found in all place types except for rural.
- **Mixed-Use** are those areas within a region which have a mix of residential, employment, and retail uses. While this development type can be found in the Suburban place type, it is most commonly found in the close-in community and urban core place type. Downtown areas that have retained their residential population to complement the employment are examples of this development type.
- **Transit-Oriented Development (TOD)** which is similar to the other development types in that it is applied to all area types except for Rural areas since it is thought to be highly unlikely that a rural TOD would be developed. The TOD development type is characterized by greater access to transit in all area types. Examples of this development type might include a Suburban TOD focused on a commuter rail station.

The process of allocating existing land use to the 13 place types is somewhat dependent on the types of data available in a region that describe existing land use, and the process can be either very detailed or somewhat simplified. The following description relays the process developed by Atlanta Regional Commission (ARC) as part of the pilot testing of RPAT and provides an example of how, mechanically, an agency can approach this allocation. It should be noted that this is merely one approach and not a specific recommendation for a method that should be followed.

In general, ARC followed a somewhat detailed process to derive input data from land use data as presented in their “Unified Growth Policy Map”, and from their regional travel demand model. They developed heuristics to align their land use with the 13 place types that RPAT uses.

The conversion of land use data to the place type scheme used in RPAT involved taking ARC’s Unified Growth Policy Map (UGPM) Areas and converting them to the 13 RPAT place types.

1. The first step was to allocate the UGPM areas to the four area types used in RPAT. The Urban Core area type includes Region Core, Region Employment Centers and Aerotropolis UGPM areas; Close-in Community includes Maturing Neighborhoods; Suburban includes Developing Suburbs and Established Suburbs; and Rural includes Rural Areas and Developing Rural.
2. The ARC traffic analysis zone (TAZ) system was overlaid with the area types and the centroid of the TAZ was used to determine its area type.
3. The RPAT development type, the other dimension of the place type matrix, which included residential, mixed-use, employment, and TOD development types was determined for each TAZ not in the rural area type using the base year percentage of the TAZ’s employment in relation to the total of the population and employment in the TAZ. The mix between the employment and employment was used to determine the TAZs development type using the following cut points:
   - Residential: < 33.33% 
   - Mixed Use: 33.33% to 66.67%
   - Employment: > 66.67%
4. Identify any TAZs that are TOD based on transit service and specific development types: only one TAZ was determined to be TOD as a development type, Lindbergh Center, in the Urban Core area type.
5. The combination of the area type and the development type was then used to allocate all TAZs to one of the 13 place types.

The following is an enumeration of each place type abbreviation as it appears in the input file as well as a brief description of that value:

| Abbreviation | Description                                     |
| ------------ | ----------------------------------------------- |
| Rur          | Rural                                           |
| Sub_R        | Suburban Residential                            |
| Sub_E        | Suburban Employment (i.e. Commercial)           |
| Sub_M        | Suburban Mixed Use                              |
| Sub_T        | Suburban Transit Oriented Development           |
| CIC_R        | Close-in Community Residential                  |
| CIC_E        | Close-in Community Employment (i.e. Commercial) |
| CIC_M        | Close-in Community Mixed Use                    |
| CIC_T        | Close-in Community Transit Oriented Development |
| UC_R         | Urban Core Residential                          |
| UC_E         | Urban Core Employment (i.e. Commercial)         |
| UC_M         | Urban Core Mixed Use                            |
| UC_T         | Urban Core Transit Oriented Development         |

[Top](#contents)

## units.csv

The "units.csv" file describes the default units to be used for storing complex data types in the model. The format of the file is as follows:

| Type     | Units    |
| -------- | -------- |
| currency | USD      |
| distance | MI       |
| area     | SQMI     |
| ![](./VERPAT_images/vdots.gif) | ![](./VERPAT_images/vdots.gif) |

The VisionEval model system keeps track of the types and units of measure of all data that is processed. More details about the file and structure can be found [here](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md#63-data-types-units-and-currency-deflators).

[Top](#contents)

# Inputs and Outputs

The VERPAT model is a compilation of several packages, listed below, the inputs of which are described respectively. The inputs are classified into five categories:

1. **User input files**: These are input files (model or scenario specific) that a user is recommended to change.
2. **User input model parameters**: These are input parameters (model or scenario specific), defined in [model_parameters.json](#model_parametersjson), that a user is recommended to change.
3. **Fixed input files**: These are input parameters specific to the model that are fixed.
4. **Fixed input model parameters**: These are input parameters specific to the model, defined in [model_parameters.json](#model_parametersjson), that are fixed.
5. **Internal module inputs**: These are inputs produced as output by other modules.

| MODULE                                                      | PACKAGE                                                      | RPAT             |
| ----------------------------------------------------------- | ------------------------------------------------------------ | ---------------- |
| [CreateHouseholds](#createhouseholds)                       | [VESimHouseholds](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESimHouseholds) | household        |
| [PredictWorkers](#predictworkers)                           | [VESimHouseholds](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESimHouseholds) | household        |
| [PredictIncome](#predictincome)                             | [VESimHouseholds](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESimHouseholds) | household        |
| [CreateBaseSyntheticFirms](#createbasesyntheticfirms)       | [VESyntheticFirms](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms) | household        |
| [CreateFutureSyntheticFirms](#createfuturesyntheticfirms)   | [VESyntheticFirms](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms) | household        |
| [CreateBasePlaceTypes](#createbaseplacetypes)               | [VELandUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VELandUse) | urban            |
| [CreateFuturePlaceTypes](#createfutureplacetypes)           | [VELandUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VELandUse) | urban            |
| [CreateBaseAccessibility](#createbaseaccessibility)         | [VETransportSupply](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupply) | accessibility    |
| [CreateFutureAccessibility](#createfutureaccessibility)     | [VETransportSupply](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupply) | accessibility    |
| [AssignVehicleFeatures](#assignvehiclefeatures)             | [VEHouseholdVehicles](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdVehicles) | vehicle          |
| [AssignVehicleFeaturesFuture](#assignvehiclefeaturesfuture) | [VEHouseholdVehicles](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdVehicles) | vehicle          |
| [CalculateTravelDemand](#calculatetraveldemand)             | [VEHouseholdTravel](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdTravel) | demand           |
| [CalculateTravelDemandFuture](#calculatetraveldemandfuture) | [VEHouseholdTravel](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdTravel) | demand           |
| [CalculateCongestionBase](#calculatecongestionbase)         | [VETransportSupplyUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupplyUse) | congestion       |
| [CalculateCongestionFuture](#calculatecongestionfuture)     | [VETransportSupplyUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupplyUse) | congestion       |
| [CalculateInducedDemand](#calculateinduceddemand)           | [VEHouseholdTravel](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdTravel) | induced          |
| [CalculatePolicyVmt](#calculatepolicyvmt)                   | [VEHouseholdTravel](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdTravel) | policyvmt        |
| [CalculateCongestionPolicy](#calculatecongestionpolicy)     | [VETransportSupplyUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupplyUse) | policycongestion |
| [ReportRPATMetrics](#reportrpatmetrics)                     | [VEReports](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEReports) | metrics          |

[Top](#contents)

## CreateHouseholds

This module creates simulated households for a model using inputs of population by age group for each Azone and year.

### User Input Files

1. **Household population (*azone_hh_pop_by_age.csv*)**: This file contains population estimates/forecasts by county and age cohort for each of the base and future years. The file format includes six age categories used by the population synthesis model:

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

2. **Household size (*azone_hhsize_targets.csv*)**: This file contains the household specific targets. This contain two household specific attributes:

   - **AveHhSize**: Average household size of households (non-group quarters)
   - **Prop1PerHh**: Proportion of households (non-group quarters) having only one person

   Here is a snapshot of the file:

   | Geo       | Year | AveHhSize | Prop1PerHh |
   | --------- | ---- | --------- | ---------- |
   | Multnomah | 2005 | NA        | NA         |
   | Multnomah | 2035 | NA        | NA         |

3. **Group quarter population (*azone_gq_pop_by_age.csv*)**: This file contains group quarters population estimates/forecasts by county and age cohort for each of the base and future years. The file format includes six age categories used by the population synthesis model:

   - **0-14**
   - **15-19**
   - **20-29**
   - **30-54**
   - **55-64**
   - **65 Plus**

   Here is a snapshot of the file:

   | Geo       | Year | GrpAge0to14 | GrpAge15to19 | GrpAge20to29 | GrpAge30to54 | GrpAge55to64 | GrpAge65Plus |
   | --------- | ---- | ----------- | ------------ | ------------ | ------------ | ------------ | ------------ |
   | Multnomah | 2005 | 0           | 0            | 0            | 1            | 0            | 0            |
   | Multnomah | 2035 | 0           | 0            | 0            | 1            | 0            | 0            |


### Module Outputs

1. **NumHh**: Number of households (non-group quarters)
2. **HhId**: Unique household ID
3. **HhSize**: Number of persons
4. **Age0to14**: Persons in 0 to 14 year old age group
5. **Age15to19**: Persons in 15 to 19 year old age group
6. **Age20to29**: Persons in 20 to 29 year old age group
7. **Age30to54**: Persons in 30 to 54 year old age group 
8. **Age55to64**: Persons in 55 to 64 year old age group
9. **Age65Plus**: Persons in 65 or older age group
10. **HhType**: Coded household age composition (e.g. 2-1-0-2-0-0) or Grp for group quarters

[Top](#contents)

## PredictWorkers

This module assigns workers by age to households and to non-institutional group quarters population. It is a simple model which predicts workers as a function of the household type and age composition. There is no responsiveness to jobs or how changes in the job market and demographics might change the worker age composition, but the user can exogenously adjust the relative employment by age group, Azone, and year. The values are the proportions of persons in the age group who are workers relative to the proportions in the estimation year.

### User Input Files

1. **Relative employment (*azone_relative_employment.csv*)**: This file contains ratio of workers to persons by age cohort in model year vs. estimation data year. This file contains five age cohorts:

   - **RelEmp15to19**: Ratio of workers to persons age 15 to 19 in model year vs. in estimation data year
   - **RelEmp20to29**: Ratio of workers to persons age 20 to 29 in model year vs. in estimation data year
   - **RelEmp30to54**: Ratio of workers to persons age 30 to 54 in model year vs. in estimation data year
   - **RelEmp55to64**: Ratio of workers to persons age 55 to 64 in model year vs. in estimation data year
   - **RelEmp65Plus**: Ratio of workers to persons age 65 or older in model year vs. in estimation data year

   Here is a snapshot of the file:

   | Geo       | Year | RelEmp15to19 | RelEmp20to29 | RelEmp30to54 | RelEmp55to64 | RelEmp65Plus |
   | --------- | ---- | ------------ | ------------ | ------------ | ------------ | ------------ |
   | Multnomah | 2005 | 1            | 1            | 1            | 1            | 1            |
   | Multnomah | 2035 | 1            | 1            | 1            | 1            | 1            |

### Internal Module Inputs

| Package         | Module                                | Outputs       | Description                                                  |
| --------------- | ------------------------------------- | ------------- | ------------------------------------------------------------ |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age0to14**  | Persons in 0 to 14 year old age group                        |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age15to19** | Persons in 15 to 19 year old age group                       |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age20to29** | Persons in 20 to 29 year old age group                       |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age30to54** | Persons in 30 to 54 year old age group                       |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age55to64** | Persons in 55 to 64 year old age group                       |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **Age65Plus** | Persons in 65 or older age group                             |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **HhType**    | Coded household age composition (e.g. 2-1-0-2-0-0) or Grp for group  quarters |

### Module Outputs

1. **Wkr15to19**: Workers in 15 to 19 year old age group
2. **Wkr20to29**: Workers in 20 to 29 year old age group
3. **Wkr30to54**: Workers in 30 to 54 year old age group
4. **Wkr55to64**: Workers in 55 to 64 year old age group
5. **Wkr65Plus**: Workers in 65 or older age group
6. **Workers**: Total number of workers
7. **NumWkr**: Number of workers residing in the zone

[Top](#contents)

## PredictIncome

This module predicts the income for each simulated household given the number of workers in each age group and the average per capita income for the Azone where the household resides.

### User Input Files

1. **Regional income (*azone_per_cap_inc.csv*)**: This file contains information on regional average per capita  household and group quarters income by forecast year in year 2000 dollars. The data can be obtained from the U.S. Department of [Commerce Bureau of Economic Analysis](http://www.bea.gov/regional/index.htm) for the current year or from regional or state sources for forecast years. In order to use current year dollars just replace ***2000*** in column labels with current year. For example, if the data is obtained in year 2005 dollars then the column labels in the file shown below will become **HHIncomePC.2005** and **GQIncomePC.2005**.
   Here is a snapshot of the file:

   | Geo       | Year | HHIncomePC.2000 | GQIncomePC.2000 |
   | --------- | ---- | --------------- | --------------- |
   | Multnomah | 2005 | 32515           | 0               |
   | Multnomah | 2035 | 40000           | 0               |

### Internal Module Inputs

| Package         | Module                                | Outputs       | Description                                                  |
| --------------- | ------------------------------------- | ------------- | ------------------------------------------------------------ |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **HhSize**    | Number of  persons                                           |
| VESimHouseholds | [CreateHouseholds](#createhouseholds) | **HhType**    | Coded household age composition (e.g. 2-1-0-2-0-0) or Grp for group  quarters |
| VESimHouseholds | [PredictWorkers](#predictworkers)     | **Wkr15to19** | Workers in 15 to 19 year old age group                       |
| VESimHouseholds | [PredictWorkers](#predictworkers)     | **Wkr20to29** | Workers in 20 to 29 year old age group                       |
| VESimHouseholds | [PredictWorkers](#predictworkers)     | **Wkr30to54** | Workers in 30 to 54 year old age group                       |
| VESimHouseholds | [PredictWorkers](#predictworkers)     | **Wkr55to64** | Workers in 55 to 64 year old age group                       |
| VESimHouseholds | [PredictWorkers](#predictworkers)     | **Wkr65Plus** | Workers in 65 or older age group                             |

### Module Outputs

1. **Income**: Total annual household (non-qroup & group quarters) income in year 1999 dollars.

[Top](#contents)

## CreateBaseSyntheticFirms

This module creates a set of firms for base year that represents the likely firm composition for the region, given the County Business Pattern data of firms by size and industry. Each firm is described in terms of the number of employees and its industry.

### User Input Files

1. **Employment (*azone_employment_by_naics.csv*)**: This file contains employment data for each of the counties that make up the region. The file is derived from County Business Pattern ([CBP](http://www.census.gov/econ/cbp/)) data by county. Industries are categorized by the North American Industrial Classification System (NAICS) 6 digit codes. Firm size categories are:

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

### Module Outputs

1. **naics**: The six digit naics code
2. **esizecat**: The employment size category
3. **numbus**: The number of businesses
4. **emp**: The number of employees in a business

[Top](#contents)

## CreateFutureSyntheticFirms

This module creates a set of firms for future year that represents the likely firm composition for the region, given the County Business Pattern data of firms by size and industry. Each firm is described in terms of the number of employees and its industry.

### User Input Parameters

1. **Employment Growth (*EmploymentGrowth*)**: This variable represents a growth rate for employment in the region between the base year and the future year. A rate of 1 indicates no changes in overall employment, a value of more than 1 indicates some growth (e.g., 1.5 = 50% growth) and a value of less than 1 indicates decline in employment. It should be defined in [model_parameters.json](#model_parametersjson) as follows:

   ```json
   {
       "NAME": "EmploymentGrowth",
       "VALUE": "1.5",
       "TYPE": "double",
       "UNITS": "multiplier",
       "PROHIBIT": "",
       "ISELEMENTOF": ""
   }
   ```

### Internal Module Inputs

| Package          | Module                                                | Outputs      | Description                           |
| ---------------- | ----------------------------------------------------- | ------------ | ------------------------------------- |
| VESyntheticFirms | [CreateBaseSyntheticFirms](#createbasesyntheticfirms) | **naics**    | The six digit naics code              |
| VESyntheticFirms | [CreateBaseSyntheticFirms](#createbasesyntheticfirms) | **esizecat** | The employment size category          |
| VESyntheticFirms | [CreateBaseSyntheticFirms](#createbasesyntheticfirms) | **numbus**   | The number of businesses              |
| VESyntheticFirms | [CreateBaseSyntheticFirms](#createbasesyntheticfirms) | **emp**      | The number of employees in a business |

### Module Outputs

1. **naics**: The six digit naics code
2. **esizecat**: The employment size category
3. **numbus**: The number of businesses
4. **emp**: The number of employees in a business

