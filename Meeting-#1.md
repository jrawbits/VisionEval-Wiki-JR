MEETING DATE:	Wednesday, July 12
MEETING TIME:	12-3 p.m. 
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
Absent
  - Chris Porter, Cambridge Systematics
  - Jeremy Raw, FHWA
  - Kristin Tufte, PSU
  - Alex Bigazzi, UBC
  - Matt Hardy, AASHTO (observer)
Observers and staff
  - Eric Pihl, FHWA (observer) 
  - Ben Stabler, RSG (staff) 
  - Brian Hurley, ODOT (staff)
  - Tara Weidner, ODOT (staff) 
  - Kristin Hull, CH2M (staff) 

## Objectives
  - Share current status of VisionEval
  - Develop operating protocols for Review Team
  - Discuss the code testing process

## Summary

### Welcome and Introductions
Kristin welcomed everyone to the call and asked participants to introduce themselves and tell the group about their experience with VisionEval or the family of models.
  - Brian Gregor, OSA – original author/designer of VisionEval
  - Daniel Flynn, Volpe – new to VisionEval; presenting on open source management 
  - Josh Roll, ODOT – lead analyst on implementing Metropolitan GreenSTEP
  - Patrick Hall, ARC – used RSPM to analyze scenarios last year (200 scenarios)
  - Jana Natarajan, WSDOT – led EERPAT pilot
  - Liming Wang, PSU – research on integrated modeling, developer of urban sim, developing RSPM Multimodal model in VisionEval format
  - Dan Frye, PSU (alternate) – advisory to PSU on open source management 
  - Eric Pihl, FHWA (observer) – supported deployment of RPAT through SHRP2 program
  - Ben Stabler, RSG (staff) – managing deployment of RPAT and RSPM
  - Brian Hurley, ODOT (staff) – implemented RSPM at small MPOs
  - Tara Weidner, ODOT (staff) – analyst at ODOT, inherited GreenSTEP model and is expanding it

### VisionEval Overview – Tara Weidner, ODOT
Tara reviewed the VisionEval Phase 2 Activities using the graphic below.  She explained that the current technical work focuses on migrating existing tools to VisionEval common software framework.  She also explained that FHWA is establishing a pooled fund to support VisionEval.  Ben noted that this pooled fund/open source approach is being used for other modeling products in the industry and will likely become more common.  Tara also noted that packages of the “RPSM Multimodal Model” developed by Liming Wang/PSU in a recent ODOT Research project will be the test submittal in the 3rd meeting.
 
### Open Source Best Practices – Dan Flynn, Volpe
Dan presented a series of slides summarizing best practices for review of contributions to open source projects, including OSADP (private GitHub), Node.js (active), vegan (smaller less formal), and ActivitySim (most similar).  He covered the development process/governance, licenses and community engagement. The slides are available on the Meeting #1 wiki.  
Group members discussed:
  - Private Github sites tend allow more control, but are less transparent and attract less new contributors. Most examples were self-funded/volunteer-time by active members (OSADP and ActivitySim are the exceptions). More formal structures have a technical review committee or equivalent decision body. Twitter & podcasts can be helpful to pull in contributors.
  - New terms: “release” is any updated version of the model or modules and is treated as a tag in GitHub;“master” is the stable working version for end users, which may also be accessible on a user friendly website (e.g., TravelWorks RPAT) and/or CRAN mirror.  Some releases may be a package with R integrated to make it easier for users to install.
  - How to share data modules and if they should live in a specific repository.
  - That a Collaborator License Agreement (CLA) should be included as part of the governance structure as it avoids future disruptions (e.g. prevents someone contributing code they don’t own; increases code credibility; tracks who contributed the code and who reviewed it).  Should be in the checklist.

Tara reviewed process described by Susan for Intel.  This process is summarized on the wiki.

### Background on VisionEval Development Tools – Ben Stabler, RSG/Brian Gregor, OSA
Ben reviewed the wiki and described how the submittal and review process works today. He reviewed software management pieces of VisionEval.  Brian reviewed goals and objectives.  He highlighted that modules or sub-models can be shared in a plug and play fashion, that it is important for modules to be easily “regionalized”, and that it was important for models to run quickly; etc.  Brian reviewed the contribution review criteria.  Dan Frye asked if most entries will be new modules or line by line additions to existing modules. Brian said that he expected to see more new modules at first and to later see revisions to existing modules. 

A group member suggested that VisionEval could have different checklists and procedures for different types of additions (e.g. a bug fix would not require Review Committee approval).  

Ben discussed VisionEval’s Automated Testing.  He explained that Automated Testing will result in an automated pass/fail message and will test:
  - Input data are checked against input data specifications;
  - Input data geography is checked against specified model geography;
  - Module specifications are checked for correctness;
  - Module specifications for data to be fetched from the datastore are checked against the specifications for the data stored in the datastore; and

### Governance Structure and Charter – Kristin Hull, CH2M
Kristin introduced the draft charter and told the Review Committee that the key task today was to review and gather input on the charter. She explained that this was a pilot process to develop and test a charter.
The group edited the charter.  Kristin, Tara and Ben will incorporate discussion items into a revised charter in advance of the Review Team’s next meeting.  
Key discussion items included:
  - Should the Review Team review and accept modules/code that are not directly related to transportation mission?  Should those modules/code be shared in a separate repository or stored on other organization’s sites with links to the VisionEval site?  The group agreed that providing links was appropriate if the owners did not agree to accept long term maintenance of this code.
  - How should the Review Team address code that is outside of the Review Team’s area of expertise?  The group discussed having a smaller core Review Team (about 6 members) and a larger board of advisors who could provide input on specific topics.
  - How should the Review Team look at submittals that modify another contributor’s work?  The group agreed that the Review Team or the GitHUB site should notify the original contributor by email and offer them the opportunity to review the new submittal. 
  - What are Review Team members reviewing for?  What is the scope of their responsibilities? The group discussed the frequency of Review Team reviews and how technical their reviews should be.  There seemed to be a mix of impromptu meetings for complex submittals, as well as periodic planned meetings to discuss larger architectural issues about the code and provide recommendations to the owners. It was suggested to have a smaller core Review Team with input requested from other outside subject matter experts, where needed, including a possible set advisory panel for this purpose. Kristin, Ben and Tara will suggest amendments to the protocol to address this issue. 
  - Role of owners.  The group agreed that owners should set boundaries and strategic direction for the project and what is included in the maintained models/releases, separate from the technical decision of the Review Team.  
  - Repository Manager. Not sure any one person should serve as the liaison between the Review Team and the contributor/developers. 
  - Review Team voting.  The group discussed pros and cons of different voting schemes and quorum requirements for accepting new code, with one option at the discretion of the Review Team Chair.  Kristin, Tara and Ben will propose several alternatives for review at the next meeting.
  - Contributor License Agreements (CLAs).  The group suggested including CLAs in the contribution and acknowledgment section.  The extra overhead is worth the documentation trail and increased code credibility.
  - Expectations for the Review Team to review contractor deliverables.  The group agreed that the process should be the same for all contributors, once the master code base is established this year.  
Define different types of code submittals and how the checklists/review process might vary. Distinguishing what can be completed by the automated review and what needs human input by the Review Team.  This will be discussed in the next meeting. Kristin asked Review Team members if there were other topics that should be covered in the charter.  Review Team members suggested that the protocols should address selected changes the Repository Manager can make without Review Team concurrence; the Review Team would be delegating its authority.

### Close and Next Steps
Kristin told the Review Team that their next meeting was scheduled for August 3. By July 19, she asked team members to provide:
  - Comments on charter
  - Input on the “Contributor Review Criteria”, which will inform the “review checklist”, including variations for different types of submittals.

- [Open Source Project](https://github.com/gregorbj/VisionEval/wiki/documents/ContributorReviewTeam1OpenSourceVolpe.pdf) information presentation
- [Contributor Review Criteria](https://github.com/gregorbj/VisionEval/wiki/Goals-and-Objectives-of-VisionEval-Model-System)
- [Automated Testing](https://github.com/gregorbj/VisionEval/wiki/Automated-Testing)
- [Intel WiDi Case Study](https://github.com/gregorbj/VisionEval/wiki/Intel-WiDi-Case-Study)