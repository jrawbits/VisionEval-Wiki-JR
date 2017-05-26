## VESimHouseholds 
  - Brian completed all the modules in the VESimHouseholds package. These modules include:
    - CreateHouseholds - creates simulated households with persons by age and also non-institutional group quarters population
    - PredictWorkers - predicts workers by age for each household (this is a new module which is needed for Liming's new multimodal travel models)
    - AssignLifeCycle - assigns a life cycle category to each household (also required by Liming's models)
    - PredictIncome - predicts annual household income. I reestimated this model from the original RSPM using the worker by age information which wasn't in the earlier model. This substantially improved the model fit.
    - PredictHousing - predicts the housing type (single family, multifamily, group quarters) for each household.
   - All the preparation of the estimation data is handled by the CreateEstimationDatasets.R script.
   - Revisions pushed to the develop branch. 
   - The package passes all the R tests but has a note that the package is larger than what CRAN accepts. That's due to the inclusion of the PUMS data used to estimate the models.
  - @Ben and others to test these modules using the new module testing capabilities offered by the visioneval package. 
    - In the 'tests' directory there are 3 folders:
      - 'defs' includes all the definition files required for the RVMPO test case
      - 'inputs' includes all the input files needed by the modules for the RVMPO test case
      - 'scripts' includes the test script. Running the script tests each module 

## visioneval framework
  - Brian added functions for implementing linear models, binary logit models, and binary search.
     - Writing these functions added some time, but they make module code more compact and understandable. In addition, they reduce a lot of redundant code in RSPM and should make transferal faster in the future.
  - Also modified the visioneval code to include units handling, as noted earlier.

## Documentation 
  - Brian made some updates to the 'model_system_design.md' documentation and pushed those to the develop branch, but there is still more to do.

## Next steps
  - @Brian plans to complete the next package which handles all the land use and system supply attributes
  - @Brian complete documentation updates
  - @Ben to test Brian's new modules, and merge to master if acceptable
