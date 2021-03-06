# Automated Test and Build System
  - Brian, RSG, and Liming @ PSU are working on integrated automatic testing of VisionEval
  - Will be using [TravisCI](https://travis-ci.org/), which integrated nicely with GitHub and R
  - Uses the testing capabilities Brian created
  - Will test every module, model, and the GUI with every commit to the repo
  - If all tests pass, then the changes can be merged to master

# Module Development
  - Brian developed the VETransportSupply package which adds metropolitan area public transit service and freeway lane-miles and transit accessibility measures (D4c from Smart Location Database).
  - The VERSPM has been updated to add in the VETransportSupply package modules.
  - Brian created the VE2001NHTS package which contains the augmented 2001 NHTS household dataset used for estimating models.
  - Liming has successfully run the modules he has created for ODOT's RSPM multimodal model research project with the other VE modules.

# Framework
  - Brian added dataset name registry and framework functions to interact with it. This will help with cataloging the names of datasets and that modules that produce them. An issue has been added to stimulate discussion on where VisionEval should go with this feature.
