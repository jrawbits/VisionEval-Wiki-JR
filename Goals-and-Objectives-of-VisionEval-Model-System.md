This page reiterates the primary goal and objectives of the model system to establish the context for review and acceptance, as described in the [Contribution Review Criteria](https://github.com/gregorbj/VisionEval/wiki/Contribution-Review-Criteria)

## Goals and Objectives
The primary goal of VisionEval is to create a model system which enables sharing and collaboration in the development of model components (aka modules) that can be easily combined together to build strategic planning models. The design objectives of the model system are:
  - Strategic Planning Models: Federal direction has challenged state, regional, and local transportation agencies with measuring the outcomes of decisions through performance-based planning, including considering how transportation solutions may impact future goals such as sustainability, health, mobility, etc. VisionEval is an open source common framework building on the successful GreenSTEP family of tools that is intended to address these needs.
  - Modularity: The model system enables new capabilities to be added in a “plug-and-play” fashion so models can be improved and extended and so improvements developed for one model can be easily shared with other models.
  - Loose Coupling: Modules operate independently from one-another, only communicating through passing of data to and from a common datastore. Modules are like pure functions, they do not change anything, and they just take data, do their computations, and then return the result.
  - Openness: Modules are developed to be completely open. All module code, parameters, data, and specifications are open to inspection and licensed to allow users to use, modify, and redistribute them as they see fit.
  - Geographic Scalability: The model system enables models to be applied at a variety of geographic scales (e.g. metropolitan, state) but share common geographic definitions to enable modules to be more readily shared between different model scales.
  - Data Accessibility: Model results are saved in a datastore that is easy to query. Results can be filtered, aggregated, and post-processed to compute desired performance measures.
  - Regionalization: Where necessary, modules will have built in capabilities for estimating and calibrating sub-model parameters from regional data for easy customization to local area.
  - Speed: Modules will run quickly so that models can be run in a practical manner large numbers of times to effectively explore a large strategic planning decision space.
  - Pre-emptive Error Checking: The model system will incorporate extensive checking to clearly identify errors in the model setup and inputs before the model is run to minimize runtime errors.
  - Documentation: Modules will include complete documentation so that they may be reviewed and understood by others. The calculations for estimating a module’s parameters will be included with the module.
  - Operating System Independence: The model system should run on any of the 3 major operating systems; Windows, Apple, or Linux.

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
