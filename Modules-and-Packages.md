This page tracks the development road map for translating the existing RPAT and RSPM implementations into VisionEval models.  All completed VE modules are for VERSPM unless otherwise noted.  

## Completed VisionEval Packages and Modules
  - VESyntheticFirms
    - CreateFutureSyntheticFirms (for VERPAT pilot)
    - CreateBaseSyntheticFirms (for VERPAT pilot)
  - VESimHouseholds
    - CreateHouseholds
    - PredictWorkers
    - AssignLifeCycle
    - PredictIncome
    - PredictHousing
  - VELandUse
    - LocateHouseholds
    - LocateEmployment
    - AssignDevTypes
    - Calculate4DMeasures
    - CalculateUrbanMixMeasure
  - VETransportSupply
    - AssignTransitService
    - AssignRoadMiles
  - VEVehicleOwnership
    - AssignVehicleOwnership
  - VETravelDemand
    - CalculateHouseholdDVMT
    - CalculateAltModeTrips
    
## Planned VisionEval Packages and Modules (and existing RSPM modules)
  - Demand Management With Car Services
    - (idEcoWorkers, idImpHouseholds, adjDvmtEcoImp, idEcoDriverHh, idLowRollTire, idPayingParkers, calcParkCostAdj)
  - Car Services And Autonomous Vehicles
    - (calcCarSvcAvail, calcVehicleUse)
  - Vehicle Characteristics
    - (predictLtTruckOwn, calcVehicleAges, assignFuelEconomy, apportionDvmt, calcVehDvmt, assignPhev, assignEv	)
  - Calculate TruckVMT
    - (adjustHvyVeh AgeDistribution, assignHvy VehFuelEconomy)
  - Commercial Service Vehicle Travel
    - (calcCommVeh TravelFromHh Income, calcCommVeh TravelFromHhDvmt, calcCommVeh TypeAgeProp, calcCommVeh Powertrain MpgMpkwh, calcCommVeh HcEvDvmt)
  - Calculate Congestion
    - (calcCongestion)
  - TravelCost
    - (calcVeh DepreciationExp, estPaydWeights, selectFromWeights, calcCosts, Calculate total cost and VMT surcharge)
  - Fuel Consumption And Emissions
    - (calcVehFuelElecCo2, calcCarSvcFuel ElecCo2Rates, calcCar SvcFuelElecCo2, calcFuel ElectricityUse, calcCommVeh Emissions, calcCommVehCosts, calcCommVeh EmissionRatesByAge, adjEcoTire)
  
## Future VERPAT Migration 
  - Will utilize and/or revise VE modules as needed for completing VERPAT, such as:
    - household() will start from VESimHouseholds
    - urban() will start from VELandUse
    - accessibility() will start from VETransportSupply
    - vehicle() will start from VEVehicleOwnership
    - demand() will start from VETravelDemand
    - congestion() 
    - policy congestion()

