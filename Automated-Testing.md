## Tests
The VisionEval model system and design of the framework software incorporates a number of features that facilitate automated testing to assure that modules will work within the system. Perhaps the most significant feature is the ‘data typing’ system that requires modules to completely specify all data that the module handles in some fashion: as model inputs, as data fetched from the common datastore, and as data that is output to be saved in the common datastore. These data specifications establish ‘contracts’ that assure data consistency and the framework software includes a number of functions that use the specifications to check consistency. These functions help to ensure that modules will work properly together. 

Following are some of the checks that are done:
  - Input data are checked against input data specifications;
  - Input data geography is checked against specified model geography;
  - Module specifications are checked for correctness;
  - Module specifications for data to be fetched from the datastore are checked against the specifications for the data stored in the datastore; and,
  - Module outputs are checked for consistency with the module specifications for those outputs.

Because of these checks and related checks, it is possible to automate a number of tests that allow a module developer to test that their module (when supplied with suitable test inputs) will work in the VisionEval model system. These checks are carried out by the ‘testModule’ function. In addition, this test can be run automatically when the package is built, enabling the developer to check at built time that the module works and the correctness to be checked as when the package is added to the VisionEval repository.

The data specification system also enables a model to be thoroughly checked before it is run. This will greatly reduce, if not eliminate, model runtime crashes. This is done by the ‘initializeModel’ function. The function checks:

  - Whether all module packages are installed, those packages contain the identified modules, and all module specifications are correct (have required attributes);
  - Specified model geography and consistency of model inputs with the geography;
  - Whether model inputs are consistent with specifications; and,
  - Whether every module when it is called will have the data it needs to run (either in specified input files or the datastore) and whether the attributes of those data are consistent with the specifications for the module.

These checks that are built into the framework software make it possible to implement automated checking of VisionEval module packages and VisionEval model whenever a module package and/or model is added to or modified in the VisionEval repository. 

## UI Testing
VEGUI is tested using shinytest.

## Test System
[TravisCI](https://travis-ci.org/) services are used to automatically test all modules and models to assure that they work properly.  Here are a few details on the test system:
  - Tests automatically run with every commit and the pass/fail status is at the bottom of the README as [rendered by GitHub](https://github.com/gregorbj/VisionEval/tree/develop)
  - The current Travis build and test script is [here](https://github.com/gregorbj/VisionEval/blob/develop/.travis.yml), which includes all the steps to install, build, and run all the VE resources
  - The build logs, which are helpful when errors happen, are [here](https://travis-ci.org/gregorbj/VisionEval/builds/)