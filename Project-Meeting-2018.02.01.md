# Revised test system
  - The build process now runs in parallel (14 Linux VMs at once!) and avoids the timeout issues.  Check out the [Travis logs](https://travis-ci.org/gregorbj/VisionEval) for more information.
  - [Developer documentation](https://github.com/gregorbj/VisionEval/wiki/Automated-Testing#test-system) updated as well since adding new modules/models is much easier

# Next release
  - Now that develop is passing all tests, we can push to master (i.e. make a release of the software)
  - Brian updated the framework documentation recently so this would be good to share
  - Brian also added [code](https://github.com/gregorbj/VisionEval/tree/develop/sources/framework/function_docs) to automatically create the interactive framework API documentation 
  - We're going to wait until next week when the VERSPM Energy and Emissions and VERPAT congestion module should be done

# RPAT Conversion
  - Some questions about how to convert RPAT run types to VisionEval's framework of modules with a set of clearly defined inputs
  - Should congestion() be one module that is run twice with policy=N and policy=Y?
  - Or should it be separate modules (still in the same package) - Base Policy, Future Policy No, Future Policy Yes
  - Adi to discuss with Colin

| RunType | RunYear | Landuse | Supply | Policy |
| ------| ----- |- | --- | ----- |
| E	| 2010  | E (existing) | 	E| 	N| 
| EL ES NP| 2040	| E| 	E| 	N| 
| FL FS NP| 2040	| F (future) | 	F| 	N| 
| FL FS YP| 2040	| F| 	F| 	Y| 


 
