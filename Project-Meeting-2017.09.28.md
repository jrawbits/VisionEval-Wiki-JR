## Repository transfer to Pooled Funds
  - Pooled funds group starts mid October and RFP expected mid Nov
  - Need to transfer repo See issues [#44](https://github.com/gregorbj/VisionEval/issues/44) before RFP released, so within ~6 weeks
  - @Ben to setup a meeting the week of Oct 23rd with the AASHTO and ODOT projects so we can discuss timing and approach
  - We're thinking of transferring ownership and then forking back to the repos we're currently working in for the existing AASHTO and ODOT projects
  - We're thinking we won't tackle splitting things out into separate repos until after the pooled funds gets up and running (https://github.com/gregorbj/VisionEval/issues/129)
  - Work flow will likely be similar: transferred VE repo for distribution (i.e. release), a separate branch/repo for development , and forks for development (off the development branch)

## Automated GUI testing
  - VE GUI automatic testing is now working [#108](https://github.com/gregorbj/VisionEval/issues/108)
  - It runs the VERPAT demo and makes sure it completes
  - Currently working on better documentation for the VEGUI code and the wiki related to test setup

## R binary files in addition to HDF5
  - See [#131](https://github.com/gregorbj/VisionEval/issues/131)
  - Code is working in a separate branch
  - Need to update VEGUI code, which we can do under the amendment
  - Workflow is Brian creates fork and turns off VEGUI test so he can test his revisions.  Then he pushes a new branch to the master repo.  Next RSG pulls the new branch, updates the VEGUI code and test and turns the test back on.  RSG pushes to the master repo and merges to development.  Once all tests pass, development is merged to master.

## Description attribute
  - See [#122](https://github.com/gregorbj/VisionEval/issues/122)
  - VERSPM modules updated to implement new requirements
  - @Brian to update VERPAT modules as well so the revisions will pass all the tests

## Call modules from other modules
  - See [#132](https://github.com/gregorbj/VisionEval/issues/132)
  - CALL spec essentially overloads a function call with a different GET list of inputs
  - @Brian to add example to the issue since I had some questions about whether to "merge" or just "replace" the GET list of inputs
