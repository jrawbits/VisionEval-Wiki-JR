This page describes the VE User Interface (including model runner and scenario viewer (visualizer of model results)). 
  - [#design-discussion]
  - [#specification]

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
    - Potential issue with reading VE's HDF5 datastore since HDF5 libraries are native
      - *Update: This [library](https://github.com/HDF-NI/hdf5.node) is the only HDF5 JavaScript library and it requires Node.js, which is basically a JavaScript web server, which is not easy to setup and maintain.  This likely prevents us from a client-side JavaScript-based solution.*
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
  - [x] Modular - the runner and visualizer are separate but they can cooperate.  VE models do not require the UI in order to be run.  In order to run a VE model from the UI, the user simply selects a modle run script.
  - [ ] GUI and the Scenario Viewer are one solution.  By using shiny, we will be able to implement the UI for running models with the scenario viewer (visualizer) for viewing the results of multiple model runs. 
  - [ ] Reads the VE settings files (geo.csv, model_parameters.json, run_parameters.json) and lets the user edit the files from the UI.
  - [ ] Reads multiple HDF5 output datastores in order to visualizer results across scenarios.  The user can select multiple HDF5 output datastores in the UI.
  - [ ] After selecting a VE model run script, it displays the VE modules to be run.  Once the model is running, it highlights which modules have been run, which is currently running, and what remains to be run.

## Required Revisions to the VE framework
