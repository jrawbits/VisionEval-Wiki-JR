# VERPAT
  - CalculatePolicyVmt module done
  - Working on final RPAT module - performance metrices - as part of new VEReports package

# VERSPM
  - Completed VERoadPerformance package. This package combines the calculation of roadway DVMT by vehicle type (CalculateBaseRoadDvmt and CalculateFutureRoadDvmt modules) with the 'congestion' calculations (CalculateRoadPerformance). This involved considerable coding to corral code from different parts of the GreenSTEP_Sim.R script and the calcCongestion function to make into modules that are also understandable. Code was written so that it will also work for GreenSTEP and EERPAT. It is written so that it will work out of the box for different metropolitan areas around the country. Has been testing by testing all modules, but still needs to be tested in full RSPM run. Will be pushed to GitHub when that has been done.

# Framework
  - Revised testModule to work for future year data sets [#149](https://github.com/gregorbj/VisionEval/issues/149)  
  - Enabled Get and Set specs for currency data to have units that don't specify a currency year. When no year is specified, the framework treats as base year [#150].
  - Corrected bugs which prohibited reading dataset from datastore located in directory other than the current directory [#151].
  - Made several changes to enable datastore referencing to work [#152] (this feature is important for scenario management).
  - Made several changes to RD datastore functions to speed up writing to the datastore.

# Next Release / Test System
  - Ready to release version, but VEGUI broke with latest update to framework
  - Will merge develop to master via pull request [#156](https://github.com/gregorbj/VisionEval/pull/156) once fixed
  - Updated [Getting Started](https://github.com/gregorbj/VisionEval/wiki/Getting-Started)
  - Still need to update [Modules and Packages](https://github.com/gregorbj/VisionEval/wiki/Modules-and-Packages) page