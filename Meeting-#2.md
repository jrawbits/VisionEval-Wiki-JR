MEETING DATE:	Thursday, August 3
MEETING TIME:	9-11 a.m.
LOCATION:	Call in/Webinar

## Attendees
Review team members and alternates
  - Brian Gregor, OSA
  - Daniel Flynn, Volpe 
  - Josh Roll, ODOT 
  - Patrick Hall, ARC 
  - Jana Natarajan, WSDOT
  - Liming Wang, PSU 
  - Dan Frye, PSU (alternate)
  - Chris Porter, Cambridge Systematics
  - Alex Bigazzi, UBC
  - Jeremy Raw, FHWA
Absent
  - Kristin Tufte, PSU
  - Matt Hardy, AASHTO (observer)

Observers and staff
  - Eric Pihl, FHWA (observer) 
  - Ben Stabler, RSG (staff) 
  - Brian Hurley, ODOT (staff)
  - Tara Weidner, ODOT (staff) 
  - Kristin Hull, CH2M (staff) 
  - Elizabeth Sall, UrbanLabs (staff)

## Objectives
* Review proposed protocols
* Discuss contribution criteria
* Review developer guide
* Introduce PSU test case


## Summary
### Welcome and introductions
Kristin reviewed the agenda.   She also addressed the key topics in Daniel Flynn’s white paper on open source projects and highlighted those topics that the Review Team will address.
Topic	Address?
License/CLA	Charter and contribution work flow
Developer Best Practices Guidance 	Discuss with Review Team today
Clear standards for code acceptance	Discuss what is covered in automated tests with Review Team today
Automated code tests	Developed by consultant team
Work flow/contribution process	Developed by consultant team; documented on wiki
Long term desired features 	Current list will be posted to wiki


### White paper
* [White paper](http://htmlpreview.github.io/?https://github.com/VisionEval/OSwhitepaper/blob/master/VEwhitepaper.html) on open source best practices

### Outline of developer guide and module example
Elizabeth reviewed the developer orientation guide outline.  The group discussed the guide.  Tara noted that the beginning of the guide will describe the VisionEval philosophy and provide context, since Strategic Models differ from traditional travel modeling.  Alex suggested organizing the guide by:
•	Resources, background, information and tools
•	Contributor expectations, style guide, review criteria
Josh suggested including a documentation template.  Liming noted that there are two types of documentation.  One is line-by-line in the R package code, and there is good example in recent VE modules.  The other – a narrative on the developer’s methods/approach – is also needed, perhaps in a vignette.  It could use better guidance for developers.  Brian said that both the model and module code should be documented by the developer in this way.

Later, Peter Hall indicated it would be useful to describe what constitutes a package.  Should the philosophy be to have few packages with many modules, or lots of packages that tackle smaller more focused functions?  Brian Gregor preferred the latter suggesting that packages focus on themes and the modules needed to achieve them, like “simulate households”.   This philosophy should be included in the developer orientation materials, e.g. Style Guide.



### Review Team protocols
Kristin introduced the two outstanding protocol issues.  Dan Frye suggested that the user community should be engaged in dialogue about submittals prior to the Review Team’s review, via GitHub issues, etc. The group agreed.
Brian Gregor noted that he thought a “Core Team” of people who could review the framework code should be identified, given Its importance (affects other modules) and complexity.  The group discussed different models for reviewing changes to the framework including a owner-driven rule-based Core Team, and a Benevolent Dictator for Life (BDFL) model, which may conflict with owner’s wishes since it raises questions about who actually “owns” the project.  After discussion, the group preferred to avoid the BDFL option, instead focusing on decisions by a core team based on warranted knowledgeable core/review team.  All agreed that this is an issue to be revisited by VisionEval owners.
The group requested distinguishing abstention from acceptance in voting. They otherwise liked the mix of expertise option that allowed Review Team members to not have to vote outside their area of expertise.
Dan asked about delegating minor review to the repository manager without a formal review.  Kristin directed him to the added protocol language on this topic.
Kristin agreed to update the protocols and circulate a clean version for approval.
### Contribution criteria
Ben led the group in reviewing the contribution requirements. Ben had put the criteria in a table to note if each requirement could be addressed by automated testing, or review team assessment of documentation and methods. A couple new questions were discussed. Ben added to existing or created new questions to address these topics:
•	Intent/Good Science: The group discussed the need to ask if “this is a good way to analyze the problem, reflecting industry best practices within the constraints of a strategic model.  They also discussed adding more about the module’s intent and purpose, and contribution within the broader model system.  
•	Data:  The group also suggested adding a question about the data being current and broad in geographic scope (if the data is not national, developer should state why). 
•	Integration Tests: Liming Wang suggested we add full model integration tests, testing both new model with contribution, as well as the old model after contribution was installed, in case some data was overwritten or code/libraries versions were incompatible.  Brian Gregor noted that namespace conflicts with old code are being addressed, but there is a need for the developer to describe the data to make sure its definition has not changed. Automated testing should also test whether the package produces the same datasets in the datastore, as other modules may rely on these data.
•	Sufficient Tests: Tara noted that if the developer is lazy and does not create many tests, some issues may not surface in the automated testing. The criteria should include a review of whether the tests provided by the developer are sufficient.


### [Introduce multimodal model](https://cities-lab.github.io/SPR788/VEReviewTeam.html#1)
Liming reviewed slides introducing the Multi-Modal model, which re-estimates the VMT model at the core of VisionEval tools using more recent NHTS and new EPA Smart Location Database (SLD). The SLD data allows inclusion of built form (5D) variables that will be useful to many VE modules.  It additionally takes a more comprehensive and rigorous approach to estimating non-auto mode outcomes – walk, bike, transit, an afterthought in the original GHG-focused model. Liming reviewed the data used, the two alternate approaches retained in the code (PMT-personal miles travelled, and 2-step TFL-Trip Frequency + Trip Length) and their econometric methods and variables (shared 1-page summary of the TFL approach). 
The Review Team will review this submittal at their next meeting to conclude the pilot effort.

### Close/actions/next steps
•	Kristin will circulate new Review Team Charter
•	Ben will update contribution review criteria
•	Liming will submit (pull request) his Multi-Modal RSPM model code for review (to be distributed to the Review Team before the next meeting)
•	Consultant team will continue to make progress on other fronts, including incorporating Review Team comments in the Developers Orientation materials.
•	Review Team can watch for materials from Meetings #1-3 on the GitHub Wiki site. 

### Adjourn
