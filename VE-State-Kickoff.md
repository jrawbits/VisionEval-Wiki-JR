MEETING DATE:	Wednesday, May 31
MEETING TIME:	11:00-12:30 p.m. pacific
LOCATION:	Call in/Skype

## Attendees
Project & Oversight team members:
  - Tara Weidner, ODOT
  - Brian Gregor, OSA
  - Ben Stabler, RSG
  - Daniel Flynn, Volpe 
  - Charles Baber, BMC (MdDOT rep)
  - Jana Natarajan, WSDOT
  - John Davies, FHWA-EERPAT (partial attendance)
Absent
  - Jeremy Raw, FHWA
  - Brian Hurley, ODOT

## Goals & Objectives
Tara welcomed everyone to the call and shared objectives and process for the VE-State project. 

Tara noted the VisionEval milestones of completing the transition of VE-RSPM & VE-RPAT code in the common framework is the foundation for building a statewide VE-State code.  She noted that ODOT uses both Statewide and Metropolitan level tools and was a key goal is to get them on the same platform to ease upgrades and capture the latest advances in VE-RSPM and EERPAT commodity flow freight model. She summarized the VE pooled fund goals and partners.

The oversight group on this call was chosen due to their various experiences with the tools The goal is for them to understand and influence the approach to a statewide VisionEval tool at a “Concept” level. Funding/schedule limit the oversight role to one of primarily review and advice. Since this is a pilot, more work is expected following this project.  Four meetings are planned to track progress on the project. This work is made possible primarily by Maryland DOT, State Highway Authority funding, supplemented with ODOT dollars.

## Introductions
Tara asked participants to introduce themselves and share  their experience with VisionEval, GreenSTEP or RSPM, and goals of the VE-State pilot project.
  - Brian Gregor, OSA – original author/designer of VisionEval. Looks forward to easier maintenance with all tools on a common code and cleaner module structure will open up to others.
  - Ben Stabler, RSG (staff) – managing deployment of RPAT and RSPM; Common VisionEval code is a better stable product due to software management product and testing with each software change. 
  - Daniel Flynn, Volpe – Volpe provides technical  support for FHWA hosting of VisionEval pooled fund project; excited to add VE-State to products available for community planning. 
  - Charles Baber, BMC  – led MdDOT EERPAT pilot. Appreciated cost-approach of VisionEval tools, MdDOT may use in biennial GHG work with state Dept of Environment. 
  - Jana Natarajan, WSDOT – led WSDOT EERPAT pilot. Nifty tool, great for planning.  Would like to see Commercial Vehicle model added (in both GreenSTEP and v3.0 EERPAT) and ability to better address issues with island counties.
  - John Davies, FHWA  – leads FHWA’s EERPAT program. Excited to see VisionEvalmoving forward with common architecture that can accommodate a statewide tool, possible EERPAT may move in trajectory of this work. EERPAT has been in a holding pattern since completing the upgrade to a commodity-based freight model. 

## VisionEval Background 
Tara quickly summarized the Strategic Niche of the VisionEval tools that use (1) detailed synthetic populations and vehicles like advance Activity Based Models; and (2) incorporate budgets and other feedbacks like integrated models; but (2) drop a detailed network to run quickly and complete many what-if scenarios. ODOT and Atlanta have run 100s-1000s of scenarios and used them in interactive web-based scenario viewers for stakeholders or the public to ascertain tradeoffs between investments and outcome. GUI and Scenario viewer will be part of the base VisionEval functionality. To make these many runs requires a balance between computational efficiency and model accuracy. 
Brian Gregor, Oregon System Analytics, also contrasted VisionEval role relative to traditional tools. He then introduced the family of VisonEval models and outlined how GreenSTEP and RSPM are alike, and how they differ.  The differences being primarily the level of detail on the land use geography. He then summarized the common VisionEval software framework and how this will work for VE-State as well as the existing VE-RSPM and VE-RPAT. The will use common software Framework and datastore, but swap out the land use modules and keeping other VE-RSPM transport modules
Brian summarized the standard geography used by the framework, which can be input or synthesized. Once a common geography is synthesized, the VE-State tool can use existing VE-RSPM modules to evaluate policies, assign vehicles, estimate VMT and congestion, and evaluate GHG.
Finally Brian summarized the new features in VE-RSPM that will be available to VE-State; improvements over both GreenSTEP and EERPAT.

## Draft Work Plan 
Brian outlined the three  step work plan and schedule.  
1- Test that RSPM code works with multiple Mareas and Azones (expected to work with minor fixes)
2- Develop a module to generate synthetic zones (the bulk of the effort, will need to capture realistic cross tabulation of household and built form attributes)
3-  Test the package in a “real world” example, using Oregon statewide data.  (ODOT will develop the data)

## Close and Next steps 
Tara summarized how the 4 meetings will fit into the work plan. Next meeting will discuss the approach for testing the code and the module to generate households, per a prepared “Integration Plan”.  These first two steps will commence, and report out at Meeting #3. Then the “real world” test will be implemented and reported in Meeting #4.  The product, in addition to the code and documentation, will include follow-up actions for future efforts beyond the pilot. Jana asked if it would be helpful to have a second state “real world” example in WA.  Tara said this was a great idea provided it didn’t slow down the schedule, and suggested revisiting this idea after Meeting #2. It could occur during or following this effort.

The project team plans to engage the oversight group using Github to house meeting materials and track issues/discussions between meetings.  The plan is to also follow each meeting with a list of questions to make sure issues are captured and addressed. 
