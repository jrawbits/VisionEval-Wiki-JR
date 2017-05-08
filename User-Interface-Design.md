The VE User Interface, which includes the model runner and scenario viewer/visualizer, is described here.
  - [Design Discussion](#design-discussion)
  - [Specification](#specification)
  - [Scenario Viewer](#scenario-viewer)

# Design Discussion

## What's our vision for the GUI/Visualizer?
  - Transferring the [existing RPAT GUI](https://planningtools.transportation.org/files/63.pdf) (see below) is scoped, but this is probably not the best choice for the long term VE project since it uses technology that is unlikely to be maintained by the VE community into the future.
  - I suggest we look into client-side web applications like R flexdashboard and maybe shiny (see below) since VE is an R-based framework.

## Design Questions / Requirements
  - We want to avoid desktop application issues such as admin rights, installers, etc.
  - We want it to be modular - the runner and visualizer are separate but they can cooperate
  - Should we merge the GUI and the Scenario Viewer into one solution?  Hopefully yes.
  - It should reads various VE settings and config files (such as the INP, GET, SET lists) to figure out what is in the model setup
  - It should reads the HDF5 output datastore
  - It should have a backend settings file so we can write a script to automate runs
  - It will display the modules to be called by the models and their current status as the model runs
  - Who will administer the GUI/Visualizer?  Who will develop and support it?  Probably modelers, not software developers.

## Example options to review and discuss
  - Client-side JavaScript such as [ABMVIZ](http://rsginc.github.io/ABMVIZ) and [RPAT Dashboard](http://gregorbj.github.io/RPAT_Viewer_Pilot/VizRPAT)
    - These are served by GitHub and read CSV files for data 
    - Potential issue with reading VE's HDF5 datastore since HDF5 libraries are native.  *Update: This [library](https://github.com/HDF-NI/hdf5.node) is the only HDF5 JavaScript library and it requires Node.js, which is basically a JavaScript web server, which is not easy to setup and maintain.  This likely prevents us from a client-side JavaScript-based solution.*
  - Client-side flexdashboard R package such as the [PART model dashboard](http://rsginc.github.io/part_model)
    - The user writes R code that gets converted to HTML/JavaScript at the end of a model run
    - See [here](http://rsginc.github.io/part_model/Modeling%20Knowledge%20Sharing%20--%20PART%20Dashboard.pptx) for more details
    - Maybe not sufficient technology for a GUI as well; can also make use of [R shiny](https://shiny.rstudio.com/), see below.
   - Brian ran into memory problems running it on his 4GB laptop
  - Server- and/or desktop-based such as the [FSDM GUI](https://github.com/gregorbj/FSDM_GUI/blob/master/documentation/FSDM_Users_Guide_20161116.docx) which uses [R shiny](https://shiny.rstudio.com/) and the existing [RPAT GUI](https://planningtools.transportation.org/files/63.pdf) which uses [CherryPy](http://cherrypy.org)
    - These are not very lightweight since they require running a web server, installing R, Python, and dependent libraries, which often requires user admin rights.
    - *Update: R shiny is fairly easy to install and update and therefore makes for a reasonable technology for the VE UI.*

## Next steps
  - Decide on technology -> the team agreed to look into R flexdashboard / shiny-based options
  - [Prototype a GUI/visualizer](https://github.com/gregorbj/VisionEval/issues/46) for running and visualizing the VE household and employment simulation models
  
# Specification
The VE UI lives [here](https://github.com/gregorbj/VisionEval/tree/master/sources/VEGUI) and is implemented with R shiny.

## Requirements
  - [x] Avoid desktop application issues such as admin rights, installers, etc.  This requirement is satisfied by using R shiny, R commands to download and install required R software, and including clear instructions in the various READMEs in the repo.
  - [x] Modular - the runner and visualizer are separate but they can cooperate.  VE models do not require the UI in order to be run.  In order to run a VE model from the UI, the user simply selects a model run script.  Cooperation is handled through the requirement to display module status (see below).
  - [ ] GUI and Scenario Viewer are one solution.  By using shiny, we will be able to implement the UI for running models and the scenario viewer (visualizer) for viewing the results of multiple model runs. 
  - [ ] Reads the VE settings files (geo.csv, model_parameters.json, run_parameters.json) and lets the user edit the files from the UI.  See [#60](https://github.com/gregorbj/VisionEval/issues/60)
  - [ ] Reads any CSV input files in the inputs folder and lets the user edit the files from the UI.  See [#61](https://github.com/gregorbj/VisionEval/issues/61)
  - [ ] Reads HDF5 output datastores from multiple runs in order to visualizer results across scenarios.  The user can select multiple HDF5 output datastores in the UI.  See [#62](https://github.com/gregorbj/VisionEval/issues/62)
  - [x] Update UI with running module status.  After selecting a VE model run script, the UI displays the VE modules to be run.  Once the model is running, it highlights which modules have been run, which module is currently running, and what modules still need to be run.  See [#63](https://github.com/gregorbj/VisionEval/issues/63)
  - [x] Copy a scenario.  After selecting a run model script, the complete scenario folder setup is copied to a new folder named by the user.  See [#64](https://github.com/gregorbj/VisionEval/issues/64)

## Revisions required to the VE framework
In order for the UI and a VE model to cooperate about the module run state, the following change will be made to the visioneval framework.  The ModelState list will be kept in the Global namespace at all times so the UI and the model run script can share it.  The ModelState list now includes the results of the `parseModelScript` function call in the `initializeModel` function, which parses the model script and creates a table of module calls in the order they are called.  The `runModule` function is updated to set the status of each module in the module table as the model runs.  Example valid status values are: "planned", "running", "complete".  This shared data structure is used to update the UI with the status of the running modules.  See [#65](https://github.com/gregorbj/VisionEval/issues/65)

# Scenario Viewer
The existing [RPAT Viewer Pilot](https://github.com/gregorbj/RPAT_Viewer_Pilot) is going to be integrated into the VE GUI.  It is implemented in JavaScript and can likely be integrated into the existing RShiny VEGUI without being significantly re-written.  The scenario viewer currently takes as input a CSV file of performance measures by scenario.  This will need to be created ahead of running the viewer.  Therefore, the current work tasks for integrating the scenario viewer into the VEGUI is:
  - Add the ability to select a folder for VEGUI to recursively search for VE HDF5 output files.  See [#96](https://github.com/gregorbj/VisionEval/issues/96)
  - Add the ability to select the performance measure R script that reads the VE HDF5 output file and produces the performance measures for each scenario. See [#96](https://github.com/gregorbj/VisionEval/issues/96)
  - Integrate the RPAT Viewer Pilot into the existing VEGUI RShiny application. See [#97](https://github.com/gregorbj/VisionEval/issues/97)
