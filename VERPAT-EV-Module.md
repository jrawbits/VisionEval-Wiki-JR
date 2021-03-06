The current version of VERPAT does not model electric vehicles (EVs).  Since EVs produce less local GHG than internal combustion engines, and policies related to EV usage are expected to impact the share of EVs on the road, it is important to add EVs to VERPAT.  This addition to VERPAT is inspired by how [GreenSTEP](https://github.com/gregorbj/GreenSTEP/blob/master/Documentation/GreenSTEP-RSPM_Documentation_20151220.docx) models EVs.

The plan to add EV support to VERPAT is to revise the following packages/modules in a fork: 
  - Revise VEHouseholdTravel :heavy_check_mark:
    - Revise CalculateTravelDemand module to identify HEV/PHEVs 
    - Revise CalculateTravelDemand module to identify DVMT by EVs 
  - Revise VETransportSupplyUse :heavy_check_mark:
    - Revise CalculateCongestionBase module to identify fuel efficiency, speeds, delays for EVs by functional class
  - Revise VEHouseholdTravel :heavy_check_mark:
    - Revise CalculateTravelDemandFuture module to identify HEV/PHEVs for future scenarios
    - Revise CalculateTravelDemandFuture module to identify DVMT by EVs for future scenarios
  - Revise VEHouseholdTravel :heavy_check_mark:
    - Revise CalculateInducedDemand module to adjust DVMT by EVs
  - Revise VETransportSupplyUse :heavy_check_mark:
    - Revise CalculateCongestionFuture module to identify fuel efficiency, speeds, delays for EVs by functional class for future scenarios
  - Revise VEHouseholdTravel :heavy_check_mark:
    - Revise CalculatePolicyVmt module to adjust DVMT by EVs by policy
  - Revise VEReports :heavy_check_mark:
    - Revise ReportRPATMetrics module to calculate metrics for EV

The existing VESimHouseholds, VESyntheticFirms, VELandUse, and VETransportSupply modules are unchanged.

Once the new forked version of VERPAT is complete, we will review the implementation and consider if we should revise it so  it can be run with or without EV.  


