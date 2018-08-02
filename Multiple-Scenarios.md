The design for support for setting up and running multiple scenarios is inspired by the [RPAT_Viewer_Pilot](https://github.com/gregorbj/RPAT_Viewer_Pilot/blob/master/automating_rpat.md)

## Multiple Scenarios and Visualizer
  - Added new [VEScenarios](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/modules/VEScenario) package under [add_scenario](https://github.com/gregorbj/VisionEval/tree/add_scenario) branch
  - Includes the following features:
    - multi-run / scenario builder
    - runs scenarios in parallel 
    - gathers results from the multiple scenarios
    - generates the [Visualizer](https://github.com/gregorbj/RPAT_Viewer_Pilot) output file
  - An example implementation for VERPAT is [here](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/models/VERPAT_Scenarios)
  - It is designed to also work for VERSPM

  - Next steps, see milestone [#17](https://github.com/gregorbj/VisionEval/milestone/17)
    - Revise VEGUI to support additional VEScenarios functionality
    - Wireframe revisions
    - Implement changes
    - Update documentation and draft tutorial