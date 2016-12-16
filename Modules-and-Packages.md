|  R Package   |  VE Module |  RPAT Module Today | RSPM Module Today | VE RPAT |  VE RSPM |
| --- | --- | --- | --- | --- | ---|
| SyntheticHouseholds | Create Synthetic Households | household() | createHhByAge, predictIncome, Supplemental household attributes, other | X | X |
| GroupQuarters PopulationSynthesis | Group Quarters Population Synthesis | NA | Not functionalized |   | X |
| SyntheticFirms | Create Synthetic Firms | household() | NA | X |   |
| SetupZones | Setup Zones | NA | Setup zones, Calculate derived land use attributes, predictBldgType |   | X |
| CreatePlaceTypes | Create Place Types | urban() | NA | X |   |
| TransportationSupply | Transportation Supply | accessibility() | Transportation supply, Parking supply | X | X |
| HouseholdLocation | Household location | NA | Not functionalized |   | X |
| DemandManagement WithCarServices | Demand Management With Car Services | NA | idEcoWorkers, idImpHouseholds, adjDvmtEcoImp, idEcoDriverHh, idLowRollTire, idPayingParkers, calcParkCostAdj |   | X |
| Calculate VehicleOwnership | Calculate Vehicle Ownership | vehicle() | predictVehOwn, group qtr not functionalized | X | X |
| CarServices AndAutonomousVehicles | Car Services And Autonomous Vehicles | NA | calcCarSvcAvail, calcVehicleUse |   | X |
| VehicleCharacteristics | Vehicle Characteristics | NA | predictLtTruckOwn, calcVehicleAges, assignFuelEconomy, apportionDvmt, calcVehDvmt, assignPhev, assignEv |  | X |
| Calculate HouseholdAutoVMT | Calculate Household Auto VMT | demand() | predictAveDvmt, predictMaxDvmt, calcAdjAveDvmt | X | X |
| CalculateTruckVMT | Calculate Truck VMT | demand() | adjustHvyVehAgeDistribution, assignHvyVehFuelEconomy | X | X |
| CalculateAltModeVMT | Calculate Alt Mode VMT | demand() | predictLightVehicles, calcLtVehDvmt, calcAltModeTrips | X | X |
| Commercial ServiceVehicleTravel | Commercial service vehicle travel | NA | calcCommVeh TravelFromHhIncome, calcCommVeh TravelFromHhDvmt, calcCommVeh TypeAgeProp, calcCommVe hPowertrainMpgMpkwh, calcCommVeh HcEvDvmt |  | X |
| CalculateCongestion | Calculate Congestion | congestion() | calcCongestion | X | X |
| InducedGrowthAndTravel | Induced Growth And Travel | policycongestion() | NA | X |   |
| PolicyAdjusted TravelDemand | Policy Adjusted Travel Demand | policycongestion() | NA | X |   |
| PolicyAdjusted Congestion | Policy Adjusted Congestion | policycongestion() | NA | X |   |
| TravelCost | Travel Cost | NA | calcVeh DepreciationExp, estPaydWeights, selectFromWeights, calcCosts, Calculate total cost and VMT surcharge |   | X |
| FuelConsumption AndEmissions | Fuel Consumption and Emissions | NA | calcVehFuelElecCo2, calcCarSvcFuel ElecCo2Rates, calcCar SvcFuelElecCo2, calcFuel ElectricityUse, calcCommVeh Emissions, calcCommVehCosts, calcCommVeh EmissionRatesByAge, adjEcoTire |   | X |
