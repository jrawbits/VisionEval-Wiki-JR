Support for setting up and running multiple scenarios is inspired by the [RPAT_Viewer_Pilot](https://github.com/gregorbj/RPAT_Viewer_Pilot/blob/master/automating_rpat.md).  Much of the development related to this work is done under [this](https://github.com/gregorbj/VisionEval/milestone/17) milestone.

## Design
  - Add new [VEScenarios](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/modules/VEScenario) package that does the following:
    - multi-run / scenario builder
    - runs scenarios outside the GUI in parallel 
    - gathers results from the multiple scenarios
    - generates the [Visualizer](https://github.com/gregorbj/RPAT_Viewer_Pilot) output file
  - An example implementation for VERPAT will be [here](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/models/VERPAT_Scenarios)
  - It will be designed to also work for VERSPM

## Additional Revisions to VisionEval as a Result
  - Revise VEGUI to support additional VEScenarios functionality
  - Update documentation and draft tutorial