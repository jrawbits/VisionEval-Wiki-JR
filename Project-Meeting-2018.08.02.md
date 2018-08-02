
## Project Management  / Pooled Funds Collaboration
  - We discussed ownership of VE resources now that WSP/CS will be the pooled funds contractor
  - A few ideas discussed include:
    - VisionEval.org continues to maintain a fork of the gregorbj version and WSP/CS forks off of the fork.  Both gregorbj/RSG and WSP/CS collaborate through the VisionEval.org fork.
    - Gregorbj transfers ownership to VisionEval.org and then gregorby forks back and WSP/CS fork off of VisionEval.org.  What does @Brian think?
    - Maybe VisionEval.org re-forks at the end of the AASHTO and ODOT contracts?
    - We'll cancel Liming's pull request and the Pooled Funds can coordinate with him 
  - I'm going to clean-up the gregorbj issues, wiki, etc. so it is focused on our scoped work.  This means closing non-scoped issues, revising the roadmap, etc.  --> this is largely done now
  - We should have a meeting with the development team ahead of the AMPO peer exchange so we instill confidence in the new pooled funds participants that we have a collective plan.
  - RSG is going to accept the pull request for the VE RPAT EV upgrades to the gregorbj project.  This way we can get all our stuff into one nice complete, tested, and documented effort.

## Multiple Scenarios and Visualizer
  - Added new [VEScenarios](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/modules/VEScenario) package under [add_scenario](https://github.com/gregorbj/VisionEval/tree/add_scenario) branch
  - Includes the following features:
    - multi-run / scenario builder
    - runs scenarios in parallel 
    - gathers results from the multiple scenarios
    - generates the [Visualizer](https://github.com/gregorbj/RPAT_Viewer_Pilot) output file
  - An example implementation for VERPAT is [here](https://github.com/gregorbj/VisionEval/tree/add_scenario/sources/models/VERPAT_Scenarios)
  - It is designed to also work for VERSPM
  - @Ben to test and @Aditya to revise as needed
  - We're planning to demo at the AMPO peer exchange
  - Next steps, see milestone [#17](https://github.com/gregorbj/VisionEval/milestone/17)
    - Revise VEGUI to support additional VEScenarios functionality
    - Wireframe revisions
    - Implement changes
    - Update documentation and draft tutorial

## VERSPM Documentation
  - @Brian working on completing the VERSPM documentation so he can branch it for VEState improvement