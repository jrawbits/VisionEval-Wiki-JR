# VERPAT 
  - Draft [Documentation of inputs and outputs](VERPAT-Inputs-and-Outputs) complete, @Ben to review
  - Made some revisions to the inputs and outputs as a result of documenting modules since there was some inconsistency in the way RunTypes are used throughout the model
  - Code changes pushed and @Ben to review

# VERSPM
  - All modules done and passing tests in a new branch, [rspm_complete](https://github.com/gregorbj/VisionEval/tree/rspm_complete)
  - Eliminated VECommercialTravel, VERoadPerformance, VEEnergyAndEmissions, and VETravelCosts, and replaced them with VEPowertrainsAndFuels and VETravelPerformance so still some work to do to merge to develop
  - @Brian working on memo on conversion and differences from RSPM as a sort of verification document
  - @Aditya to help with the merge next week

# Documentation
  - We need to start thinking about how to auto-generate documentation for modules
  - Maybe add a block of text at the top and then pull it out and create a Rmarkdown document? Similar to [roxygen](http://roxygen.org/)
  - For now, it's important to get the content written down.  We can work on the technology to auto-create things later.

# Test System and Setup
  - Updated [Getting Started](https://github.com/gregorbj/VisionEval/wiki/Getting-Started) to refer to a new install.R script
  - Need to note that installation takes a long time due to re-downloading the repo 
  - Tested triggering builds of dependent projects in TravisCI if we decide to eventually go with [separate repositories](https://github.com/gregorbj/VisionEval/issues/129)

# Usability Workshop
  - We need to get the usability workshop on the calendar; @Ben to follow-up with Kristen