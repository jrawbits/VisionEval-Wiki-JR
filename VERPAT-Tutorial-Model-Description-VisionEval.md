### Overview of the VERPAT modeling process

The diagram below illustrates the modeling system with inputs, model components, and feedback loops. Links are provided to the source code that implements each section.

[![](VERPAT-Tutorial-images/rpat_process3.png)](VERPAT-Tutorial-images/rpat_process3.png)

<table>
  <tr>
    <td> <ul> 
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESimHouseholds"> Households Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms"> Firms Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VELandUse"> Land Use Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupply"> Transport Supply Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdVehicles"> Household Vehicles Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEHouseholdTravel"> Household Travel Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupplyUse"> Transport Supply Use Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETravelPerformance"> Travel Performance Package </a> </li>
	<li> <a href="https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEReports"> Reporting Package </a> </li>
	</ul> </td>
  </tr>
</table>


For more, see [[VERPAT Modules and Outputs | VERPAT-Modules-and-Outputs]].


### VERPAT Objectives

RPAT is a tool for evaluating the impact of various smart growth policies. RPAT is designed to be a high-level evaluation at a regional scale that can bridge the distance between evaluating smart growth policies during a regional visioning process and evaluating smart growth policies at a project or alternative level in a regional transportation plan. RPAT evaluates policy scenarios to identify the most promising policies that could be further tested using a more detailed project-level tool. Currently, RPAT can provide information on the following changes in the regional system:
 Built Environment – changes to the urban form (proportion of population and employment living in mixed-use areas, transit-oriented developments, or rural/greenfield areas)
 Travel Demand – changes in population demographics (age structure), changes in personal income, changes in firms by size or industry, relative amounts of development occurring in urban core, close-in communities, suburban or rural areas, urban core, auto and light truck proportions by year, and induced demand
 Transportation Supply – amounts of regional transit service, amounts of freeway and arterial capacity
 Policies – pricing (vehicle miles traveled charges or parking pricing programs), intelligent transportation system (ITS) strategies for freeways and arterials, demand management (vanpool, telecommuting, ridesharing, and transit pass programs)
RPAT is designed to evaluate regions, which can be a multi-county metropolitan region. It distinguishes between population and employment living/working in the urban core, close-in communities, suburban and rural/greenfield areas based on densities, diversity in land uses, street design or intersection densities, job accessibility by auto, distances to transit stops, and connectivity of the street system.
The intended audience for RPAT is regional decision-makers and land use and transportation planners involved in the development and evaluation of transportation and land use policies and who need to conduct scenario planning to evaluate smart growth policies and determine their impact on travel demand. RPAT was designed to address as many of the limitations identified in the research as possible and to provide a tool that filled a gap in the set of available tools. The relationships in the RPAT tool were based upon the background research conducted for the SHRP 2 C16 project. RPAT is designed to allow the evaluation of a wide range of policies and combination of policies in a consistent framework quickly and easily so that promising smart growth strategies can be
USER’S
GUIDE
AASHTO
Rapid Policy Assessment Tool Documentation
4 April 30, 2015
identified and pursued in the land use and transportation planning processes. RPAT is intended to precede and supplement more sophisticated modeling efforts, which can be used to evaluate specific smart growth projects. It is designed to be accessible to land use and transportation planners with no modeling experience.RPAT is a tool for evaluating the impact of various smart growth policies. RPAT is designed to be a high-level evaluation at a regional scale that can bridge the distance between evaluating smart growth policies during a regional visioning process and evaluating smart growth policies at a project or alternative level in a regional transportation plan. RPAT evaluates policy scenarios to identify the most promising policies that could be further tested using a more detailed project-level tool. Currently, RPAT can provide information on the following changes in the regional system:
 Built Environment – changes to the urban form (proportion of population and employment living in mixed-use areas, transit-oriented developments, or rural/greenfield areas)
 Travel Demand – changes in population demographics (age structure), changes in personal income, changes in firms by size or industry, relative amounts of development occurring in urban core, close-in communities, suburban or rural areas, urban core, auto and light truck proportions by year, and induced demand
 Transportation Supply – amounts of regional transit service, amounts of freeway and arterial capacity
 Policies – pricing (vehicle miles traveled charges or parking pricing programs), intelligent transportation system (ITS) strategies for freeways and arterials, demand management (vanpool, telecommuting, ridesharing, and transit pass programs)
RPAT is designed to evaluate regions, which can be a multi-county metropolitan region. It distinguishes between population and employment living/working in the urban core, close-in communities, suburban and rural/greenfield areas based on densities, diversity in land uses, street design or intersection densities, job accessibility by auto, distances to transit stops, and connectivity of the street system.
The intended audience for RPAT is regional decision-makers and land use and transportation planners involved in the development and evaluation of transportation and land use policies and who need to conduct scenario planning to evaluate smart growth policies and determine their impact on travel demand. RPAT was designed to address as many of the limitations identified in the research as possible and to provide a tool that filled a gap in the set of available tools. The relationships in the RPAT tool were based upon the background research conducted for the SHRP 2 C16 project. RPAT is designed to allow the evaluation of a wide range of policies and combination of policies in a consistent framework quickly and easily so that promising smart growth strategies can be
USER’S
GUIDE
AASHTO
Rapid Policy Assessment Tool Documentation
4 April 30, 2015
identified and pursued in the land use and transportation planning processes. RPAT is intended to precede and supplement more sophisticated modeling efforts, which can be used to evaluate specific smart growth projects. It is designed to be accessible to land use and transportation planners with no modeling experience.RPAT is a tool for evaluating the impact of various smart growth policies. RPAT is designed to be a high-level evaluation at a regional scale that can bridge the distance between evaluating smart growth policies during a regional visioning process and evaluating smart growth policies at a project or alternative level in a regional transportation plan. RPAT evaluates policy scenarios to identify the most promising policies that could be further tested using a more detailed project-level tool. Currently, RPAT can provide information on the following changes in the regional system:
 Built Environment – changes to the urban form (proportion of population and employment living in mixed-use areas, transit-oriented developments, or rural/greenfield areas)
 Travel Demand – changes in population demographics (age structure), changes in personal income, changes in firms by size or industry, relative amounts of development occurring in urban core, close-in communities, suburban or rural areas, urban core, auto and light truck proportions by year, and induced demand
 Transportation Supply – amounts of regional transit service, amounts of freeway and arterial capacity
 Policies – pricing (vehicle miles traveled charges or parking pricing programs), intelligent transportation system (ITS) strategies for freeways and arterials, demand management (vanpool, telecommuting, ridesharing, and transit pass programs)
RPAT is designed to evaluate regions, which can be a multi-county metropolitan region. It distinguishes between population and employment living/working in the urban core, close-in communities, suburban and rural/greenfield areas based on densities, diversity in land uses, street design or intersection densities, job accessibility by auto, distances to transit stops, and connectivity of the street system.
The intended audience for RPAT is regional decision-makers and land use and transportation planners involved in the development and evaluation of transportation and land use policies and who need to conduct scenario planning to evaluate smart growth policies and determine their impact on travel demand. RPAT was designed to address as many of the limitations identified in the research as possible and to provide a tool that filled a gap in the set of available tools. The relationships in the RPAT tool were based upon the background research conducted for the SHRP 2 C16 project. RPAT is designed to allow the evaluation of a wide range of policies and combination of policies in a consistent framework quickly and easily so that promising smart growth strategies can be
USER’S
GUIDE
AASHTO
Rapid Policy Assessment Tool Documentation
4 April 30, 2015
identified and pursued in the land use and transportation planning processes. RPAT is intended to precede and supplement more sophisticated modeling efforts, which can be used to evaluate specific smart growth projects. It is designed to be accessible to land use and transportation planners with no modeling experience.RPAT is a tool for evaluating the impact of various smart growth policies. RPAT is designed to be a high-level evaluation at a regional scale that can bridge the distance between evaluating smart growth policies during a regional visioning process and evaluating smart growth policies at a project or alternative level in a regional transportation plan. RPAT evaluates policy scenarios to identify the most promising policies that could be further tested using a more detailed project-level tool. Currently, RPAT can provide information on the following changes in the regional system:
 Built Environment – changes to the urban form (proportion of population and employment living in mixed-use areas, transit-oriented developments, or rural/greenfield areas)
 Travel Demand – changes in population demographics (age structure), changes in personal income, changes in firms by size or industry, relative amounts of development occurring in urban core, close-in communities, suburban or rural areas, urban core, auto and light truck proportions by year, and induced demand
 Transportation Supply – amounts of regional transit service, amounts of freeway and arterial capacity
 Policies – pricing (vehicle miles traveled charges or parking pricing programs), intelligent transportation system (ITS) strategies for freeways and arterials, demand management (vanpool, telecommuting, ridesharing, and transit pass programs)
RPAT is designed to evaluate regions, which can be a multi-county metropolitan region. It distinguishes between population and employment living/working in the urban core, close-in communities, suburban and rural/greenfield areas based on densities, diversity in land uses, street design or intersection densities, job accessibility by auto, distances to transit stops, and connectivity of the street system.
The intended audience for RPAT is regional decision-makers and land use and transportation planners involved in the development and evaluation of transportation and land use policies and who need to conduct scenario planning to evaluate smart growth policies and determine their impact on travel demand. RPAT was designed to address as many of the limitations identified in the research as possible and to provide a tool that filled a gap in the set of available tools. The relationships in the RPAT tool were based upon the background research conducted for the SHRP 2 C16 project. RPAT is designed to allow the evaluation of a wide range of policies and combination of policies in a consistent framework quickly and easily so that promising smart growth strategies can be
USER’S
GUIDE
AASHTO
Rapid Policy Assessment Tool Documentation
4 April 30, 2015
identified and pursued in the land use and transportation planning processes. RPAT is intended to precede and supplement more sophisticated modeling efforts, which can be used to evaluate specific smart growth projects. It is designed to be accessible to land use and transportation planners with no modeling experience.



### VERPAT Modules

[] = indicates VE modules

  1. **Define Households** - *Households Package*  
Create synthetic households for the region, including persons [Create Households] and workers [Predict Workers] by age group. This determines lifecycle category for households (i.e. Elderly couple, Family with small children, single middle aged adults, etc.)[AssignLifecycle]. Identify total income for each household [PredictIncome].
  2. **Assign Land Use and Other Policies** - *Land Use Package*  
Determines the dwelling type (single-family, multifamily, group quarters) for each household and their location within a zone of the region [PredictHousing]. Allocate jobs by type (total, retail, service) and their location in the region, and assign household workers to these employment locations [Locate Employment]. Assign land use characteristics to each zone and the households and workplaces within that zone. These include an initial development type (either urban or rural) [AssignDevType], 4D built form measures (e.g., density, diversity, design, and accessibility) [Calculate4DMeasures], which enables identification of mixed use areas (i.e., that meet the density, diversity, design, and accessibility criteria) [CalculateUrbanMixMeasure]. Add policies as they apply to each zone and thus home and work location. These include zone-based parking restrictions and price [Parking Restrictions], Demand Management Programs (households and/or worker participation) [AssignDemandManagement], car sharing services (TNC’s) availability [AssignCarSvcAvailability].
  3. **Assign Transportation System** - *Transport Supply Package*  
Assign the regional transportation system, including road lane miles for freeways and arterials [AssignRoadMiles] and transit bus-equivalent revenue miles [AssignTransitService] per capita and transit vehicle-miles by vehicle type. Transit service is identified by zone.
  4. **Assign Vehicle Characteristics** - *Household Vehicle Package*  
Assigns household driver and vehicle characteristics. This includes the number of drivers by age group [AssignDrivers], number of vehicles owned [AssignVehicleOwnership] and their type (auto or light truck) [AssignVehicleType], and age [AssignVehicleAge]. The ownership cost of each household vehicle is calculated [CalculateVehicleOwnCost] and adjusted for car service usage, where rates are competitive [AdjustVehicleOwnership].
  5. **Estimate VMT** - *Household Travel Package*  
Calculate multi-modal travel. This includes total number of household trips [CalculateVehicleTrips] and daily VMT for household and car service vehicles [CalculateHouseholdDvmt]. Calculate non-auto trips and miles per household, including walking, biking and transit [CalculateAltModeTrips]. Adjust auto VMT, based on short-trip diversion input, i.e., the proportional of short-range single occupant automobile trips to bicycle or similar "non-auto" modes [DivertSovTravel].
  6. **Estimate GHG** - *Powertrain and Fuels Package*  
Calculate the average carbon intensity of fuels by vehicle type and the carbon intensity of electricity [CalculateCarbonIntensity]. Assigns powertrain types (gasoline, electric, hybrid, plug-in hybrid) and associated attributes to household and car share vehicles [AssignHhVehiclePowertrain].
  7. **Iterate to Balance VMT with Costs** - *Travel Performance Package*  
Calculate daily light duty VMT (household and commercial vehicles) by urbanized area, vehicle type, and road class [CalculateBaseRoadDvmt] [CalculateFutureRoadDvmt]. Calculate urbanized area roadway congestion, speeds, and delay, and then divides travel between freeways and arterials based on congestion and pricing levels [CalculateRoadPerformance]. Adjust vehicle fuel efficiency (MPG and MPKwh) by vehicle type to reflect the effects of congested travel speeds, and transfer adjustments to household vehicles [CalculateMpgMpkwhAdjustments] [AdjustHhVehicleMpgMpkwh]. Calculate operating costs across all household vehicles and use that to allocate DVMT among vehicles and the use of car services. [CalculateVehicleOperatingCost].
Adjust VMT as necessary to fit within transportation share of overall household budget. Calculate household vehicle travel energy consumption and emissions including from the use of carsharing. Calculate final travel, energy and emissions [BudgetHouseholdDvmt].
  8. **Non-household Travel and Emissions** - *Travel Performance Package*  
Calculate the energy consumptions and emissions for non-household vehicles. This includes light duty commercial and heavy duty trucks and public transit vehicles [Commercial Vehicle Energy and Emissions] [Public Transit Energy and Emissions].

Performance metrics are calculated in the [VEReports package](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEReports).  For more information, also see [VERPAT Modules and Outputs](https://github.com/gregorbj/VisionEval/wiki/VERPAT-Modules-and-Outputs#reportrpatmetrics).  
  
### For more information

  + [VisionEval Model System Design and Users Guide](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md)
  + [TravelWorks Rapid Policy Assessment Tool](https://planningtools.transportation.org/551/rapid-policy-analysis-tool.html)
  + [RPAT User manual](https://planningtools.transportation.org/files/63.pdf)

[[Overview | VERPAT-Tutorial-Overview]]
