## Contribution Review Criteria
Following are a number of potential module review criteria that are related to the listed objectives:
  - Does it contain all the elements that are required by the VisionEval system specifications?
  - Does it include test data?
  - Does it pass the ‘testModule’ test which validates that it will run correctly in the model system?
  - Does it include regression tests to enable checking that consistent results will be returned when updates are made to the framework and/or R programming environment?
  - Does it only interact with the computing environment by returning a properly structured list to the framework: i.e. does not modify the global environment, does not read or write files (except by calling the ‘writeLog’ function), and only calls framework functions that are allowed?
  - Does it includes all source files and data?  If a contributed module does not include all source data, either because of file size or confidentiality, it should include a minimal example data file for testing and so it is clear what data structure is needed to run the module.  It should also include clear instructions on how to fetch the large public data and/or a clear explanation of why non-included data is confidential and contact information for data owners.
  - Is it licensed with the VisionEval [license](https://github.com/gregorbj/VisionEval/blob/master/LICENSE) that allows the code to be freely distributed and modified and includes attribution so that the ‘provenance’ of the code can be tracked?
  - Is it based on geographic definitions that are consistent with the model system definitions?
  - If the module allows the estimation of regional parameters, does it provide default data, does it have clear documentation of what the estimation data needs to be and how it is to be formatted, and does it include proper data specifications to ensure that the user’s input data are correct?
  - Does the module compute quickly enough (NOTE: need to talk about how to review this)?
  - Is the module documentation complete? Does it include documentation of model estimation, algorithms, and instructions for using?
  - Does the module only call R code and packages that work on all operating systems? If the code includes any non-R code (e.g. FORTRAN, C++) will that code compile on all operating systems?
