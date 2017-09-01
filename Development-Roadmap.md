This page maintains current, future, and wishlist related developments to the VisionEval model system.  The current set of work packages are:
  - [Setting Up VisionEval including VERSPM Migration](#setting-up-visioneval-including-verspm-migration) 
  - [Integrate PSU Multi-Modal model](#integrate-psu-multi-modal-model)
  - [VERPAT Migration](#verpat-migration)
  - [Upcoming](#Upcoming)

This page also maintains a set of wishlist/enhancements, which may overlap with the project [issues](https://github.com/gregorbj/VisionEval/issues).
  - [Wishlist](#wishlist)

## Setting Up VisionEval, including VERSPM Migration
This current work task is described in more detail [here](https://github.com/gregorbj/VisionEval/wiki/Modules-and-Packages)

## Integrate PSU Multi-Modal model
Replace VERSPM modules with PSU’s Multi-Modal model, including modules X, Y, and Z.  This model has a more rigorous output estimation of non-vehicle  travel (bike, walk, transit).  In the process, it improves the auto ownership module (important in car sharing and automated vehicle policies).  It also add household attributes  that can improve/be used by other  modules, including:
  - home location 5D built form variables (density, design, diversity, destination accessibility, distance to decent transit)
  - Number of workers

## VERPAT Migration 
The translation of RPAT to VERPAT still needs to be completed.  VERPAT will utilize and/or revise VE modules as needed.  For example:

  - household() will start from VESimHouseholds and VESyntheticFirms
  - urban() will start from VELandUse
  - accessibility() will start from VETransportSupply
  - vehicle() will start from VEVehicleOwnership
  - demand() will start from VETravelDemand
  - congestion() 
  - policy congestion()

## Upcoming
* Improve the graphic user interface and integrate the dashboard/visualizer
* Improve documentation

## Wishlist
* Safety and security: link policies to safety outcomes including ITS, autonomous vehicles, multimodal countermeasures
* Mobility: roadway and ITS mobility measure, better congestion model sensitive to network connectivity, local/long distance freight modules, roadway reliability 
* Accessibility and connectivity: impact of well-connected bike/walk network, transit-autonomous vehicle connections, expanded TDM programs, intercity commutes and distance to CBD, modules to address emerging modes
* Community and economic vitality: Research on economic growth outcomes and feedback, congestion pricing
* Land use: allow specific multimodal impacts based on built form, employment and work location attributes
* Equity: transit access, shared economic growth, affordable housing indicator, case studies of equity measures from existing outputs
* Environmental stewardship: availability of EV charging infrastructure
* Strategic investment and financial responsibility: improved cost accounting framework (life cycle cost, asset management, user cost by income, transit fares)
* Integration with other tools like TREDIS, ITHIM, land use sketch tools, input pre-processor (bike, ITS, TO)
* US/global comparisons for inputs
* Case studies of use of results
