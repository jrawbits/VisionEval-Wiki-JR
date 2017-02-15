## HH and employment pilot modules
  - @Brian revised a development version of the VisionEval package
    - Will post on GitHub once pilots are complete
  - Revised and tested the HouseholdSim package
  - Still working on the VisionEvalSyntheticFirms package
    - Needed to split VisionEvalSyntheticFirms into a base and future year module

## Work plan and early ideas for visualizer and GUI
  - Requirements / Questions
    - Should the GUI/Visualizer be one tool?  Hopefully yes.
    - Should the GUI/Visualizer be a desktop application, a client-side web application, or a server-based web application?  Hopefully a client-side web application since this means limited back-end administration
    - The GUI/Visualizer should get all its data from the VD HDF5 datastore
  - Example GUI/Visualizer options to review and discuss:
    - Client-side JavaScript such as [ABMVIZ](http://rsginc.github.io/ABMVIZ) and [RPAT Dashboard](http://gregorbj.github.io/RPAT_Viewer_Pilot/VizRPAT)
      - These are served by GitHub and read CSV files for data 
      - Potential issue with reading VE's HDF5 datastore since HDF5 libraries are native to the OS; this [library](https://github.com/HDF-NI/hdf5.node) may solve this problem
    - Client-side flexdashboard R package such as the [PART model dashboard](http://rsginc.github.io/part_model)
      - Is run at the end of a model run; write R code that gets converted to HTML/JavaScript; see [here](http://rsginc.github.io/part_model/Modeling%20Knowledge%20Sharing%20--%20PART%20Dashboard.pptx) for more details
      - Maybe not sufficient technology for a GUI as well; can also make use of [R shiny](https://shiny.rstudio.com/), see below.
    - Server- and/or desktop-based such as the [FSDM GUI](https://github.com/gregorbj/FSDM_GUI/blob/master/documentation/FSDM_Users_Guide_20161116.docx) which uses [R shiny](https://shiny.rstudio.com/) and the existing [RPAT GUI](https://planningtools.transportation.org/files/63.pdf) which uses [CherryPy](http://cherrypy.org)
      - These are not very lightweight since they require running a web server, installing R, RStudio, Python, and dependent libraries, which often requires user admin rights.
   - What's our vision for the VE GUI/Visualizer?
      - The scope says transfer the existing RPAT GUI (CherryPy) but that probably isn't the best choice for the long term future of VisionEval
      - I suggest we look into client-side web applications like R flexdashboard

## Proposed revision to work plan
  - RSG has spent about XXXXX of its budget
  - OSA has spent about XXXXX of its budget
  - Let's figure out a GUI/Visualizer plan and then discuss remaining work/budgeting
