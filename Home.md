# VisionEval

VisionEval is a programming framework for disaggregate strategic planning models.  Background information is available on the project [Website](https://gregorbj.github.io/VisionEval/), including the [System Design](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md).  This site is focused on management of the collaborative effort.  

### Getting Started
Start with the [[Getting Started|Getting-Started]] page, the description of the [[VE Models|VisionEval-Models]], the [[VERPAT Tutorial|VERPAT-Tutorial-Overview]], and the [[Developer Orientation|Developer-Orientation]] page.

### Contributions
When considering contributing to VisionEval, start by reviewing the [Goals and Objectives](Goals-and-Objectives-of-VisionEval-Model-System) page and the [Contribution Review Criteria](https://github.com/gregorbj/VisionEval/wiki/Contribution-Review-Criteria).  In addition, the [Working Together](Working-Together) page describes how we use version control and our test system, and the [Automated Testing](Automated-Testing) describes our test setup in more detail. Our [Development Roadmap](Development-Roadmap) should also be reviewed. 
Contributions are currently being reviewed by the [[Pilot Review Team|Review-Team-Charter]].

### Modules & Packages 
Modules perform individual tasks and are the fundamental building blocks of VisionEval code (e.g., create households). They perform single or multiple (sub-module) functions.  Packages are logically related combinations of one or more modules organized into libraries, as a way to distribute the VisionEval code (e.g. HH synthesis including location, income, age, etc.). Each module is assigned to a package.

  - [Modules and Packages](Modules-and-Packages)

### Models
Models consist of a set sequence of modules called in a run script (e.g. RSPM, RPAT). A model is further customized for a local community by the set of data used from the datastore.
  - [RPAT](https://github.com/gregorbj/VisionEval/tree/master/sources/models/VERPAT)
  - [RSPM](https://github.com/gregorbj/VisionEval/tree/master/sources/models/VERSPM)

### Graphical User Interface and Scenario Viewer
A GUI and scenario viewer (outputs visualizer) that works for both the RPAT and RSPM models is being developed and integrated.  The GUI and scenario viewer support setting up, running, and viewing multiple scenarios.
  - [VEGUI](https://github.com/gregorbj/VisionEval/tree/master/sources/VEGUI)
  - [Multiple Scenarios + Scenario Viewer](https://github.com/gregorbj/VisionEval/wiki/Multiple-Scenarios)

### Outstanding Issues and Project Progress
The current list of VisionEval todos, feature requests, known issues, etc. is being managed as [Issues](https://github.com/gregorbj/VisionEval/issues) within [Project Milestones](https://github.com/gregorbj/VisionEval/milestones).  The [Meeting Notes](Meeting-Notes) are also a useful resource.  
