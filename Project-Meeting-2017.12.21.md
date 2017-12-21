## RSPM Migration
  - Brian working on the energy and emissions model: VEEnergyAndEmissions
  - Made two significant revisions to the framework as a result:
    - Added an optional inputs pre-processor step called by the initialize module
    - Added an OPTIONAL tag to <INP> to check, if data is present
    - These can be used to pre-process input data and to run various data checks, such as proportions sum to 1
    - Still need to update documentation for framework revisions
  - Working in the storage-test branch and so will merge in develop before committing and testing
  - Moved some stuff from VEHouseholdVehicle to VEEnergyAndEmissions as well - vehicle powertrains, mpg, etc
  - VERPAT could use VEEnergyAndEmissions with default data by year as optional inputs maybe
  - Should be done with this in a few days
  - Next up is budgets and costs and congestion modules
  - Should be done with VERSPM by mid-Jan

## VERPAT
  - Adi finished placetypes module and accessibilities module
  - Adi working on vehicles module now
  - VESimHouseholds doesn't work for 0 group quarters - @Brian to investigate
  - Should be done with vehicles module by end of year
  - Next up is travelDemand module
  - Maybe new optional data inputs feature will make working with inputs of different years easier

## Repository Management
  - Adi merged storage-test into develop, fixed the tests, and updated VEGUI to work with RD files via the new framework API
  - Travis test limited to 50 minutes and we're now at 42 minutes
  - Installing all the dependent packages takes a long time
  - We could solve this problem by splitting VE resources into separate repositories [#129](https://github.com/gregorbj/VisionEval/issues/129)

## Project Management
  - We need to setup our administrative meeting again - say every 6 to 10 weeks
  - All work is currently being done under the AASHTO contract
  - General schedule for delivery is VERPAT software end of March, VEGUI/Visualizer end of May
    - There are [project milestones](https://github.com/gregorbj/VisionEval/milestones) for these project phases


