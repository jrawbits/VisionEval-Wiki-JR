### Workflow
  - The master branch contains the latest working/release version of the VE resources
  - The master branch is write protected and can only be written to by a pull request
  - Work is done in the develop branch or an issue/feature branch off of develop
  - When an issue/feature is complete, it is merged into the develop branch
  - Committing to develop automatically runs the build and test system on [Travis CI](https://travis-ci.org/)
  - The framework, modules, models, and soon GUI are all always tested
  - After all tests pass and when deemed ready, a pull request is created to merge develop into master
  - The repository administrator handles the pull request and makes sure to also update related resources such as the wiki, documentation, issues, release notes, etc.

