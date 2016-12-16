VisionEval Framework is a model system:
  - Modules perform individual tasks and are the fundamental building blocks of VisionEval code (e.g., create households). They perform single or multiple (sub-module) functions.
  - Packages are logically related combinations of one or more modules organized into libraries, as a way to distribute the VisionEval code (e.g. HH synthesis including location, income, age, etc.). Each module is assigned to a package. 
  - Run scripts call modules via the package, but only the module(s) called are run, not necessarily all modules in the package.
  - Models consist of a set sequence of modules called in a run script (e.g. RSPM, RPAT). A model is further customized for a local community by the set of data used from the datastore.
  - Datastore and Framework services support a running model
  - Consistent geography (explicit or synthesized) in all components allows modules/packages to be shared across models

Projects
  - [RPAT](https://github.com/RSGInc/VisionEvalRPAT)
  - RSPM
  - List of [Modules and Packages](Modules-and-Packages)