This page tracks the development road map for translating the existing RPAT and RSPM implementations into VisionEval models.

## Completed VE Packages and Modules
All completed VE modules are for VERSPM unless otherwise noted.

  - [VESyntheticFirms](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms)
    - CreateFutureSyntheticFirms (VERPAT)
    - CreateBaseSyntheticFirms (VERPAT)
  - [VESimHouseholds](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESimHouseholds)
    - CreateHouseholds
    - PredictWorkers
    - AssignLifeCycle
    - PredictIncome
    - PredictHousing
  - [VELandUse](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VELandUse)
    - LocateHouseholds
    - LocateEmployment
    - AssignDevTypes
    - Calculate4DMeasures
    - CalculateUrbanMixMeasure
  - [VETransportSupply](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETransportSupply)
    - AssignTransitService
    - AssignRoadMiles
  - [VEVehicleOwnership](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VEVehicleOwnership)
    - AssignVehicleOwnership
  - [VETravelDemand](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VETravelDemand)
    - CalculateHouseholdDVMT
    - CalculateAltModeTrips
    
## Planned VE Packages and Modules
Below are the remaining RSPM modules to be re-implemented as VE modules.

  - Demand Management With Car Services
    - idEcoWorkers, idImpHouseholds, adjDvmtEcoImp, idEcoDriverHh, idLowRollTire, idPayingParkers, calcParkCostAdj
  - Car Services And Autonomous Vehicles
    - Existing RSPM modules: calcCarSvcAvail, calcVehicleUse
  - Vehicle Characteristics
    - Existing RSPM modules: predictLtTruckOwn, calcVehicleAges, assignFuelEconomy, apportionDvmt, calcVehDvmt, assignPhev, assignEv
  - Calculate TruckVMT
    - Existing RSPM modules: adjustHvyVeh AgeDistribution, assignHvy VehFuelEconomy
  - Commercial Service Vehicle Travel
    - Existing RSPM modules: calcCommVeh TravelFromHh Income, calcCommVeh TravelFromHhDvmt, calcCommVeh TypeAgeProp, calcCommVeh Powertrain MpgMpkwh, calcCommVeh HcEvDvmt
  - Calculate Congestion
    - Existing RSPM modules: calcCongestion
  - TravelCost
    - Existing RSPM modules: calcVeh DepreciationExp, estPaydWeights, selectFromWeights, calcCosts, Calculate total cost and VMT surcharge
  - Fuel Consumption And Emissions
    - Existing RSPM modules: calcVehFuelElecCo2, calcCarSvcFuel ElecCo2Rates, calcCar SvcFuelElecCo2, calcFuel ElectricityUse, calcCommVeh Emissions, calcCommVehCosts, calcCommVeh EmissionRatesByAge, adjEcoTire
  
## Future VERPAT Migration 
The translation of RPAT to VERPAT will utilize and/or revise VE modules as needed.  For example:

  - household() will start from VESimHouseholds
  - urban() will start from VELandUse
  - accessibility() will start from VETransportSupply
  - vehicle() will start from VEVehicleOwnership
  - demand() will start from VETravelDemand
  - congestion() 
  - policy congestion()

