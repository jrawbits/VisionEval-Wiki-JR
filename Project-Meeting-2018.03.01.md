# RSPM Migration
  - @Brian working on congestion module as part of new VERoadPerformance package
    - Plan to deprecate VECommercialTravel and move functionality into VERoadPerformance 
    - New package calculates DVMT by year, vehicle class, facility type, etc.
    - Then calculates congestion levels
    - Still need to calculate travel speeds and facility type allocation
    - Lots of inline code documentation already
  - Will go back and finish VEEnergyAndEmissions once VERoadPerformance outputs VMTs and speeds
  - After that, the next package is VECosts for calculating HH level costs like parking
  - Probably done with VERSPM in about a month

# RPAT Migration
  - @Aditya should finish PolicyVMT translation tomorrow
  - Next week start on PolicyCongestion, which should take about a week to translate
  - The final module is performance metrics
  - We decided to create a VEReports package that does the following:
    - Includes functions to produce the existing RPAT metrics
    - Eventually will make use of new framework functions to query the datastore using user specified queries
    - We'll translate the RPAT functionality for now and then look to generalize it with the next revision, which depends on schedule and budget
    - We may add functions to VEReports that makes querying easier, and which may be moved to the framework once proven
    - This package is going to evolve quite a bit as we start to work more on end user stuff
    - @Brian share example of CALL module

# Repository Management
  - Job [#153.6](https://travis-ci.org/gregorbj/VisionEval/jobs/347814107) failed the test.R script test but Travis still passed?  @Ben to investigate

