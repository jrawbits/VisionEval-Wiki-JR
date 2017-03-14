# What's our vision for the GUI/Visualizer?
  - The scope says transfer the [existing RPAT GUI](https://planningtools.transportation.org/files/63.pdf) (see below), but that is probably not the best choice for the long term VE project
  - I suggest we look into client-side web applications like R flexdashboard and maybe shiny (see below) since VE is an R-based framework.

# Design Questions / Requirements
  - We want to avoid desktop application issues such as admin rights, installers, etc.
  - We want it to be modular - the runner and visualizer are separate but they can cooperate
  - Should we merge the GUI and the Scenario Viewer into one solution?  Hopefully yes.
  - It should reads various VE settings and config files (INP, GET, SET) to figure out what is in the model setup
  - It should reads the HDF5 output datastore
  - It should have a backend settings file so we can write a script to automate runs
  - Who will administer the GUI/Visualizer?  Who will develop and support it?  Probably modelers, not software developers.
  - It will display the modules to be called by the models and their current status as the model runs

# Example options to review and discuss
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

# Next steps
  - Decide on technology -> the team agreed to look into R flexdashboard / shiny-based options
  - [Prototype a GUI/visualizer](https://github.com/gregorbj/VisionEval/issues/46) for running and visualizing the VE household and employment simulation models
  