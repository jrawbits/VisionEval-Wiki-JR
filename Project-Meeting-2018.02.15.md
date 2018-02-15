# VERSPM
  - Revised the Initialize module of the VEEnergyAndEmissions package to include additional data checks 
  - Corrected testModule code because the results weren't being written to the datastore
  - Completed the CalculateCarbonIntensity module in the VEEnergyAndEmissions package
  - Added the calculation of VMT by transit vehicle type (van, bus, rail) to the AssignTransitService module 
  - A third of the way through the CalculateCongestion module required for VEEnergyAndEmissions package
  - Added the ability to adjust worker employment rates by age group in the PredictWorkers module
  - Created the AssignDrivers module in the VEHouseholdVehicles package to allows users to adjust the relative licensing rates by age group and modified the AssignVehicleOwnership and CalculateTravelDemand modules to use drivers rather than driving age persons
  - Plans for completion of the VEEnergyAndEmissions package

# VERPAT
  - Done coding the induced model, and testing and documentation should be done by COB Friday
  - VERPAT run types will be separate modules, with related names but separate INP specs
  - They will still be in the same package though so they can make use of shared code 
  - The induced model already does this.  For example `AssignVehicleFeatures_Existing` and `AssignVehicleFeatures_Future`
  - Next module to translate is policy_vmt, which should be done in a couple of weeks
  - policy_congestion is the module after that, and should take probably two weeks to complete

# Release planning
  - Reviewed the new parallel Travis build process with the technical team
  - Waiting on VEEnergyAndEmissions and VERPAT induced modules to be completed before merging to master (i.e. making a new release of the software)
  - VE organization should probably fork master once we merge
