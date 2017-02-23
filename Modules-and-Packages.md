|  R Package   |  VE Module |  RPAT Module Today | RSPM Module Today | VE RPAT |  VE RSPM |
| --- | --- | --- | --- | --- | ---|
| VESimHouseholds | [Create Households](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms) | household() | createHhByAge, predictIncome, Supplemental household attributes, other | X | X |
| Group Quarters Population Synthesis | Group Quarters Population Synthesis | NA | Not functionalized |   | X |
| VESyntheticFirms | [Create Base Synthetic Firms](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms) | household() | NA | X |   |
| VESyntheticFirms | [Create Future Synthetic Firms](https://github.com/gregorbj/VisionEval/tree/master/sources/modules/VESyntheticFirms) | household() | NA | X |   |
| Setup Zones | Setup Zones | NA | Setup zones, Calculate derived land use attributes, predictBldgType |   | X |
| Create Place Types | Create Place Types | urban() | NA | X |   |
| Transportation Supply | Transportation Supply | accessibility() | Transportation supply, Parking supply | X | X |
| Household Location | Household location | NA | Not functionalized |   | X |
| Demand Management With Car Services | Demand Management With Car Services | NA | idEcoWorkers, idImpHouseholds, adjDvmtEcoImp, idEcoDriverHh, idLowRollTire, idPayingParkers, calcParkCostAdj |   | X |
| Calculate Vehicle Ownership | Calculate Vehicle Ownership | vehicle() | predictVehOwn, group qtr not functionalized | X | X |
| Car Services And Autonomous Vehicles | Car Services And Autonomous Vehicles | NA | calcCarSvcAvail, calcVehicleUse |   | X |
| Vehicle Characteristics | Vehicle Characteristics | NA | predictLtTruckOwn, calcVehicleAges, assignFuelEconomy, apportionDvmt, calcVehDvmt, assignPhev, assignEv |  | X |
| Calculate Household AutoVMT | Calculate Household Auto VMT | demand() | predictAveDvmt, predictMaxDvmt, calcAdjAveDvmt | X | X |
| Calculate TruckVMT | Calculate Truck VMT | demand() | adjustHvyVeh AgeDistribution, assignHvy VehFuelEconomy | X | X |
| Calculate AltModeVMT | Calculate Alt Mode VMT | demand() | predictLight Vehicles, calcLtVehDvmt, calcAltModeTrips | X | X |
| Commercial Service Vehicle Travel | Commercial service vehicle travel | NA | calcCommVeh TravelFromHh Income, calcCommVeh TravelFromHhDvmt, calcCommVeh TypeAgeProp, calcCommVeh Powertrain MpgMpkwh, calcCommVeh HcEvDvmt |  | X |
| Calculate Congestion | Calculate Congestion | congestion() | calcCongestion | X | X |
| Induced Growth And Travel | Induced Growth And Travel | policy congestion() | NA | X |   |
| Policy Adjusted Travel Demand | Policy Adjusted Travel Demand | policy congestion() | NA | X |   |
| Policy Adjusted Congestion | Policy Adjusted Congestion | policy congestion() | NA | X |   |
| TravelCost | Travel Cost | NA | calcVeh DepreciationExp, estPaydWeights, selectFromWeights, calcCosts, Calculate total cost and VMT surcharge |   | X |
| Fuel Consumption And Emissions | Fuel Consumption and Emissions | NA | calcVehFuelElecCo2, calcCarSvcFuel ElecCo2Rates, calcCar SvcFuelElecCo2, calcFuel ElectricityUse, calcCommVeh Emissions, calcCommVehCosts, calcCommVeh EmissionRatesByAge, adjEcoTire |   | X |

The columns in the table are as follows:
  - R Package: Name of the package to group modules.
  - VE Module: Description of a VisionEval module to carry out some defined functionality.
  - RPAT Module Today: The name of the RPAT function which now embodies the module functionality. NA means the functionality is not present.
  - RSPM Module Today: The name of RSPM functions or if just part of a script (not functionalized) which embodies the module functionality. NA means the functionality is not present.
  - VE RPAT: Checkmark if the module would be used for RPAT.
  - VE RSPM: Checkmark if the module would be used for RSPM.
