  - Date: July 5, 2018
  - Participants: Brian G, Brian H, Jana, Jeremy, John, Tara, Charles, Ben
  - Next meeting: October 3rd

## Questions
  - Synthetic population
    - You could skip some of the synthetic population parts of VE and instead use your own pop syn, provided it produces the requires household and person attributes.  For example, BMC could create a VEPopGenImporter module.  This may be done in Oregon as well for some of the models.
  - Need to improve sensitivities of auto ownership model
   - There are more auto ownership / income sensitivities in the model as compared to EERPAT
   - The model operates at geographies finer than counties
   - Can adjust driving licensing rates
   - You could also skip some of the auto ownership pats of VE and instead use your own auto own module, provided in produces the required attributes, including vehicle type and powertrains
   - May want to better separate households auto ownership attributes from vehicle attributes for more modular use
 - Setting up a Washington state model
   - based on Oregon example
   - need a good description of the required inputs

## VE zone system recap
  - Region - whole model area
  - Azone (like a TAZ)
  - Bzone (like a MAZ/parcel)
  - MArea - groups of zones (like a district)

## Basic Plan
  - From VERSPM (which operates at bzone) to VEState (also bzone, but synthesized)
    - From MArea to Azones (county)
    - From Azones (districts) to Bzones (block groups)
    - SimHHs module will put households into bzones
    - From LandUse package to SimLandUse package
      - will create synthetic bzones with land use attributes
    - VERSPM needs bzone inputs, but that's too much detail at a state level
    - So VEState will operate at the bzone level, but with synthesized bzones based on Azone and MArea inputs

## Work Tasks
  - 1 - Test VERSPM with multiple MAreas and Azones by duplicating the 1 existing VERSPM example MArea (basically double the region, as opposed to split all inputs into two halves)
  - 2 - Develop the synthetic zone generator
  - 3 - Create the full set of VEState inputs and test

## RSPM LandUse steps to Synthesize
  - Predict Housing
  - Locate Employment
  - Assign Development Types
  - Calculate 4Ds
  - Calculate Urban Mix Measures
  - Assign Parking Restrictions
  - Assign Demand Management
  - Assign Car Service Availability
  - See Brian's slides for details about each step

## Bzone Attributes to Synthesize
  - Destination access, number of hhs, hhs by type, number of jobs by sector, place types (like development types in GreenSTEP, but plan to use RPAT-like types based on area type and development type), 

## Estimation
  - Plan to use EPA SLD at block group level for 2010

## Questions
  - Will create a new branch off of develop in the repository called VEState
  - Need a flow chart of model steps and a detailed description of all inputs
  - Default values will be important to get the model up and running for other states
  - Using the EPA SLD as the primary data source is great since it is available to everyone