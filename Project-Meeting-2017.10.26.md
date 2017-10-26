### Framework
  - Enable calling of modules from other modules
    - Needed to implement several modules (Carshare/AV, Budget, etc.)
    - Specs determine whether module can be called and whether module can call other modules
    - Framework enforces rules on calling and includes checks
    - Model initialization includes checking satisfaction of called module data requirements

### CalibrateHouseholdAttraction 
  - Eliminated need for CalibrateHouseholdAttraction module by modifying PredictHousing & LocateHouseholds modules
    - Current RSPM method for calibrating Bzone income attraction factors is very time consuming and clunky
    - Combined PredictHousing & LocateHouseholds modules into new PredictHousing module
    - New module eliminates need to calibrate attraction factors
    - Uses IPF to quickly allocate number of households by income quartile and housing type to Bzones

### Vehicle Module
  - Completed the module for setting up the vehicle table
  - Completed the module for determining vehicle types (auto, light truck) 
  - Completed the module for determining vehicle ages
    - Revised the code for this from GreenSTEP/RSPM to match average age targets rather than to adjust 95th percentile

### VETravelCosts package
  - Working on VETravelCosts package to include all modules which calculate various travel costs
  - Working on parking cost

### CarshareAV module
  - Working on CarshareAV module

8) Added a module to assign workers to job locations
    - Had earlier created PredictWorkers and LocateEmployment modules under the ODOT multimodal model contract
        - PredictWorkers assigns number of workers by age to each household
        - PredictEmployment balances jobs and workers
    - Realized that assigning workers to job locations simplifies parking cost model and makes much easier for users to develop inputs
    - Also open opportunities for future TDM (and other) models
    - Workers randomly allocated to Bzone job locations as function of number of Bzone jobs

### PAYD Module
  - Working with Nazneen (CH) to advise on PAYD module and produce datastore having data needed to implement

### Minor revisions to several modules
  - Minor revisions to several modules
  - Make consistent approach to UNITS spec for categorical variables

### Revised and tested VERSPM
  - Revised and tested VERSPM with added new PredictHousing, AssignVehicleType, CreateVehicleTable, and AssignVehicleAge modules
  - Tested with both datastore types: HDF5 and R data
    - HDF5: 19 minutes 11 seconds
    - R data: 6 minutes 59 seconds

### VERPAT translation
  - Received NTP to return to VERPAT translation
  - Planning a design meeting with Brian, Adi, and Colin to get us going
  - GreenSTEP work to follow since both require a good approach to zone synthesis to sync up with RSPM

### Repository transfer
  - @Ben to setup meeting to discuss upcoming transfer to Volpe

### Develop branch broken
  - @RSG investigating and will fix asap
  - Will add master and develop TravisCI build icons to the main readme

### Pilot review team
  - @Ben to send review results to Liming
