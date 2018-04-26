## Branches
  - The master branch contains the latest release version of the VE resources
  - Work is done in the develop branch or an issue/feature branch off of develop
  - The gh-pages branch contains only the [website](https://gregorbj.github.io/VisionEval) resources

## Master, Develop Workflow
  - The master branch is write protected and can only be written to by a pull request
  - Work is done in the develop branch or an issue/feature branch off of develop
  - When an issue/feature is complete, it is merged into the develop branch
  - Committing to develop automatically runs the build and test system on Travis CI
  - The framework, modules, models, and GUI are all always tested, as described [here](https://github.com/gregorbj/VisionEval/wiki/Automated-Testing)
  - After all tests pass and when the contribution is deemed ready, a pull request is created to merge develop into master
  - The repository administrator handles the pull request and makes sure to also update related resources such as the wiki, documentation, issues, release notes, etc.

## Website Workflow
  - The [website](https://gregorbj.github.io/VisionEval) is on the gh-pages branch so it is rendered by GitHub instead of being displayed in raw form
  - This branch is not tested and updated separately from the core (master, develop) resources
  - Eventually we may update the Travis build process to (test) and push the website off of develop, but for now they are just separate