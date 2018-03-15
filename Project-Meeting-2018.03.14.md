# VERPAT
  - CalculatePolicyVmt module done
  - Working on final RPAT module - performance metrices - as part of new VEReports package
  - Should be done by end of next week / early the following week

# VERSPM
  - Completed VERoadPerformance package. This package combines the calculation of roadway DVMT by vehicle type (CalculateBaseRoadDvmt and CalculateFutureRoadDvmt modules) with the 'congestion' calculations (CalculateRoadPerformance). This involved considerable coding to corral code from different parts of the GreenSTEP_Sim.R script and the calcCongestion function to make into modules that are also understandable. Code was written so that it will also work for GreenSTEP and EERPAT. It is written so that it will work out of the box for different metropolitan areas around the country.
  - Plan to commit by end of this week
  - Next will return to VEEnergyAndEmissions and plan to complete by end of next week
  - Will work on VETravelCosts the final week of March and expect to complete by end of week

# Framework
  - Revised testModule to work for future year data sets [#149](https://github.com/gregorbj/VisionEval/issues/149)  
  - Enabled Get and Set specs for currency data to have units that don't specify a currency year. When no year is specified, the framework treats as base year [#150](https://github.com/gregorbj/VisionEval/issues/150).
  - Corrected bugs which prohibited reading dataset from datastore located in directory other than the current directory [#151](https://github.com/gregorbj/VisionEval/issues/151).
  - Made several changes to enable datastore referencing to work [#152](https://github.com/gregorbj/VisionEval/issues/152) (this feature is important for scenario management).
  - Made several changes to RD datastore functions to speed up writing to the datastore.

# Next Release / Test System
  - Ready to release version, but VEGUI broke with latest update to framework [#155](https://github.com/gregorbj/VisionEval/issues/155)  
  - Will merge develop to master via pull request [#156](https://github.com/gregorbj/VisionEval/pull/156) once fixed
  - Updated [Getting Started](https://github.com/gregorbj/VisionEval/wiki/Getting-Started)
  - Updated [Modules and Packages](https://github.com/gregorbj/VisionEval/wiki/Modules-and-Packages) page

# Project management
  - Reviewed, commented on, and closed several issues
  - Added a new [milestone](https://github.com/gregorbj/VisionEval/milestones) - End User Experience - for the next phase of work
  - Cleaned up the licensing throughout the repository [#47](https://github.com/gregorbj/VisionEval/issues/47)
  - Plan to stick with R 3.4 for completing VERPAT and VERSPM
  - Let's review who is on the meeting invite list - I'll send an email about this
