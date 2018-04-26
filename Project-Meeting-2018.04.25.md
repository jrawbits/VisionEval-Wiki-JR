# VERPAT 
  - [Documentation of inputs and outputs](VERPAT-Inputs-and-Outputs) almost complete
  - Working on some revisions to the inputs and outputs as a result of documenting modules since there was some inconsistency in the way the RunTypes are used throughout
  - Should be done by end of week

# VERSPM
  - All modules done and passing tests in a new branch, [rspm_complete](https://github.com/gregorbj/VisionEval/tree/rspm_complete)
  - Eliminated VECommercialTravel, VERoadPerformance, VEEnergyAndEmissions, and VETravelCosts, and replaced them with VEPowertrainsAndFuels and VETravelPerformance so still some work to do to merge to develop
  - Working on memo on conversion and differences from RSPM as a sort of verification document
  - Plan to reconcile revisions next week
  - Will do a release once ready

# Test System and Setup
  - Updated [Getting Started](https://github.com/gregorbj/VisionEval/wiki/Getting-Started) to refer to a new install.R script
  - Tested triggering builds of dependent projects in TravisCI if we decide to eventually go with [separate repositories](https://github.com/gregorbj/VisionEval/issues/129)