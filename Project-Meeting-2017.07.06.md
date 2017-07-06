# Automated Testing and Building
  - We’re now automatically testing the framework, modules, and models using [Travis CI](https://travis-ci.org/)
  - Tests automatically run with every commit and the pass/fail status is at the bottom of the README as [rendered by GitHub](https://github.com/gregorbj/VisionEval/tree/develop)
  - The current Travis build and test script is [here](https://github.com/gregorbj/VisionEval/blob/develop/.travis.yml), which includes all the steps to install, build, and run all the VE resources
  - The build logs, which are helpful when errors happen, are [here](https://travis-ci.org/gregorbj/VisionEval/builds/)
  - Master (release) branch is now write protected and can only be written to by a pull request

# GUI
  - GUI broke with the latest revisions to the framework since we changed how the model state object is managed
  - Currently working on fixing this + an issue with parsing the model spec tree

# RSPM Translation
  - Lots of progress - income model re-estimated, multiple updates to supports Liming's model, land use package complete, 5D measures complete, transportation supply package complete, auto ownership model complete
  - All these improvements are in VERSPM now
  - Using RVMPO as the test
  - Needed to create some of the RVMPO test data as well, which took some time

# Framework
  - Created a [name registry](https://github.com/gregorbj/VisionEval/blob/develop/sources/modules/VENameRegistry.json) for managing module methods across packages

# Reviewing VE contributions
  - Josh wants to know what he should review
  - I reviewed the draft review team submittal requirements
    - Software – module, model, and/or user interface code
    - Tests – sufficient code coverage testing with an included example test data set
    - Documentation – both developer and end-user documentation
    - Methods – description of methods

# Next Steps
  - Once the GUI is working again, we're going to add automated testing of it as well
  - Next VERSPM package is probably autonomous vehicles and car sharing
  - Once everything is working and tested, we'll merge to master for a new release
