## Objectives
* Review results of multimodal module test case
# Summary
## WELCOME AND INTRODUCTIONS
Kristin reviewed the agenda. She told the group that this was their final meeting during the pilot process and that the group would spend their time today testing the review process developed in the last two meetings and encapsulated in the Review Team charter, review criteria and other changes on the VisionEval wiki.  

## OVERVIEW OF MULTIMODAL MODEL AND RESULTS
Tara reminded the Review Team that they had been emailed links to the developer’s submittal being reviewed today.  This included links to the GitHub pull request and relevant documents and automated test results 

Liming reviewed slides summarizing his code submittal, the multimodal model (MM) update to VERSPM.  He explained that the VETravelDemandMM package would provide a better representation of multi-modal travel of households, update models with the latest and best available data, provide rigorous selection and benchmark of different model structures, and take advantage of R infrastructure and new packages.  A summary of the package is available here. He reviewed the methods and model structure.  Liming also reviewed the documentation or the module. He shared the results of the automated tests and said that the package passed all automated tests.

## CONTRIBUTION REVIEW CRITERIA RESULTS AND FEEDBACK FORM
Tara and Ben reviewed Liming  responses to the contribution review criteria,  summarizing their comments on how the submittal met each question. _(In notes: *Issues to be addressed following the meeting and reflected on the VisionEval Wiki charter, criteria, etc. +Issues to be addressed by sponsor/pooled fund partners at a future date)_

The Review Team discussed the following:
* It was noted that this submittal will also bring RPAT and RSPM closer together, as they will both use similar land use/5D built form input variables when this module is adopted.
* How are accepted module/package changes added into the overall production model (e.g., VERPSM, VERPAT)?  Who owns the overall repository and has authority to revise pieces of the model.  The group discussed these questions and determined that what is included in the next production release of models is part of the job descriptions of the release and repository managers and will be addressed in consult with the sponsors.
* *The group discussed where data should reside when it comes from external sources, or is oversized or confidentiality issues.  Should the data set be copied to a repository or should links to the external data be provided, with instructions if needed for access to confidential data.  The group agreed that a subset of the developers (Ben, Brian Gregor, Liming, Tara) should address this question.
* *A member asked if the estimation script was in the R directory.  Liming explained that the estimation script cannot be put the R directory because it will not run correctly due to the confidential data. Ben suggested the documentation be changed to note the data issue.
* +A review team member suggested that it might be good to test the model with a larger set of test data than the RVCOG data.
* +Need for some standard contract language for licensing to ensure that contractors developing code have the appropriate permissions for licensing. 
* *Slight revision to Review Criteria question 9 to ensure verification of release of ownership.  A CLA might be considered.
* *How to sort modules and packages where users have a choice between models or modules that do similar things.  As used in this submittal, submitted modules should try to use the same name as original module plus extra characters at the end, e.g., VETravelDemandMM)
## REVIEW TEAM FEEDBACK ON THE PROCESS/PILOT
* This process was useful.
* Liming’s summary is a good way to focus reviewers.
* Contribution review criteria covered the key questions.
* A pre-submittal meeting (like the one that Tara and Ben had with Liming) is a useful part of the process.  We should offer it to developers.
* It was noted that Liming has made significant contributions to moving the VisionEval project forward with this research/submittal.  He helped clean up the code and added helper functions that can be added to the framework for other developers, as well as adding to the automated tests. 
* *It was suggested that develop input on the process be included as a last question on the criteria list. Liming’s developer comments on this pilot process included:
** *It would be helpful to have some history of how a package developed over time. It was suggested that the suggested pull request be done to pull more than just a snapshot of the code. 
** +Responses to contribution review questions took a lot of time for the developer.  We may need to look at how developers are supported through this process if the development is not funded/sponsored by an institution or agency. This would result in more complete submittals beyond code that passes automated tests (e.g., in-line code comments, vignettes, function menus, estimation scripts and data, sensitivity testing) 
** +Some overlap in Review Team Criteria questions.
** Developer pre-meeting worked well to highlight any issues that could be addressed before the Review Team met to discuss the submittal.
* +The team should identify a different process for contributions that affect the framework.
* *To aid the job of the Review Team in complex contributions, it was suggested that developers include a summary showing how the changed package fits into the overall model system and a quick summary of the estimated functions and their dependent variables.  
* Review team members should plan on 2-3 hours to review a submittal.
* Template of Review Team Criteria questions worked well.
* Review Team co-chairs (Tara & Ben) worked well to cover both code details and methods.
* Meeting structure worked well, i.e., short developer overview followed by Review Team chair(s) walking through developer response to Review Team criteria questions to frame the discussion by submitter and Review Team members, arriving at whether each criterion was adequately met. 
Based on the discussion, the Review Team chairs (Tara and Ben) recommended acceptance of the submittal after the following changes are made.  The developer will be alerted by the repository manager (Ben) of these required actions once formalized in a vote of the Review Team:
* Update automated testing script to test new package.
* Revise the documentation/software to let the user know that the NHTS2009, SLD, confidential data for estimation, and estimation script are exceptions to the guidelines for various reasons.
* Add proof of ODOT release of ownership.
* Vignette and/or cheat sheet summarizing estimated functions and dependent variables.

## CLOSE/NEXT STEPS
Kristin will send out a “voting” email to all Review Team members.  Ben will post he and Tara’s responses to the contribution review criteria to the Wiki for member use.

Issues above designated with * will be addressed following the meeting and reflected on the VisionEval Wiki charter, criteria, etc. Those designated with + are left to be addressed by sponsor/pooled fund partners at a future date. 

