# Design
  - Merge the GUI and the Scenario Viewer into one solution
  - Reads various VE settings and config files (INP, GET, SET) to figure out what is in the model setup
  - Reads the HDF5 output datastore

# Technology
  - Entirely in javascript and served by GitHub pages
  - Uses [hdf5.node](https://github.com/HDF-NI/hdf5.node), which requires the HDF5 libraries to first be installed on the user's machine
  - Maybe use [Vega](https://vega.github.io/vega/) javascript library
  - Maybe use [shiny](https://shiny.rstudio.com/) instead

# Prototype
  - Setup and run with VE household and employment simulation models

# Batch running
  - GUI will have a backend settings file so we can write a script to automate runs