# Design Questions
  - Should we merge the GUI and the Scenario Viewer into one solution?  Hopefully yes.
  - It should reads various VE settings and config files (INP, GET, SET) to figure out what is in the model setup
  - It should reads the HDF5 output datastore
  - It should have a backend settings file so we can write a script to automate runs
  - Who will administer the GUI/Visualizer?  Who will develop and support it?  Probably modelers, not software developers.

# Example options to review and discuss
  - Client-side JavaScript such as [ABMVIZ](http://rsginc.github.io/ABMVIZ) and [RPAT Dashboard](http://gregorbj.github.io/RPAT_Viewer_Pilot/VizRPAT)
    - These are served by GitHub and read CSV files for data 
    - Potential issue with reading VE's HDF5 datastore since HDF5 libraries are native; need to first install this [library](https://github.com/HDF-NI/hdf5.node)
  - Client-side flexdashboard R package such as the [PART model dashboard](http://rsginc.github.io/part_model)
    - The user writes R code that gets converted to HTML/JavaScript at the end of a model run
    - See [here](http://rsginc.github.io/part_model/Modeling%20Knowledge%20Sharing%20--%20PART%20Dashboard.pptx) for more details
    - Maybe not sufficient technology for a GUI as well; can also make use of [R shiny](https://shiny.rstudio.com/), see below.
  - Server- and/or desktop-based such as the [FSDM GUI](https://github.com/gregorbj/FSDM_GUI/blob/master/documentation/FSDM_Users_Guide_20161116.docx) which uses [R shiny](https://shiny.rstudio.com/) and the existing [RPAT GUI](https://planningtools.transportation.org/files/63.pdf) which uses [CherryPy](http://cherrypy.org)
    - These are not very lightweight since they require running a web server, installing R, RStudio, Python, and dependent libraries, which often requires user admin rights.

# What's our vision for the GUI/Visualizer?
  - The scope says transfer the existing RPAT GUI but that probably is not the best choice for the long term VE project
  - I suggest we look into client-side web applications like R flexdashboard and maybe R shiny since VE is an R-based framework.

# Next steps
  - Decide on technology
  - Prototype a GUI/visualizer for running and visualizing the VE household and employment simulation models
