# VisionEval #
VisionEval (VE) is a model system and supporting software framework for building collaborative disaggregate strategic planning models. Background information is available on the project [webpage](https://gregorbj.github.io/VisionEval/) and project administration is available on the linked [wiki](https://github.com/gregorbj/VisionEval/wiki).

The VE software framework is written in the R programming language for statistical computing and graphics. The software framework is available as a R package, *visioneval*. The purpose of the model system and framework is to enable models be created in a plug-and-play fashion from modules that are also distributed as R packages. A simple R script is used to implement a model by initializing the model environment and then calling modules successively. This repository contains currently contains a demonstration module package and demonstration model script and associated resources. In the future, the repository will hold a number of working modules, model scripts, and resources that implement the GreenSTEP model and related strategic planning models.

This repository is organized into two directories:
- The **sources** directory contains four directories:
  - [visioneval framework](https://github.com/gregorbj/VisionEval/tree/master/sources/framework/visioneval) package
  - [VE modules](https://github.com/gregorbj/VisionEval/tree/master/sources/modules) such as VESimHouseholds and VESyntheticFirms
  - VE models such as the pilot version of [VERPAT](https://github.com/gregorbj/VisionEval/tree/master/sources/models/VERPAT)
  - [VE GUI](https://github.com/gregorbj/VisionEval/tree/master/sources/VEGUI) graphical user interface and scenario viewer / visualizer for running and viewing results of VE models
- The **api** directory contains documentation of the model system. The [model system design](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md) document is the most complete at the present time. VisionEval framework functions are documented in a [network visualization](https://gregorbj.github.io/VisionEval/website/visioneval_functions.html) of the functions and their call relationships. Functions are represented by network nodes. Call relationships are represented by arrows which point from the calling function to the called function. Function details are shown at the bottom of the page when a function node is selected.

# Getting Started

## Installation and Setup
  1. Install [R 3.3+](https://cran.r-project.org) in a location where you have write access.
  2. Start R
  3. If working within a proxy server (like ODOT), run the following commands to enable install from GitHub:
```
library(httr)
set_config(use_proxy(url="proxynew.odot.state.or.us", port=8080)) 
set_config( config( ssl_verifypeer = 0L ) )
```
  4. If working with an R install without write access to its library folder (like ODOT), first change your library location to a write accessible location.
  5. Run the following commands to download and install the required libraries and their dependencies:
```
install.packages(c("devtools", "roxygen2", "stringr", "knitr"))
install.packages(c("shiny", "shinyjs", "shinyFiles", "data.table", "DT", "shinyBS", "future", "testit", "jsonlite", "shinyAce", "envDocument", "rhandsontable"))
devtools::install_github(c("tdhock/namedCapture", "trestletech/shinyTree"))
devtools::install_bioc(c("BiocInstaller", "rhdf5"))
```
  6. Run the following commands to download and install the required VE framework package:
```
devtools::install_github("gregorbj/VisionEval/sources/framework/visioneval")
```
  7. Run the following commands to download and install the required VE modules for VERPAT:
```
#the following modules are required for the pilot VERPAT; others are required for VERSPM
devtools::install_github("gregorbj/VisionEval/sources/modules/VESyntheticFirms")
devtools::install_github("gregorbj/VisionEval/sources/modules/VESimHouseholds")
```

## Running the Pilot VE RPAT from within R
  1. Git clone (i.e. copy) this repository to your computer.
  2. Start R and run the following commands:

```
#point to the location of the cloned repository, not the location of the auto-installed R packages
full_path_to_VERPAT = "C:/projects/development/VisionEval/sources/models/VERPAT"
setwd(full_path_to_VERPAT)
source("run_model.R")
```

## Running the Pilot VE GUI to run Pilot VE RPAT
  1. Git Clone (i.e. copy) this repository to your computer.
  1. Start R and run the following commands:

```
library("shiny")
runGitHub("gregorbj/VisionEval", subdir="sources/VEGUI")
```
  3. The VE GUI should launch in your browser
  4. Click "Select Scenario Script" and navigate to the VERPAT run_model.R script in your local repository
  5. Click "Run" and then "Run Model Script" to run the VERPAT model

# Develop Branch

The current release version of VisionEval is on the master branch.  The current development version is on
the develop branch.  To download, install, and test the develop branch resources, do the following:
  1. Git clone (i.e. copy) the develop branch to your computer.  By default, Git will clone the master branch.  After cloning, switch to the develop branch.
  2. Run the same R commands above, except reference the develop branch, for example:
```
devtools::install_github("gregorbj/VisionEval/sources/framework/visioneval", ref="develop")
devtools::install_github("gregorbj/VisionEval/sources/modules/VESyntheticFirms", ref="develop")
devtools::install_github("gregorbj/VisionEval/sources/modules/VESimHouseholds", ref="develop")
runGitHub("gregorbj/VisionEval", subdir="sources/VEGUI", ref="develop")
```
  3. Navigate to and run both VERPAT and VERSPM's run_model.R script 

Ensure these operations complete successfully before finalizing commits to develop.

# Build Status 

[![Travis-CI Build Status](https://travis-ci.org/gregorbj/VisionEval.svg?branch=develop)](https://travis-ci.org/gregorbj/VisionEval)
