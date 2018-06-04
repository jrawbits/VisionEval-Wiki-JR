## Overview of deliverables, initial plan, and requirements discussion – 9 to 10 – Ben
  - Deliverables: 
    - Documentation of this workshop’s findings and recommendations for implementation
    - Updates to the user interface for configuring, running, and visualizing multiple scenarios at once
      - How do we specify which inputs can be systematically varied in the VE framework and exposed in the UI?
      - How do we communicate within VE model runs in a more programmatic manner than a log file so we can inform the user of progress?
      - How do we understand and query multiple runs from within the UI?
    - Integrated documentation and tutorials (share RPAT TravelWorks Workshop.pdf as prior example)
      - Integrated and hidable getting started or separate (Rmarkdown?)? 
  - Requirements:
    - Some of these are in the [backlog](https://github.com/gregorbj/VisionEval/milestone/17)
    - For beginning VisionEval users with little R experience, [86](https://github.com/gregorbj/VisionEval/issues/86), [99](https://github.com/gregorbj/VisionEval/issues/99), 
    - An RShiny-based solution that works with any VE model and can be maintained by modelers with strong R programming skills 
    - Provides multiple scenario visualization capabilities, [98](https://github.com/gregorbj/VisionEval/issues/98), [97](https://github.com/gregorbj/VisionEval/issues/97), [96](https://github.com/gregorbj/VisionEval/issues/96)
    - Integrated documentation and tutorials, [159](https://github.com/gregorbj/VisionEval/issues/159)
    - Tested and versioned
    - In addition to running locally, also run on the cloud – visioneval.org/demo for example?
    - Implements a clean interface between the R models and the GUI runner + visualizer, [91](https://github.com/gregorbj/VisionEval/issues/91), [154](https://github.com/gregorbj/VisionEval/issues/154)
      - HTTP messages, start+stop text files, etc?
  - Questions: 
    - What’s the relative importance of aesthetics versus features?  i.e. how much budget should we spend on the look of the software? 
    - Can we build an online demo version that runs the test model?  This could be really useful for beginners and for marketing/outreach.
    - Others?

## Review of inspirational examples – 10 to 12
  - Select sites from showmeshiny – 10 to 10:30 - Ben 
    - http://shinyprognostics.de/pemDemo/
    - https://johnyagecic.shinyapps.io/ManningsMC/
    - http://www.mephistosoftware.com/shiny/401k_simulator/
    - https://cawthron.shinyapps.io/BMOP/
    - https://compassnz.shinyapps.io/NZIPR/
    - http://www.shinyapps.io/ (for a cloud-based demo)
  - Input documentation management and ODOT SARSPM - 10:30 to 11 - Tara
  - [TF Guide](https://rguide.rsginc.com) (Method Selection for Travel Forecasting) GUI with Wizard, and NCHRP Report 852 - 11 to 11:30 – Kevin 
  - [FSDM](https://github.com/gregorbj/FSDM) RShiny user interface – 11:30 to 12 – Brian  

## Finalizing the plan –  12 to 1 – Ben 
  - What’s our recommendation for implementation?
    - UI design
    - UI model interface
    - Documentation integration
  - What are the most important next steps?
  - How do we parse our plan into agile iterations of improvements to a working user interface?
  - Who will test the user interface and provide feedback?
