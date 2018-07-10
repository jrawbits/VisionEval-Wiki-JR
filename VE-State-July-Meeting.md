  - Date: July 5, 2018
  - Participants: Brian G, Brian H, Jana, Jeremy, John, Tara, Charles, Ben
  - Next meeting: October 3rd

## Questions from Kickoff
  - Using Synthetic population sensitivities/differences by region
    - You could skip some of the synthetic population parts of VE and instead use your own pop syn, provided it produces the requires household and person attributes.  For example, BMC could create a VEPopGenImporter module.  This may be done in Oregon as well for some of the models.
  - Like to improve sensitivities of auto ownership model
    - There are more auto ownership / income sensitivities in the model as compared to EERPAT
    - The model operates at geographies finer than counties
    - Can adjust driving licensing rates
    - You could also skip some of the auto ownership pats of VE and instead use your own auto own module, provided in produces the required attributes, including vehicle type and powertrains
    - May want to better separate households auto ownership attributes from vehicle attributes for more modular use
 - Setting up a Washington state model for pilot testing
    - based on Oregon example
    - need a good description of the required inputs

## VE zone system recap
  - Region - whole model area
  - Azone (district groups of BZones in VE-RSPM, e.g., jurisdiction, County in VE-State)
  - Bzone (BlockGroup in VE-RSPM, Synthetic aspatial BlockGroup in VE-State)
  - MArea - Metropolitan area overlay, grouping of Bzones 

## Basic Plan
  - From VERSPM (which operates at Bzone) to VEState (also Bzone, but aspatial, synthesized)
    - From MArea to Azones (county)
    - From Azones (districts) to Bzones (block groups)
    - New SimHHs module will put households into aspatial simBzones 
    - Add LandUse package to SimLandUse package, which will create synthetic bzones with land use attributes
    - VERSPM needs Bzone inputs, but that's too much detail at a state level
    - So VEState will operate at the Bzone level, but with synthesized Bzones based on Azone and MArea inputs

## Work Tasks
  - 1 - Test VERSPM with multiple MAreas and Azones to ensure existing software will work.
    - Will duplicate the 1 existing VERSPM example MArea
    - Basically double the region, as opposed to split all inputs into two halves, since this is easier
  - 2 - Develop the synthetic Bzone generator
  - 3 - Create the full set of VEState inputs and test

## RSPM LandUse steps to Synthesize
  - Predict Housing
  - Locate Employment
  - Assign Development Types
  - Calculate 4Ds
  - Calculate Urban Mix Measures
  - Assign Parking Restrictions
  - Assign Demand Management programs
  - Assign Car Service Availability
  - See [Brian's slides](https://github.com/gregorbj/VisionEval/wiki/documents/VE-STATE_Mtg2_final_20180705.pdf) for details about each step

## Bzone Attributes to Synthesize BZones
  - Destination access, number of hhs, hhs by type, number of jobs by sector, place types (like development types in GreenSTEP, but plan to use RPAT-like types based on area type and development type), 
  - Plan to use EPA SLD at block group level for 2010 to develop the various models/relationships
  - Expect some new AZone, MArea inputs as well. Use defaults, best practice methods, to keep as manageable as possible.  

## Discussion
  - Will create a new branch off of develop in the repository called VEState
  - Need a flow chart of model steps and a detailed description of all inputs, preferably for the next meeting
  - Default values will be important to minimized complexity in getting the model up and running for other states
  - Using the [EPA SLD](https://www.epa.gov/smartgrowth/smart-location-mapping#SLD) as the primary data source is great since it is available to everyone
  - Brian to get into the work and share progress, enable e-review, ahead of the October meeting
  - Post October meeting, "real world" Test of the pilot tool and report at December meeting