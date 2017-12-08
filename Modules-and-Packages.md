This page tracks progress on the current FHWA project to translate the existing RPAT and RSPM implementations into VisionEval models.  The larger, overall VisionEval roadmap is maintained on the [Development Roadmap](https://github.com/gregorbj/VisionEval/wiki/Development-Roadmap) page.  The translation of RPAT to VERPAT will utilize and/or revise VE modules as needed.  This work task is in the [Development Roadmap](https://github.com/gregorbj/VisionEval/wiki/Development-Roadmap).

Module Status Code Key:  
- I = module includes implementation code (i.e. it will run in a model)
- E = module includes code to estimate model parameters  
- T = module includes test code  
- D = module includes model documentation  
- V = module includes vignettes which explain what the module does and how it is used  

This table includes columns for Package, Module, Description, Status, Completion, and Notes.  Please scroll at the bottom of the table to see additional columns.


Package | Module | Description | Status | Completion | Notes
-- | -- | -- | -- | -- | --
VESyntheticFirms | CreateBaseSyntheticFirms | Creates base year synthetic firms by NAICS and number of jobs | I |   | VERPAT model
VESyntheticFirms | CreateFutureSyntheticFirms | Creates future year synthetic firms by NAICS and number of jobs | I |   | VERPAT model
VESimHouseholds | CreateHouseholds | Creates households with number of persons by age group | EIT | July |  
VESimHouseholds | PredictWorkers | Assigns number of workers by age group to households | EIT | July |  
VESimHouseholds | AssignLifeCycle | Assigns household lifecycle category | EIT | July |  
VESimHouseholds | PredictIncome | Predict total household income | EIT | July |  
VELandUse | PredictHousing | Predict household housing (single-family, multifamily, group quarters)   and place each household in a Bzone | EIT | July |  
VELandUse | LocateEmployment | Allocate number of jobs by Bzone and type (total, retail, service) &   assign jobsite Bzone to workers and create worker table | EIT | July |  
VELandUse | AssignDevTypes | Assign development type to household (urban, rural) | EIT | July |  
VELandUse | Calculate4DMeasures | Calculate Bzone density, diversity, design, and accessibility measures | EIT | July |  
VELandUse | CalculateUrbanMixMeasure | Assign urban mixed use attribute to households | EIT | July |  
VELandUse | CalculateBasePlaceTypes | Assign households and firms to the place types (bzones) for the base year | IT | December | VERPAT model |
VELandUse | CalculateFuturePlaceTypes | Assign households and firms to the place types (bzones) for the years that are not base year | IT | December | VERPAT model |
VETransportSupply | AssignTransitService | Calculates transit revenue miles per capita for region and Bzone transit   service level | EIT | July |  
VETransportSupply | AssignRoadMiles | Calculates regional per capita lane-miles for freeways and for arterials | EIT | July |  
VETransportSupply | CalculateCongestion | Models roadway speeds, delay, and congestion costs |   | November |  
VEHouseholdVehicles | AssignVehicleOwnership | Assign number of vehicles owned by household | EIT | July |  
VEHouseholdVehicles | AssignCarServiceAV | Identifies household use of car services and adjusts vehicle ownership.   Autonomous vehicle deployment. |   | November |  
VEHouseholdVehicles | AssignVehicleType | Assigns vehicle type (auto, light truck) to each household vehicle | EIT | October |  
VEHouseholdVehicles | CreateVehicleTable | Creates vehicle table and populates with household and vehicle IDs,   geography, and vehicle type | EIT | October |  
VEHouseholdVehicles | AssignVehicleAge | Assign age to each household vehicle | EIT | October |  
VEHouseholdVehicles | AssignPowertrain | Assigns powertrain type (ICE, HEV, PHEV, EV) to each household vehicle | EIT | October |  
VEHouseholdTravel | CalculateHouseholdDVMT | Calculates household DVMT on household vehicles and carshare vehicles | EIT | October |  
VEHouseholdTravel | CalculateAltModeTrips | Calculates household walk trips, bike trips, and transit trips | IT | August |  
VEHouseholdTravel | DivertSovTravel | Calculates proportional reduction of DVMT based on user-established goals   for shifting short-range SOV tours to bike or similar "slow" modes | EIT | November |  
VEHouseholdTravel | AssignVehicleDvmtSplit | Determines how household DVMT is split between household vehicles | EIT | November |  
VEHouseholdTravel | AssignVehicleDvmt | Assigns household DVMT to household vehicles | EIT | November |  
VEHouseholdTravel | CalculateVehicleEnergySplit | Determines proportions of DVMT of each vehicle powered by stored   electricity vs. on-board hydrocarbon fuel | EIT | November |  
VECommercialTravel | CalculateLDVCommerialDVMT | Calculate light-duty commercial service vehicle DVMT |   | November |  
VECommercialTravel | CalculateHDVCommercialDVMT | Calculate heavy-duty vehicle DVMT |   | November |  
VECommercialTravel | CalculatePTDVMT | Calculates public transit DVMT by type |   | November |  
VECommercialTravel | AssignLDVCharacteristics | Assign light-duty vehicle age, powertrain, and fuel type characteristics |   | November |  
VECommercialTravel | AssignHDVCharacteristics | Assign heavy-duty vehicle age, powertrain, and fuel type characteristics |   | November |  
VECommercialTravel | AssignPTVehicleCharacteristics | Assign public transit vehicle age, powertrain, and fuel type   characteristics |   | November |  
VEEnergyAndEmissions | CharacterizeLightDutyVehicles | Input light duty vehicle characteristics by model year, vehicle type, and   powertrain |   | November |  
VEEnergyAndEmissions | CharacterizeHeavyDutyVehicles | Input heavy duty vehicle characteristics by model year, vehicle type, and   powertrain |   | November |  
VEEnergyAndEmissions | AdjustFuelConsumptionRates | Adjust vehicle fuel economy to account for congestion and eco-driving |   | November |  
VEEnergyAndEmissions | CalculateHouseholdEnergy | Calculate household vehicle energy consumption by type (hydrocarbon fuel,   electricity) |   | November |  
VEEnergyAndEmissions | CalculateHouseholdEmissions | Calculate household vehicle emissions |   | November |  
VEEnergyAndEmissions | CalculateCommercialEmissions | Calculate commercial LDV, HDV, and PT emissions |   | November |  
VETravelCosts | AssignUnitCosts | Input unit cost assumptions for vehicle travel, energy, emissions, etc. |   | November |  
VETravelCosts | AssignPAYDInsurance | Identifies which households have pay-as-you-drive insurance |   | November |  
VETravelCosts | CalculateHouseholdCosts | Calculates household costs for owning and operating vehicles |   | November |  
VETravelCosts | CalculateRoadCostsAndRevenues | Calculates roadway costs and revenues and additional taxes to balance |   | November |  

