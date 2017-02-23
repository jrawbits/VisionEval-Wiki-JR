# VisionEval

VisionEval is a programming framework for disaggregate strategic planning models.  Background information is available on the project [webpage](https://gregorbj.github.io/VisionEval/).  This site is focused on management of the collaborative effort.

###Modules & Packages 
Modules perform individual tasks and are the fundamental building blocks of VisionEval code (e.g., create households). They perform single or multiple (sub-module) functions.  Packages are logically related combinations of one or more modules organized into libraries, as a way to distribute the VisionEval code (e.g. HH synthesis including location, income, age, etc.). Each module is assigned to a package.

  - [Modules and Packages Table](Modules-and-Packages)

###Models
Models consist of a set sequence of modules called in a run script (e.g. RSPM, RPAT). A model is further customized for a local community by the set of data used from the datastore.
  - [RPAT](https://github.com/gregorbj/VisionEval/tree/master/sources/models/VERPAT)
  - RSPM

###Graphical User Interface and Scenario Viewer
A GUI and scenario viewer (outputs visualizer) that works for both the RPAT and RSPM models is being developed.  
  - [VEGUI](https://github.com/gregorbj/VisionEval/tree/master/sources/VEGUI)
  - [[Design | User-Interface-Design]]

### Outstanding Issues and Project Progress
The current VE todo list and overall project progress is being managed as [Issues](https://github.com/gregorbj/VisionEval/issues) and [Project Milestones](https://github.com/gregorbj/VisionEval/milestones).  
