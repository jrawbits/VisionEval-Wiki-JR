
*Last updated: February 15, 2018*

# Intro

The purpose of this document is to outline a documentation approach to VisionEval and identify additional documentation needs.

This document is organized as follows: it first discusses the various audiences and needs for VisionEval documentation and then goes on to define documentation venues and finally specific pieces of documentation that have or should be developed, their statuses, and relative priority.

**Outline**
 * [Audiences](#audiences)
 * [Venues](#venues)
 * [Situational Needs](#situational-needs)
 * [Proposed Products](#proposed-products)
 * [Priorities](#priorities)

**Principles:**
Documentation for VisionEval should adopt the following principles:

-   Cross-referencing rather than copying of information
-   Drill down to obtain more detail
-   Open sharing philosophy
-   Clean documentation without clutter based on differing audiences’

**Terminology**:
For the purposes of this Documentation Plan, the following terms and groupings are used:

*Primary VisionEval Framework Projects*, current projects working on the
base VisionEval framework, including:

-   Phase 1 ODOT Common Framework Demo, managed by Tara Weidner
-   Phase 2 AASHTO Project, managed by Brian Gardner and Jeremy Raw
-   Phase 2 Support Oregon DOT, managed by Tara Weidner
-   FHWA VisionEval Pooled Fund, managed by Jeremy Raw
-   Portland State University project, managed by Tony Knudson and Tara

*VisionEval Applications*, are projects that use VisionEval. These will typically involve customizing one of the VisionEval models(e.g., VE RSPM) for a particular state or metropolitan region, but could also be other projects, such as use in academic research for transportation or other related sectors.

*VisionEval Predecessor Models*, are the various incarnations and evolutions of the original GreenSTEP model and include:

-   GreenSTEP
-   RSPM
-   EERPAT
-   RPAT, formerly SmartGAP

# Audiences
This section identifies various VisionEval documentation audiences. For the purposes of this documentation plan., most of these  For the purposes of this documentation plan, most of these fall into one of the following categories:

 - decision-maker,   
 - semi-technical planner leading a project application,   
 - more technical model applier, and   
 - contributors (for model enhancement, research, or core framework development)  

## Decision-Maker

**Policy-maker / Agency Manager**: responsible for deciding whether to invest in VisionEval in time or resources (e.g., apply within region, or participate in pooled fund) as well as knowing when and how it is useful within the broader policy context. Needs to evaluate return-on-investment from a time/money/opportunity-cost perspective, relative to other tools. Concerned with application staffing and resource needs, maintenance, as well as tool credibility and value.

## Semi-Technical Manager
**Planner / Project Manager:** responsible for knowing how VisionEval might fit into a specific planning or policy project. Understands how to budget (time and money) and staff VisionEval tools within the context of a project or plan update and how to utilize the model and results. Understands basic data needs and model assumptions and caveats, how to choose between VE models, data needs, and how VE models can integrate with other tools.

## Model Applier
Model appliers could range in spectrum from people comfortable primarily in a GUI environment to those more interested and comfortable exploring the code and methods that they are using.

**Basic User:** responsible for gathering inputs, setting up, running, and evaluating and summarizing the results for VisionEval models within the context of a project or plan update. Understands the model methods, assumptions, caveats, and how to change them. Can identify and troubleshoot unexpected results and present results at appropriate levels of aggregation considering caveats. Has a basic knowledge of the R programming language and intermediate knowledge of travel modeling concepts, but is more comfortable using graphical user interfaces (GUI).  Documentation for the basic user should focus on using the mouse and GUI rather than on entering and running r-commands or code snippets via R-Studio or the command line.

**Super User:** In addition to more basic application of the tool, this audience will typically be more interested in VisionEval coding and methods and their evolution. These data scientists or academics, could possess more coding experience or subject matter strength, making them good candidates for reviewing new code, advise on new methods, or capable of basic upgrades, re-ordering modules, or re-estimation of parts of the VisionEval code (typically not building a module from scratch). The super-user may choose to run VisionEval using a GUI, but is comfortable writing and executing commands or code in R-Studio or a command line interface using the VisionEval API.

## Contributor
This category encompasses everyone who might contribute code or concepts to mainline VisionEval models.

**Developer:** responsible for using templates and instructions for developing new models, modules, and packages for VisionEval. Has an intermediate to advanced knowledge of the R programming language (experience in creating R packages) and advanced knowledge of travel modeling concepts (or is working with somebody who does). Model Developers should be well acquainted with VisionEval coding guidance and interested in contribution criteria and processes.

**Researcher:** interested in using VisionEval to test a research hypothesis. Should be familiar with all aspects of being a model applier and if needed, should also have skills associated with model developer. In addition, a researcher will be interested in research questions of interest to society that can be addressed with VisionEval as well as data that may help develop and support new modules. Also interested in materials that enable use of VisionEval in curriculum/classroom settings. Also interested in materials that enable use of VisionEval in curriculum/classroom settings.

**Framework Developer:** A “super-developer” able to alter VisionEval core code, uses an advanced understanding of the R programming language, the VisionEval framework, and VisionEval contribution guidelines, governance, and roadmap in order to progress the state of the VisionEval framework for the benefit of all.

# Situational Needs

This section lists information needs or questions organized by situations and ordered from general (general knowledge) to specific (narrow audiences). Table 1 shows how each of these situations (rows) likely maps to each audience (columns). Each cross-section mapping or “point of information”, highlighted in the table should be easily accessible from a *Primary VisionEval Venue*, which is discussed in the next section.

> Each of these information needs or questions should be
addressed within one click of entering into a Primary VisionEval Venue

Table 1. Situational needs fall out of mapping of audiences to situations

 . | **Policy/Project Mgr** |  **User**  | **Super User** | **Developer** | **Researcher** | **Fmwk Dev’r** | **Agency Mgr**
--- | :---: | :---: | :---: | :---: | :---: | :---: | ---
Awareness | :red_circle: | :red_circle: | :black_circle: |:black_circle: |:black_circle: |:black_circle: |:black_circle: |
Consider | :red_circle: | :red_circle: | :white_circle: |:white_circle: |:black_circle: |:white_circle: |:white_circle: |
Project Planning | :white_circle: | :red_circle: | :red_circle: |:white_circle: |:white_circle: |:black_circle: |:white_circle: |
Using GUI  | :white_circle: | :black_circle: | :red_circle: |:black_circle: |:black_circle: |:black_circle: |:black_circle: |
Using API  | :white_circle: | :white_circle: | :black_circle: |:red_circle: |:black_circle: |:black_circle: |:black_circle: |
Developing | :white_circle: | :white_circle: | :white_circle: |:black_circle: |:red_circle: |:black_circle: |:black_circle: |
Research| :white_circle: | :white_circle: | :white_circle: |:white_circle: |:white_circle: |:red_circle: |:white_circle: |
Framework Dev’t| :white_circle: | :white_circle: | :white_circle: |:white_circle: |:white_circle: |:white_circle: |:white_circle: |


## A. Awareness

**Primary Audiences:** Agency Manager or Project Manager  
**Other Audiences:** All

Strategically placed and widely available promotional materials will raise awareness about Vision Eval.  Materials developed as part of documentation can inform and provide material for an awareness campaign.   Dimensions that should be addressed when developing initial awareness include easy (one-click) access to the following information:

-   What it is. What can it be used to evaluate?
-   How can results support policy conversations?
-   How is VisionEval different from other models that are in our agency toolbox?
-   Tool credibility. Why should they trust it. Who is behind it and who uses it.
-   High level information on how does one “use VisionEval”?
    -   What is it going to cost me?
    -   What data do I need?
    -   What staff do I need or who do I hire?

> #### Recommendation:   
To the extent possible, references to previous frameworks in the VisionEval history should be scrubbed from any ‘primary’ descriptions so as to avoid confusion for new audiences.

## B. Consideration / Evaluation

**Primary audiences:** Agency Manager or Project Manager  
**Other audiences:** Researcher

Once aware and considering its use, they will likely be interested in:

-   Best practices and case studies highlighting value, how VisionEval supports planning process (e.g. structures planning conversations; quantifies adopted plans)
-   High level project history, structure, and roadmap for the future
-   What a project looks like with VisionEval and how and what data and staff resources are needed
-   What VisionEval is sensitive to; key influencing variables for development of additional modules.
-   How VisionEval compares with other tools in their toolbox;
-   Tool credibility. Have results been compared to other tool I use? literature ?
-   Key differences that impact choice of which VisionEval model to use on their project.

## C. Planning for Model Application

**Primary audience:** model applier and planning or policy project manager  
**Other audiences:** planner, model developer, model framework
developer, researcher

Once a team has decided to use VisionEval for a project or plan update, they need to plan out what that looks like with more specifics.

-   Prerequisites and preparation
-   Overview of main components and how it works
-   Specific data needs and where one typically finds them
-   Best practices and case studies that they can follow or learn from
-   Resources to connect with others who are using VisionEval to get their assistance/opinions
-   Understanding of which modules and inputs have an effect on outcomes they are concerned with
-   What skills do I need to acquire to be a High-End applier/Developer;  What outside/inside resources are available to gain these skill sets

## D. Using VisionEval as a Basic User

**Primary audience:** user; model applier  
**Other audiences:** planner, super-user, model developer, model
framework developer, researcher

When a project is underway and the model applier sits down to start using VisionEval, the model applier will need some much more specific guidance, such as:

-   How do they install VisionEval and get it running with example data?
-   How do they clean and setup input data?
-   How do they set up a VisionEval run? What model definition files do they need to create and how do they go about creating them? How dothey develop a model run script? What settings should be selected
 when and why?
-   What are typical troubleshooting tactics, and if those don’t work how do they get help?
-   Quick reference on terminology and definitions

This documentation should focus on the how to use VisionEval with graphical user interfaces (GUI) rather than running code via the command line.  Documentation should include plenty of screen-shots.


## E. Using Advanced VisionEval

**Primary audience:** super-user  
**Other audiences:** user, model developer, model framework developer,
researcher

Super-users will likely prefer to use the API rather than the GUI to use VisionEval. Documentation for using VisionEval with the API should integrated into the GUI-based documentation, but obscured by default such that regular users are not presented with code. This can be accomplished using a tab-based system.

## F. Developing Modules, Packages, or Models

**Primary audience:** model developer  
**Other audiences:** model framework developer, researcher, super-user

Model developers will need access to both the underlying theories of
each VisionEval package, module, and model as well as the development
philosophy and contribution guidelines,. Specifically, they will need:

-   VisionEval development philosophy and contribution guidelines
-   Testing, and documentation requirements
-   Theories, assumptions, and data the models, packages, and modules are based on
-   Modification strategies: when to adjust data or parameters vs adding a module or a package
-   How to adjust parameters or an existing module
-   How to add a module to a package
-   How to add a package
-   Licensing
-   How to modify or add a model

## G. Using VisionEval for Research or Classroom Projects

**Primary audience:** model researcher or teacher
**Other audiences:** model framework developer

An academic researcher may want to use VisionEval for a specific research project (in which case they would have similar needs to a Model Applier), but researchers may also be interested in knowing what research questions have been sourced by the VisionEval community or its related communities. They may also wish to use VisionEval models within a classroom setting to illustrate how analysis supports and influences policy discussions. Thus, they have the additional documentation need of:

-   What are outstanding research questions? Who are potential  collaborators with my common interests?
-   How can I add VisionEval modules from my domain while trusting existing modules outside my expertise? What model limitations or caveats do I need to be aware of?
-   How do I cite VisionEval?
-   How have others used VisionEval as part of classroom curriculum?

## H. Developing the VisionEval Software Framework

**Primary audience:** model framework developer

In addition to all the information needed under Developing Modules, Packages, and Models, model framework developers will need to to understand if and how to modify the framework as a whole, which could require substantial collaboration within the VisionEval governance structure.

-   Software development roadmap
-   Framework governance
-   Contribution guidelines
-   Licensing
-   Framework software documentation

# Venues

This section describes where various forms of documentation should be aggregated in order to be easily accessed by various audiences. Each venue should have one-click access to material used by its primary audience and also reference other venues.

## Focus Development / Limit Documentation Sprawl
One of the challenges facing the VisionEval project is the multiple channels of funding and development that have contributed to or are currently contributing to its development and use. In order to focus attention and resources, the Primary VisionEval Framework Projects should identify and commit to using a finite “stack” of Primary Documentation Venues and limit the addition of information sprawl beyond them. Exceptions to this strategy may include information that is required to be hosted from another site (i.e., conference proceedings, local agency projects or guidelines).

VisionEval documentation should be disseminated via the following Primary Documentation Venues:

-   Main Website: visioneval.org
-   User Website: visioneval.org/users
-   Developer Website: visioneval.org/developers
-   Github Code github.com/<...>
-   Agency project websites (including [*Oregon DOT Scenario Planning page with  video*](http://www.oregon.gov/ODOT/Planning/Pages/Strategic-Assessment.aspx))
-   Outside References/Related Links (e.g., TRF Resource, SHRP2 Future  Forces, FHWA Scenario Planning; other travel modeling open source  projects/forums)

Table 2 maps these venues to the situations identified in the previous section with the dark color representing a primary and light color representing secondary. A switchover from VisionEval.org occurs when the primary audience switches from policy/planning to technical in nature.

Table 2. Mapping of Primary Documentation Venues to situations (dark:
primary light: secondary)

. | **VisionEval.org** |  **Agency Project Website**  | **User Website** | **Developer Website** | **Github Code**
--- | :---: | :---: | :---: | :---: | ---
Awareness | The Front Door :red_circle: | Explain agency involvement, redirect to VisionEval.org :black_circle: |   |  |
Consideration | The Front Door :red_circle: | Provide information specific to the agency, but then redirect to VisionEval.org <br> :black_circle: |   |  |
Project Planning | :red_circle: | Provide information specific to the agency, but then redirect to VisionEval.org <br> :black_circle: | Case Studies: How supported conversions, partnerships, resources needed. | |
Using |  | Provide information specific to the agency, but redirect to user's guide <br> :black_circle: | :red_circle: | | |
Developing | | Provide information specific to the agency, but redirect to visioneval.org/developers :black_circle: | | :red_circle: | |

### Retirement of and redirection from previous venues

To limit confusion, each VisionEval Predecessor Model should clearly identify that future focus and development has migrated from that model to the VisionEval framework. Currently, it seems as though they are being actively developed and maintained since they don't have a redirect to VisionEval (from project website and their github code), which causes confusion that they are “competing” projects.

> #### Recommendation  
Each predecessor project should clearly direct users to the appropriate VisionEval resource and very clearly indicate its replacement via a statement such as "RPAT is now transitioning to VisionEval. Please refer to VisionEval project for all information post RPAT version X."

Additionally, when models with similar capabilities are developed within the VisionEval framework, they should have separate identities in order to limit confusion and clearly identify the differences. A google search of “VisionEval RSPM” could easily direct an unknowing user to the retired RSPM website, but a name akin to “VisionEval - Regional” would not. For now, using a VE-RSPM as a single word is clear enough.

## Responsibilities and Maintenance

Each Venue should have a responsible party, a support team, and a plan to make sure all information and links are up-to-date. Table 3 shows a suggested schedule of these responsibilities, although most of the cells are yet to be determined pending decisions made in the VisionEval pooled fund shared management plan.  Any plans will also need to decide access/editing rights to the website content. Development and version progression will likely require a more frequent update schedule for development and user’s guides whereas more broad information about the framework will change less frequently.

Table 3. Mapping of Primary Documentation Venues to Maintenance
Schedules

. | Responsible Party | Support Team | Maintenance Schedule
--- | --- | --- | ---
`visioneval.org` | TBD | TBD | semi-annual
`visioneval.org/user` | TBD | TBD | quarterly
`visioneval.org/developers` | TBD | TBD | quarterly
`github/<...>`  | repository and release manager | TBD | weekly builds
Agency website | respective agency | respective agency | quarterly
Case studies | TBD | TBD | annual

Each maintenance interval should include updates and highlights, testing of any ‘how-tos’ with any software changes, testing links, and taking down old and outdated information.

## Documentation versus Outreach

The focus of this Documentation Plan is on the organization and content of venues under the purview of the VisionEval Project; however, in the case of the ‘awareness’ objective, a significant amount of outreach and integration with other documentation is a prerequisite to getting the right traffic at our destinations.

**Outreach Chanel A** :arrow_lower_right:  
**Outreach Chanel B** :arrow_right:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  **Primary "Awareness" VisionEval Venue**  
**Outreach Chanel C** :arrow_upper_right:

The focus of the outreach facet of the documentation plan will be on what people should see once they seek VisionEval out as well as having tidy summaries and bites of information “at the ready” should there be an opportunity to add VisionEval to a related information channel. In all cases, it should strive to drive interested parties back to a VisionEval Primary Venue. A partial list of potential channels is provided below, but should be more fully addressed through an outreach plan.

Potential awareness channels:

-   [*North American City Transportation Officials*](https://nacto.org/), American Planning Association,[*American Association of State Transportation Official*](http://aashto.org)s, [*Transportation Research Board*](http://trb.org), [*Institute of TransportationEngineers*](http://ite.org), [*Women’s Transportation Seminar*](http://wtsinternational.org), [*RPA*](http://www.rpa.org/), [*SPAN*](http://www.scenarioplanning.io/), University Transportation Center Conferences
-   Magazine articles in [*Governing*](http://www.governing.com/), [*TR News*](http://www.trb.org/Publications/PubsTRNewsMagazine.aspx), [*ITE Journal*](http://www.nxtbook.com/ygsreprints/ITE/G86608_ITE_Jan2018), and [*Planning*](https://www.planning.org/planning/)
-   Website articles like [*Planitizen*](https://www.planetizen.com/) or [*Streetsblog*](http://streetsblog.org)
-   Podcasts like [*Streetsblog*](https://usa.streetsblog.org/category/special-features/podcast/)
-   [*Zephyr Foundation*](http://zephyrtransport.org)
-   [*Travel Forecasting Resource*](http://tfresource.org)
-   [*Travel Model Improvement Program*](https://tmip.org/forum) listserv/forum

## Documentation versus Support

Good documentation is not a replacement for the product support. As VisionEval acquires a broader user base, dynamic quality product support will become a significant need. However, support is often one of the poorest executed components of an otherwise successful open source project. While the Primary VisionEval Projects are likely loathe to support or advertise for a single commercial support provider, they can provide the framework for a peer support network of users. Again, in order to limit information sprawl, the Primary VisionEval Projects should create, endorse, and maintain a limited selection of peer-to-peer resources, which are not specifically detailed as a documentation product, but are critical to the success of the VisionEval ecosystem, such as a users group, group chat, and an in-person meeting.


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:arrow_upper_right: **User's Group**  
**Primary "User" VisionEval Venue** :arrow_right: **Conferences**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:arrow_lower_right: **Group Chat**

**Users Group**: email list or bulletin of some kind to broadcast information.    
**Group chat**: more ad-hoc conversations and help via a platform like [*Slack*](https://slack.com/).  
**Conferences**: in-person get-togethers covering planning or developer topics, to share best practice applications, showcase advances and integration into larger toolkit, and work through hurdles and the roadmap together.

# Proposed Products

Proposed products are discussed in the following situational groups:
1.	awareness, consideration, and model application planning,  
2.	using VisionEval, and   
3.	developing VisionEval.  

Each documentation “product” is denoted by a :large_blue_diamond: symbol although in the end the content of many various products may be combined together.

## 1 - Awareness, Consideration and Model Application Planning Oriented Documentation

### :large_blue_diamond: Splash Page Home
**Awareness Situation**: The Splash Page is the main point of entry for people who are getting familiar with VisionEval for the first time.  and should be able to quickly answer or direct people to resources that addresses each of the needs identified for the Awareness role:

- What it is. What can it be used to evaluate?
- How can results support policy conversations?
- How is VisionEval different from other models that are in our agency toolbox?
- Tool credibility. Why should they trust it.  Who is behind it and who uses it.
- High-level information on how one “uses VisionEval”

**Consideration Situation**: The Splash Page should directly address the interests and needs of the consideration situation where it intersects with the awareness situation, but save more in-depth reading for material that is directly linked from it.  Specifically, the Splash Page should address:
- How VisionEval supports planning process
- How VisionEval compares with other tools in their toolbox
- Tool credibility.
- Links to:
 - High level project history, structure, and roadmap for the future
 - What a project looks like with VisionEval and how and what data and staff resources are needed.
 - Key differences that impact choice of which VisionEval model to use on their project.
 - Best practices and case studies highlighting value, how VisionEval supports planning process (e.g. structures planning conversations; quantifies adopted plans)
 - What VisionEval is sensitive to; key influencing variables for outputs of interest;
 - More detailed tool credibility. Have results been compared to other tool I use? Have results been validated to expected elasticities from the literature?

**Model Application Planning Situation**: The Splash Page should direct an individual to the appropriate resources for model application planning, but not clutter the page by directly addressing them.  

- Link to “VisionEval in a Nutshell” which addresses most of their needs.
 - Prerequisites
 - Overview main components, and how it works
 - Specific data needs and where one typically finds them
 - Understanding of which modules and inputs have an effect on outcomes they are concerned with
 - What skills do I need to acquire to be a High-End applier/Developer; What outside/inside resources are available to gain these skill sets
- Links to:
 - best practices and case studies that they can follow or learn from
 - Resources to connect with others who are using VisionEval to get their assistance/opinions

 The content should be crisp, quickly consumable, and not littered with unnecessary detail. Page design should be modern, mobile-ready web design of full-bleed graphics and a scroll-down with small menu selections shown in top-right corner.  Top-level menu options should include: users-guide, get-started, and about.  Additionally, a github logo somewhere in the top header should let developers know to “click there”.

Suggested content ordering is:
1.    **What it is? What can it be used to evaluate?** Top headline should have a full-bleed graphic, the byline “Exploring  Tomorrow Today” and state what VisionEval does in less than two sentences in words that mean something to a city official. Message can be further supplemented with short video (Volpe’s 5-min video).
2.   **How can results support policy conversations and the planning process?** Three (or so) short case studies (see below) representing different use case typologies should be listed with click-thrus available to a full description with graphics that could be printed out if desired. Quotes from agencies could be listed under the headlines, if applicable.
3.   Key Products, such as the web-based interactive Scenario Viewer could be included to, Place Type Tool, Curriculum guide that further share value of specific case studies and underscore other valued uses of the tools. To highlight these products, a short couple minute video might be needed to provide context.
4.    **How VisionEval compares with other tools in their toolbox.**  High level description of how VisionEval would fit into an existing toolbox/why it is different, using graphics.  Some of this content already exists (RSPM vs Other Models. other models.docx being best example), but it need to be shortened, crisped, and re-aligned to VisionEval rather than any of the predecessor models.
5.   **Tool credibility.** A collection of logos from agencies and companies that VisionEval is “used and supported by”.  This is not to show official endorsement or investment; rather, it is to show that there are a lot of agencies working with it.
6.   **High-level information on how one “uses VisionEval”.** A diagram of “how it works” to use VisionEval from a manager’s perspective using graphics to show different stages including hiring consultants/using existing technical team, data development, developing and testing scenarios, and evaluating the results.  This section should answer high-level questions like what it costs, data requirements, time requirements, and staff needs.  It should also link to one to two longer, in-depth case studies (see below).
7.   **Tool credibility.** To add even more “trustworthiness”, a select list of peer-reviewed references, project awards, with a link to more (e.g., peer review, sensitivity tests).  It should also point to pooled fund investment and code acceptance/review team process.
8.   Track interested parties through an email list sign up form.  
9.   Links to:  
  - About VisionEval
  - Pitch Deck + Tear Sheet
  - VisionEval in a Nutshell
  - User’s Guide  
  - Developer Documentation
  - Resources for Assistance

*Examples*: Both [*Envision Tomorrow*](http://envisiontomorrow.org/) and
[*Urban Footprint*](https://urbanfootprint.com/) have effective modern, graphics-forward splash pages with content-snippets that are examples to look towards.

The splash page should live at http://visioneval.org and be an easily-updated Jekyll page (or similar). VisionEval.org is currently owned by Volpe as part of the pooled fund and exists as a placeholder page. This page should be updated no less than semi-annually to feel fresh and include Google Analytics in order to track traffic.

### :large_blue_diamond: Splash Page / About
The About page should have information about governance, financial support, and predecessor projects, which should be kept off the main splash page because it is potentially confusing.

**Consideration Situation**:
 - High level project history, structure, and roadmap for the future

**Awareness Situation**:
 - Trustworthiness. Why they  should trust it.  Who is behind it and who uses it.

Example: [*http://visioneval.org/about/*](http://visioneval.org/about/)

### :large_blue_diamond: Tear Sheet

The purpose of the Tear Sheet is to have something you can “hand” to somebody to generate awareness.

**Awareness**: The Tear Sheet should touch on all the needs for the Awareness situation, but in an abbreviated fashion necessitated by the format.  These include:  
 - What it is. What can it be used to evaluate?
 - How can results support policy conversations?
 - How is VisionEval different from other models that are in our agency toolbox?
 - Tool credibility. Why should they trust it.  Who is behind it and who uses it.
 - High-level information on how one “uses VisionEval”

 This is something that can be printed and brought to conferences or printed out to bring to a meeting.  Content should be a summary of content on visioneval.org Splash Page and should be a downloadable PDF linked to from the main Splash Page.  This should be updated whenever the Splash Page content is updated.  

*Example*: The Peer Exchange Handout
(`VisionEval_HandOut_2016PeerExchange.pdf`) is an example of a tear-sheet, but takes up precious real-estate describing the history and relationship between each of the predecessor models rather than showcasing value. Other VisionEval handouts have been developed for the 2016 TRB ITM Conference's "Strategic Planning Tool" workshop and 2017 Pooled Fund Outreach.

### :large_blue_diamond: Pitch Deck

**Awareness Situation**: The Pitch Deck should function similar to the Splash Page, but delivered to the audience rather than being actively consumed.  It should touch on all the needs for the Awareness situation:
 - What it is. What can it be used to evaluate?
 - How can results support policy conversations?
 - How is VisionEval different from other models that are in our agency toolbox?
 - Tool credibility. Why should they trust it.  Who is behind it and who uses it.
 - High-level information on how one “uses VisionEval”

A short (5 - 10 slide) presentation deck that summarizes the information on the landing page. This can be used as source material for anyone giving a VisionEval presentation or would be used in meetings discussing the potential use of VisionEval. Creating a standard set of 5-10 slides that are routinely updated will ensure the message of what VisionEval is remains crisp, and up-to-date while reducing redundant work.

### :large_blue_diamond: Hypothetical Use Cases / Short Case Studies
The purpose of these hypothetical use cases or short case studies is to show what the framework is designed to be used for.  It should primarily address the Awareness situation, while briefly touching on some of the concerns of the Consideration situation.

**Awareness Situation**: The short case studies should touch on the following needs of the Awareness situation:
 - What it is. What can it be used to evaluate?
 - How can results support policy conversations?
 - How is VisionEval different from other models that are in our agency toolbox?

**Consideration Situation**: The short case studies should also touch on the following need for the Consideration situation.
 - Best practices and case studies highlighting value, how VisionEval supports planning process (e.g. structures planning conversations; quantifies adopted plans).

They can be real case studies (if they exist), case studies from predecessor frameworks that could be easily implemented in VisionEval, or hypothetical case studies based on capabilities. These should be short – no longer than a few paragraphs and a few photos. Content for each use case should follow a standard template and include: (1) how tool supported policy conversation, provided value, influenced decision (2) a comparison to other tools that were considered and (3) a rough trade-off calculation on time/precision/money/data requirements that makes VisionEval a competitive/useful tool. Cases should be reviewed no less than every year to make sure they are accurate and cover all the framework capabilities.

*Examples*: VisionEval capabilities handout from the August 2016 Peer Exchange (`VisionEval Capabilities_20160817.pdf`) is a good start for defining what they should focus on. Volpe has also developed [*RPAT pilot Case Studies*](https://planningtools.transportation.org/560/resources.html) including those for FHWA newsletter articles that might be used as a template for what to include. A more technical example of these can be found at [*Use Cases from R Open-Sci*](https://ropensci.org/usecases/).

### :large_blue_diamond: Full Case Studies
The purpose of full case studies is to help a project manager template a process for a project or plan update that uses VisionEval.  The primary audiences are the Consideration and Model Application Planning situation.

**Consideration Situation**:  The Full Case studies will help an individual in the Consideration Situation understand the value and investment that could be involved in a VisionEval implementation.  They should address the following needs of an individual in the Consideration Situation:
 - Best practices and case studies highlighting value, how VisionEval supports planning process (e.g. structures planning conversations; quantifies adopted plans).
 - What a project looks like with VisionEval and how and what data and staff resources are needed?

**Model Application Planning Situation**: The Full Case Studies should serve as a model for an individual planning a VisionEval implementation and specifically address:
 - Best practices and case studies that they can follow or learn from.
 - What skills do I need to acquire?

The content should focus on process, resource needs (time, money, and personnel), and outcomes. It should be self-critical in so much as any improvement or iterations could be helpful to anybody following along and should also include up-to-date contact info for the technical project manager at the relevant agency where they can seek even more candid feedback and advice.

Full case studies should be their own page on visioneval.org, but formatted in order to be easily printed to PDF or to a printer to bring to a meeting or use as a reference. Case studies should be reviewed annually to make sure they are still accurate, relevant, and recent enough to be compelling.

## 2 - User-Oriented Documentation

The user-oriented set of documentation takes over after an agency decides that it will be using VisionEval and needs documentation on how best to implement and use it.  The primary audience should be a basic user, with the needs super users and contributors addressed while remaining accessible to the semi-technical manager.

The User’s Guide content should be divided into components which will be accessed from different stages and points in time:

1.  Project Planning: what to expect and what to prepare for
2.  VisionEval in a Nutshell
3.  Guides customized for each model:
    a.  Getting Started: installation and navigation
    b.  Data + Parameters
    c.  Running a VisionEval model
    d.  Modules, and influencing variables
    e.  Output analysis (e.g., GUI or HDF5 tools)
4.  Reference
    a.  Cheatsheets
    b.  Datastore
    c.  Terminology
    d.  Best practices in agency documentation tool applications
5.  Help!
6.  Course

Content should be centered around the website: visioneval.org/user, which would ideally be a jekyll-based (or similar) website hosted on GitHub. Some content discussed here already exists, but needs to be reframed to a user rather than developer.

The user documentation should have the following features:
-   Can be easily updated when relevant software is updated, but backward-rollable to view documentation for any version (i.e. VueJS.org.
-   Toggle between GUI-based and code-based descriptions and  instructions to enable more advanced users to access more features, but not alienate users who are more comfortable pointing and clicking; be able to drill down as far as you want, but top-level framing should be similar to Appendix 2 in the [*RSPM User’s  Guide.*](http://www.oregon.gov/ODOT/Planning/Documents/Oregon-Strategic-Assessment-RSPM-Users-Guide.pdf)
-   Toggle between models, but uses reusable content blocks where models are the same
-   Version-controllable

Some good examples of user guides include:

-   [*AstroPy*](http://www.astropy.org/index.html) has clear links at the top of the page, including for how to get help. The /documentation section is well organized at the higher-levels, although content in each item is hit-or miss.
-   [*VueJS*](https://vuejs.org/v2/guide/) has a great user’s guide which can be rolled back to view various versions.
-   [*SWIM 2*](http://www.oregon.gov/ODOT/Planning/Documents/Oregon-Strategic-Assessment-RSPM-Users-Guide.pdf)
-   [*RSPM*](http://www.oregon.gov/ODOT/Planning/Documents/Oregon-Strategic-Assessment-RSPM-Users-Guide.pdf)
-   Geography presentation (`VisionEval_Geog.pptx`).

Useful online documentation format examples include:
-   [*Atom Flight  Manual*](http://flight-manual.atom.io/using-atom/sections/atom-packages/), [*built using  Atlas*](http://blog.atom.io/2016/03/24/the-new-and-improved-flight-manual.html) and [*Nanoc*](http://nanoc.ws)
-   [*Hitchiker’s Guide to   Python*](http://docs.python-guide.org/en/latest/), using SPHINX and ReSTructured text
-   [*VueJS.org*](https://vuejs.org/v2/guide/) using vueJS
-   [*Stripe*](http://p)
-   [*Atlas, using Atlas*](http://docs.atlas.oreilly.com/)

### :large_blue_diamond: Project Planning: What to expect and prepare for
The project planning component should primarily address the Semi-Technical Manager’s needs during the Planning for Model Application situation, but should also be read by VisionEval users to provide background.

**Planning for Model Application Situation**: The project planning component should specifically address the following concerns of an individual planning for a model application:
-   Prerequisites and preparation
-   Specific data needs and where one typically finds them
-   What skills do I need to acquire to be a High-End applier/Developer; What outside/inside resources are available to gain these skill sets
-   Links to:
 -   Best practices and case studies that they can follow or learn from
 -   Resources to connect with others who are using VisionEval to get their assistance/opinions

The Project Planning component should include one-to three simplified checklists to follow and provide links to the in-depth case studies.  Potential checklists include:
-   Preparing your team (including yourself)
-   Preparing your data
-   Preparing your management
-   Process for a basic VisionEval process (probably using RSPM)

If it is possible, it would also be useful to provide ranges for estimated level of effort and time horizons that should be used for planning a project.

### :large_blue_diamond: VisionEval in a Nutshell
VisionEval in a Nutshell should be a less than half day (20 to 30 pages) read about VisionEval philosophies, definitions, models and setup. VisionEval in a Nutshell should be oriented towards the Model Application Planning Situation as well as Basic Users, Advanced Users, Researchers, and Developers.  

**Model Application Planning, User, and Developer Situations**: are all interested in the following issues in VisionEval in a Nutshell:
-   Prerequisites
-   Overview of main components and how it works
-   Specific data needs and where one typically finds them
-   Understanding of which modules and inputs have an effect on outcomes they are concerned with

As a prologue to the more step-by-step components of the User’s Guide, this product should focus on new users be able to be read top-to bottom rather than as a reference or as a how-to document (i.e., the “background reading” before a classroom assignment). A potential outline for this component of the user’s guide is as follows:

1.  Where VisionEval fits in the planning process  
    a.  Comparison with other tools (e.g., strategic planning, level of detail, policy breadth)  
    b.	Companion tools (e.g., place types_USA, ITHIM health, etc.)  
2.  Framework Design  
3.  Intro to each model and purpose (e.g., methods and influencing factors)  
4.  Discussion of model differences, commonalities, modules, and data needs  

Some content already exists, including:

-   [*VisionEval system design  document*](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md), reframed to focus on **user** needs rather than **developers.**
-   [*RSPM Quick  Summary*](http://www.oregon.gov/ODOT/Planning/Documents/RSPM-Quick-Summary.pdf), with more detail.
-   The RSPM Handout (`RSPM_handout_20141015.pdf`) is a good example of content, but should also include documentation that documents each module referenced in the model (`RSPM-TFLmodelVariables_May2017.pdf`) and links to module-level documentation on estimation results and validation.
-   ODOT [*Data  checklist*](http://www.oregon.gov/ODOT/Planning/Documents/Appendix-Metropolitan-Data-Decision.pdf) from appendix.

###  Guides
Guides should be what you have on your screen or in your hand when you are ready to start following a particular process.  VisionEval Guides should be oriented towards the Basic User audience in the User situation, but provide additional information (in a tab or sidebar) about the API and code organization for Advanced Users or developers.  

**User Situation**: will be interested in getting the following information from the Guides:
-  How do they install VisionEval and get it running with example data?  
-  How do they clean and setup input data?  
-  How do they set up a VisionEval run? What model definition files do they need to create and how do they go about creating them? How do they develop a model run script? What settings should be selected when and why?  
-  What are typical troubleshooting tactics, and if those don’t work how do they get help?  

**Development and Research Situation**: In addition to the interests as a User, individuals in Developer and Researcher situations will be interested in the following information from the guides:
-  Theories, assumptions, and data the models, packages, and modules are based on.  

General outlines for guides should be:

1.   Before you get started \[ with this guide \]  
2.   Pre-requisites  
3.   Outcomes  
4.   Primary content  

Guides should be togglable between the basic and advanced users as well a different VisionEval versions. They should use example scenarios and data that are packaged with the framework, but call out any gotchas or information that may be important or relevant for other types of data or examples.

Guides will be customized for each model, using reusable content blocks when possible.

#### :large_blue_diamond: Getting Started Guide
This guide walks a user through installation and a tour of both the GUI (Basic User) or API (Advanced User) for using VisionEval to run a model.  Ideally the guide would be accompanied by an example model dataset (see data under product #3).  Definitions and standards should be noted (e.g., basics on common input formats, geography definitions, etc.).  Some content oriented towards Advanced Users currently exists in the [*VisionEval wiki*](https://github.com/gregorbj/VisionEval/wiki/Getting-Started), but should be augmented to use the example model and integrated into the User Guide venue.  Over time, this guide should also be augmented to include a troubleshooting section to aid users through commonly encountered problems when setting it up for the first time.  

#### :large_blue_diamond: Data + Parameter Guide
This guide should walk through input data acquisition, cleaning, and formatting that could easily be used as a template.  It should include common and practical tests of data validity, best practices as well as helpful guidance about where to source data.  For example default vehicle inputs that might be standardized reflecting Federal CAFE vs. CA-led states vehicle programs, or low carbon fuel programs, or reasonable biking diversion ranges, or converting transit funding into transit estimated service inputs. The data guide also walks through the datastore and how it is organized and queried.  This guide will also reference outside tools where appropriate such as the [*PlaceTypes USA*](https://github.com/gregorbj/Placetypes_USA) tool.

#### :large_blue_diamond: Running a VE Model Guide
This guide should discuss how to set up scenarios and definitions, strategies for running scenarios across a decision-space, and should undertake appropriate sanity checks on the output.

#### :large_blue_diamond: Output Analysis Guide
This guide should provide some templates for processing the VisionEval outputs into useful analyses for a handful of situations and scenarios.  Examples include scenario comparisons, decision-space analysis, and translation into the scenario viewer.

### :large_blue_diamond: Module Documentation
Each module or package should include appropriate use, method origination and documentation, and derivation of suggested parameter settings.

### References
References should be designed to easily find specific pieces of information rather than to be read through from top-to-bottom.  

#### Cheatsheets
Using the [*R-Studio
format*](https://www.rstudio.com/resources/cheatsheets/) should be
developed to use as a printed out quick-reference. These could cover
both process and implementation How-To needs.

#### Package and Module Organization
This is discussed primarily in the developer-oriented documentation section.

#### Glossary
A glossary reference of terms and names of models.

### Help!
The Help page should have troubleshooting, frequently asked questions, directions on how to submit a bug, and what to do if they need more help or assistance.

### Course
If the user community grows large enough, we should consider an interactive course structure, which are available to create using frameworks like [*Teachable*](https://teachable.com/).  Existing curriculum for using the tools in classroom settings should be made available for academic use.

## 3 - Developer-Oriented Documentation

The developer site should be the main entry point and point of organization for developers, but some of the information will also be of interest to Advanced Users.

**Developer Situation**: Individuals in this situation are interested in the following issues to be addressed within the developer site:  
-  VisionEval development philosophy and contribution guidelines  
-  Testing, and documentation requirements  
-  Theories, assumptions, and data the models, packages, and modules are based on  
-  Modification strategies: when to adjust data or parameters vs adding a module or a package  
-  How to adjust parameters or an existing module  
-  How to add a module to a package  
-  How to modify or add a model  
-  Licensing  

**Framework Developer Situation**: Individuals in this situation will be interested in everything in the Developer Situation in addition to:  
-  Software development roadmap  
-  Framework governance  
-  Contribution guidelines  
-  Framework software documentation  

One of the main challenges will be organizing developer documentation from potentially many Github repositories that could exist for not only the VisionEval Framework, but supporting packages and other materials as well. For that reason, we suggest creating a web landing page as a central point rather than using a wiki within a specific GitHub repository. This does not preclude the content from living in a GitHub wiki linked to from a webpage, but using a separate, version-controlled webpage gives much greater flexibility in how content is viewed and updated and allows for a better user-experience for documenting multiple versions. In some cases (such as a VisionEval development roadmap) this flexibility isn’t required and thus transitioning to a webpage from wiki is not necessary.

The current [*VisionEval Framework webpage*](https://gregorbj.github.io/VisionEval/) is a good start. It is based in Jeykyll and links to developer information contained in the VisionEval wiki. The following is a list of suggested content that is directly linked to from the page:

1.  Repository README.md
2.  Quick Start
3.  Development principles and design
    a.  Framework
    b.  Models
    c.  Datastore
    d.  Package and module organization
4.  Contributing:
    a.  Developer Orientation
    b.  Contribution process
    c.  Development roadmap
    d.  Testing guide + dataset
    e.  Development vignettes
5.  References:
    a.  API Reference
    b.  API Cheat Sheet
    c.  Style Guide

Each of these items is discussed in more detail below.

### :large_blue_diamond: Repository README.md
Even though similar content will be available in the User’s Guide and other points of entry, the GitHub Read Me (currently in the .md / markdown format) should have at a minimum:

-   Purpose of code and framework
-   Links to main website properties
-   Quick Start and installation guide
-   Authorship, copyrights, and licenses
-   Links to contributing guidelines
-   [*Changelog*](http://keepachangelog.com) of methods and inputs/outputs since since last code version

### :large_blue_diamond: Quick Start
Developer Setup instructions are for the most part already documented in the [*Quick Start wiki*](https://github.com/gregorbj/VisionEval/wiki/Getting-Started), but should be reframed to make sure developers are installing from Github clones.

### :large_blue_diamond: Development Principles and Design
The current [*System Design Document*](https://github.com/gregorbj/VisionEval/blob/master/api/model_system_design.md) does an excellent job, but should be strengthened by referring to an example model that uses a small dataset that can be used throughout all the documentation, the Package Template, and datastore API. Some of this content can be re-used from the user's guide and should, similar to the user's-guide be multidimensional across versions.

### :large_blue_diamond: Package and Module Organization
This needs to be fully documented in order to aid people adding to existing packages or translating from predecessor software packages, we should create a mapping of modules to packages – both existing and planned. Ideally this would happen through an interactive web application and would be universally sensitive to various versions of the framework, models, and packages. The user or module developer would be able to:

-   Query individual modules to learn about inputs it needs, data that needs to be retrieved from the datastore, what modules produce the needed datasets, what the module saves to the datastore.
-   Search on datasets using registered names and also using keywords. This search would provide into on the datasets, what modules use them, and what modules produce them.

### Contributing

#### :large_blue_diamond: Developer Orientation
This page contains a list of all the content a new contributor should review, thus this is somewhat a rehash of that.

#### :large_blue_diamond: Contribution Process
This document that tells you how to contribute. The [*Contribution Criteria*](https://github.com/gregorbj/VisionEval/wiki/Contribution-Review-Criteria), [*Review Team Charter,*](https://github.com/gregorbj/VisionEval/wiki/Review-Team-Charter) and [*Working Together*](https://github.com/gregorbj/VisionEval/wiki/Working-Together) pages contain sufficient content, but one has to read a lot in order to understand the basics from the perspective of a potential outside contributor. The following friendly suggestions try to remedy this:

-   Make “working together” the central document and include diagrams about the repository structure that are currently in the Review Team Charter and add information about governance and variety of teams and projects.
-   Rename Contribution Criteria to Contribution Process and frame it as a step-by-step process.
-   Git branching and versioning can be in its own document. Suggest adding “squash and merge” as a default for merging pull requests

#### :large_blue_diamond: Testing Guide
Most of the content exists in the [*Testing framework*](https://github.com/gregorbj/VisionEval/wiki/Automated-Testing) wiki entry, which has a fairly comprehensive discussion about the testing that is done on the framework itself and the user interface. Additional content is needed in order to document the desired structure and tests for supporting packages and how to implement regression testing with the test dataset.

#### :large_blue_diamond: Test Dataset
There needs to be a VisionEval Test Dataset small enough to store in the GitHub repository for a model (i.e. RSPM). It can be used for doing regression tests as well as understanding how the model works through the various vignettes.

#### :large_blue_diamond: Development Roadmap
The current [development roadmap](https://github.com/gregorbj/VisionEval/wiki/Development-Roadmap)* is fairly comprehensive, but will need to be updated based on migration to the new organizational home and projects that are going to be pursued by the Pooled Fund.

### :large_blue_diamond: Development Vignettes
Three types of vignette guides would be useful:
1.    adding a new package using package template
2.    adding a module to existing package
3.    making changes to existing module

### References

#### :large_blue_diamond: Style Guide  
The [Style Guide](https://github.com/gregorbj/VisionEval/blob/master/api/Coding_Guidelines.md) is comprehensive, but should be shortened to be more consumable. In particular, a “not that, but this” table at the top would be helpful to have at the top of the document.

#### :large_blue_diamond: API Functions Reference
This is an exhaustive list of all the API functions, as [*currently exists.*](https://github.com/gregorbj/VisionEval/blob/master/api/functions_summary.md)

#### :large_blue_diamond: API Cheat Sheet
This does not currently exist, but should include a list
of useful methods within the VisionEval API and examples of how to use them. If deemed useful enough, this could also be formatted into a downloadable “cheat sheet”. This would be a compliment to the complete API documentation of each function which currently exists.

# Priorities
VisionEval has had a strong start on documentation geared towards developers, so the priority for documentation needs to shift to getting basic coverage for awareness and user situations.

## Applier Audience

1.  **User’s Guides**.  Start by outlining the various Guides. Design the framework so the Basic (less-technical) User audience sees less-technical documentation (e.g., RSPM User Guide appendix 2), but Advanced Users can drill down as much as possible into the actual code, which should be as self-documenting as possible. Contributors (including ODOT and consultants) can begin populating the VisionEval Guides with what we know today; with the understanding that some things will change in forthcoming versions.
2.  **VE in a Nutshell**. This high-level read from a user perspective could built on content in the *RSPM Quick Summary document* and would include a good explanation of the strategic planning model and inputs and a table of influencing factors and key differences between VE and other tools.

## Developer Audience

1.  **Example Datasets**.  Datasets for each model would enable testing and showcasing of working modules.
3.  **Contribution Vignettes**. Vignettes explain components and provide an example of code documentation vest practices.  More of these facilitate and enable contributions from other sources.

## Awareness Audience

1.  **Video explaining two-way scenario viewer**. This would facilitate awareness of a compelling reason to use strategic tools.  However, it may be best completed after a User Experience design review of the two-way viewer.
