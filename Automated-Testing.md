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
VEGUI is an application that allows a user to run various VisionEval models. VEGUI is tested using shinytest to ensure its functionality and its usability. Multiple test scripts are written to test different functionalities. Following is a list of tests currently implemented:
- [open_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/tests/opentest.R): Checks if VEGUI opens and closes without any glitch,
- [run_verpat_model_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/tests/run_verpat_model_test.R): Checks if VEGUI opens, runs a VERPAT model, collects all the results, and closes properly.

A test requires a set of expected results (images or json) to make comparisons and draw conclusions. A test is successful if it finishes. A failed test will prompt the user with the differences compared to the expected results.
The main test script [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R) serves has a host and makes call to all the aforementioned tests.

The following steps describe a process to create a new test and/or the expected results:
 - Use [test_template](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/tests/test_template.R) as a template to write your own script;
 - Set the parameter `createExpectedResults` in the main test script [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R) to TRUE (this will allow a user to create a new set of expected results);
 - Source the new test script in [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R);
 - Run [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R) to save the expected results;
 - Set the parameter `createExpectedResults` in the main test script [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R) to FALSE;
 - Run [run_vegui_test](https://github.com/gregorbj/VisionEval/blob/develop/sources/VEGUI/run_vegui_test.R) to ensure that the test finishes successfully.

## Test System
[TravisCI](https://travis-ci.org/) services are used to automatically test all modules and models to assure that they work properly.  Here are a few details on the test system:
  - Tests automatically run with every commit and the pass/fail status is at the bottom of the README as [rendered by GitHub](https://github.com/gregorbj/VisionEval/tree/develop)
  - The current Travis build and test script is [here](https://github.com/gregorbj/VisionEval/blob/develop/.travis.yml), which includes all the steps to install, build, and run all the VE resources.  To add a new module or model, add an additional line to the `env` property for the module or model.  This will result in an additional parallel build process using Travis' [build matrix](https://docs.travis-ci.com/user/customizing-the-build/#Build-Matrix).  The environment variables are:
    - FOLDER=sources/modules/VELandUse (folder location relative to the root; note framework, modules, and models are fixed)
    - SCRIPT=tests/scripts/test.R (test script to run, which is required by the VisionEval specification)
    - TYPE=module (either module or model)
    - DEPENDS=VE2001NHTS,VESimHouseholds (list of packages required to run this module or model)
  - The build logs, which are helpful when errors happen, are [here](https://travis-ci.org/gregorbj/VisionEval/builds/)