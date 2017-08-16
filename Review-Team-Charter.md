The VisionEval Open Source project houses a common code base for a family of strategic planning models for public use which is maintained and supported by a set of agencies (i.e., “Sponsor”).   As illustrated below, the “code base,” housed in this publicly accessible repository, includes a common set of component “modules” that are assembled in various ways along with a “user interface” and the “services” that allow them to communicate.  Together these modules make up functioning “models” (i.e., RPAT, RSPM) that can be applied with local data to support analysis in various communities. 
 
FIGURE ONE

To maintain the integrity of these end models, the Sponsors established a Review Team process.  The Sponsors have delegated authority to this Review Team and appointed staff/consultants to manage and accept changes to VisionEval and make periodic releases of the software. The Review Team will not accept contributions that make changes to the fundamental framework without input from the Sponsors.

The VisionEval repository includes two main branches:
  - The [[master branch|https://github.com/gregorbj/VisionEval]] contains the latest version of the end models and the latest release of the VisionEval software. 
  - The [[develop branch|https://github.com/gregorbj/VisionEval/tree/develop]] is the in-progress development branch and contains all proposed changes, ranging from sponsor-directed upgrades and developer contributions, to updates due to new releases of R.

Before migrating from the develop branch to the master branch, all changes must successfully pass the review process and [[contribution criteria|Contribution-Review-Criteria]] (e.g., software acceptance tests, coding and documentation guidelines, and verification that sound methods have been implemented).  Both the Review Team’s technical approval and Sponsors’ acceptance are necessary for the change to be included in the released version of the software.  Software components that are not maintained will be dropped from future releases.

If developers wish to create software components that are outside of the core mission of VisionEval, as defined by Sponsors, developers are invited to host that code in their own GitHub repositories or in a separate branch. This site may include links separate repositories. 

This VisionEval review process is outlined in this document. 

FIGURE TWO

### Table of Contents
[Charge and Roles](#charge-and-roles)
[Review Team Governance](#review-team-governance)
[Code and Documentation Management ](#code-and-documentation-management)

## Charge and Roles

### Review Team Charge and Responsibilities 
The VisionEval Review Team is appointed by VisionEval Sponsors and is charged with maintaining the integrity and usability of the VisionEval repository and framework.  Specifically, the Review Team is charged with:
-  Developing a Review Team process for testing and accepting contributions into VisionEval.
-  Implementing the software testing and acceptance process (i.e., [[contribution criteria|Contribution-Review-Criteria]]) as new VisionEval modules, models and user interfaces, or other changes are completed.
-  Maintaining the integrity of the VisionEval repository, and software [[license|https://github.com/gregorbj/VisionEval/blob/master/LICENSE]].
-  Provide input as the Sponsors develop or update a [[roadmap|Development-Roadmap]] of new features or enhancements that will be considered for each product release, determining release plans and approving official releases.

Review Team members commit to:
  - Meeting up to four times a year; the Review Team may be asked to participate in longer strategic meetings for complex submittals or larger architectural issues. 
  - Reviewing results of software acceptance tests and content of contribution on an ongoing basis either though GitHub review or short impromptu meetings based on the number/frequency of submittals.
  - Reviewing results of contribution criteria and acceptance tests and providing written and verbal feedback to developers.
  - Reviewing contributions in areas specific to individual knowledge and experience. Each contribution will be reviewed for software, methods and documentation as described in the [[Contribution Review Criteria|Contribution-Review-Criteria]].  Review Team members will choose core review areas to focus on.
  - Maintaining familiarity with VisionEval tools and framework through regular use or development.
  - Abiding by these guidelines.

## VisionEval Roles

### Sponsors
The Sponsors will be responsible for overall project funding, strategic direction and governance decisions. The Sponsors will develop a governance agreement. This may include appointing Review Team members, hiring a Repository Manager and Release Manager, and/or funding and directing consultants working development on the VisionEval framework software on behalf of the Sponsors. Sponsors will not be responsible for deciding technical matters such as the quality of the software.

### Review Team
The Review Team will review results of all software acceptance tests and vote to accept contributions into VisionEval or provide feedback to developers about improvements that must be made for acceptance into VisionEval. The Review Team should have individuals with expertise in software, documentation and methods. Review Team members will specify their core review area. The Review Team is led by a Review Team Chair whom is elected by the Review Team. The Review Team may call on outside advisors for input when a submittal falls outside of the Review Team’s expertise.  More scrutiny and expertise is expected for changes to the core VisionEval framework used by all modules.

### Repository Manager and Release Manager
The Repository Manager and Release Manager will work at the direction of the Sponsors. The Repository Manager will maintain the repository, maintain the automated software acceptance test system, contribution criteria, share results with the Review Team, and assist the Review Team in communications with contributors.  The Release Manager will coordinate periodic software releases of accepted changes at discretion of Sponsors.  The Repository Manager is responsible for monitoring and documenting contributor process.  

### Developer Community
The developer community will develop changes to enhance and expand VisionEval based on their interests and project needs. Developers will fork the repository and issue a pull request to the develop branch of the repository. The Sponsors may also engage contributors to fulfill specific VisionEval needs to achieve the complete integration of the family of tools into VisionEval.

### User Community
VisionEval users will apply VisionEval end models to planning projects and provide input to the Sponsors and Review Team about the effectiveness of VisionEval, via GitHub issues where possible.  This may include technical aspects of downloading and running the software, identify bugs or issues, new feature requests, or the applicability of VisionEval to MPO or DOT processes.

## Review Team Governance

### Membership 
The Review Team will be appointed by the Sponsors.  The Review Team will be supported by project staff and will include an elected chair.  The Review Team will have about 6 members with membership rotating annually.  The Review Team must include a mix of individuals with competency in software, documentation and methods, and a balance of representatives from academia, consulting and agencies.

Review Team Operating Protocols
  - Review Team meetings will be facilitated by a Review Team Chair.  The Review Team Chair will be elected by Review Team members.
  - All Review Team decisions will be made in Review Team meetings or through voting on the project wiki.  The Review Team Chair will document decisions and post decisions and rationale to the wiki. All Review Team meetings will be hosted by webinar to allow remote participation.
  - Meeting summaries will be posted in the wiki.
  - Review Team members may discuss VisionEval, including the results of software acceptance tests, outside of meetings.  Review Team members will commit to bringing issues related to software maintenance, contribution criteria, and software acceptance tests results, to meetings for discussion by the full Review Team.
  - Review Team members may not speak on behalf of the VisionEval project.  This role is reserved for Sponsors.
  - The Review Team Chair will be responsible for advancing the review process when issues not anticipated in these protocols arise.

### Decision Making
The Review Team’s decision making is limited to accepting or rejecting revisions into the VisionEval repository.  The Review Team is responsible for the integrity of the software (e.g. does it work), licensing, documentation, and the integrity of the content (e.g. is it valid).
  - Each Review Team member has one vote.  Review Team members may vote to (1) accept; (2) accept but recommend revisions; (3) do not accept; or (4) abstain.  If a Review Team member chooses not to vote, a vote of (1) abstain will be recorded. 
  - Review team members will vote on software, documentation and methods.  If any area receives one “do not accept” vote, the contribution will not be accepted. 
  - A vote of “do not accept” is considered a veto.  If any Review Team member casts a “do not accept” vote, the contribution will be rejected.  The Review Team chair will determine next steps when a “do not accept vote” cast.
  - Review team members may vote in some or all categories depending on their area of expertise. 
  - Voting is recorded on the project site.  
  - The Review Team chair is responsible for determining how to move forward when a Review Team member does not cast a vote or seeking outside reviews if there are too few accept votes (i.e., due to abstains).  

The Review Team will provide feedback to developers via this site. The Review Team provides feedback for each required submittal category as follows:

| Status  | Software | Documentation	 | Methods | 
|---------|----------|-------------------|---------|
| Accept  |          |                   |         |
| Accept but recommend revisions |  |    |         |
| Do not accept|          |              |         |
| Abstain      |          |              |         |

## Code and Documentation Management 

### Automated Testing
The VisionEval software repository is under continuous [[automated testing|Automated-Testing]] to ensure contributions do not break existing functionality, additions are well formatted and functioning.  This testing will also ensure consistency with prior versions.  Before any changes are merged into the master branch, new VisionEval code must pass all tests.  The contributor must address issues that result in a failing test before the pull request is created and the change is ultimately merged into VisionEval. 

As described in [[Working Together|Working-Together]], developers either work on a fork of the repository, or in a developer feature branch and then issue a pull request to the VisionEval repository develop branch.  When a new feature is developed in the repository, the continuous integration system automatically tests the new software to ensure it operates correctly.  All VisionEval resources are automatically tested.  This includes the VisionEval framework (foundation) package, modules, models, and user interfaces.  This ensures the complete end user software will work when a user downloads a new release.  The Repository Manager maintains the test coverage goals and enforces a minimum threshold of test coverage for each new pull request.  Developers are encouraged to watch the repository to be informed of revisions that may interest them.

### Releases
The Release Manager will make official releases of VisionEval. The Release Manager will always have a working version of the complete software package as confirmed by the automated testing system.

### Documentation
Software documentation, including developer and user-oriented documentation, is maintained in the repository.  Documentation is held to the same standard as code.  If any of the documentation is missing or insufficient, the contribution will be rejected. Documentation is intended to ensure that contributions are well understood by the community of developers, reviewers, and users.

## Style, Philosophy and Licensing
The VisionEval project maintains a code and documentation style guide, as well as many examples from which to better understand what is expected in a contribution.  All contributions are open source and must be licensed according to the documented VisionEval [[license|https://github.com/gregorbj/VisionEval/blob/master/LICENSE]].  Contributions deemed insufficient in terms of style, philosophy, or license will be rejected.  

### Contribution Criteria
The Review Team maintains clear standards for software acceptance in the form of [[contribution criteria|Contribution-Review-Criteria]] available on the project site.  The Review Team will ensure that these criteria are available to developers in creating their submittal (along with developer guidance and examples), and used in Review Team assessment of code submittals.

### Contribution and Acknowledgment
Each contributor should be recognized and feel a productive part of the community, and it is a goal to encourage diversity, respect, and equality. Key to this is the recognition of contributions from individuals in a manner that also recognizes the community effort that made it all possible. Contributions of actual code are supported by design discussion, oversight, testing, documentation, bug fixes and much more. No code contribution is an independent unit of work (or should not be). It is therefore impossible to credit individual developers.  Developers will be recognized on GitHub as developers, but individual code will not be acknowledged.

Each contributor will complete the [[Contributor Licensing Agreement|]] in order to grant ownership to the Sponsors for the contribution project resources.
