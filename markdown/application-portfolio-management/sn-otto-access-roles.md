---
title: Now Assist for Enterprise Architecture \(EA\) access roles
description: The following roles help you to configure and use each Now Assist for Enterprise Architecture \(EA\) skill.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-17"
reading_time_minutes: 8
breadcrumb: [Configure, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Now Assist for Enterprise Architecture \(EA\) access roles

The following roles help you to configure and use each Now Assist for Enterprise Architecture \(EA\) skill.

Access to Now Assist for Enterprise Architecture \(EA\) skills is controlled by a combination of the EA Workspace role assigned to the user and, in some cases, additional platform-level or feature-specific roles. The table summarizes each skill, the role required to use it, and whether additional roles are needed.

|Skill|Configure role|Use role|
|-----|--------------|--------|
|Configure Now Assist for EA \(all skills\)|admin|Not applicable|
|Configure AI Data Explorer and Query Generation skills|now\_assist\_explorer\_admin or higher \(AI Data Explorer\); admin \(Query Generation\)|Not applicable|
|Generate a summary for ADRs \(ADR doc summarization\)|admin|sn\_apm.apm\_user|
|Elaborate or shorten content in ADRs|admin|sn\_apm.apm\_user|
|Generate insights into business applications|admin|sn\_apm.apm\_user|
|Compare Enterprise Modeling and Visualization diagrams|admin|sn\_apm.apm\_read and sn\_apm.apm\_user|
|Elaborate or shorten content in form fields \(Refine text\)|admin|sn\_apm.apm\_user|
|Generate insights for EA Workspace dashboard widgets \(AI Data Explorer\)|now\_assist\_explorer\_admin or higher|sn\_apm.apm\_user or sn\_apm.apm\_read; now\_assist\_explorer\_user|
|Register a business application using conversational experience|admin|None \(any authenticated user\)|
|Register a digital integration using conversational experience|admin|None \(any authenticated user\)|

## Configuration

All Now Assist for EA skills are configured from the Now Assist Admin console. Configuration requires the admin role or, for AI Data Explorer skills, the now\_assist\_explorer\_admin role.

<table id="table_section_config"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Activate and configure all Now Assist for EA skills from the Now Assist Admin console \(ADR summarization, business application insights, diagram change analysis, refine text, conversational experience\)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure skill availability conditions \(always available or custom conditions\)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure role-based access to individual skills

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Define and configure custom parameters for the business application insights prompt; make a copy of the business application insights skill

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate and configure conversational experience skills for registering business applications and digital integrations through Virtual Agent

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure Query Generation skills \(Analytics query generation and Analytics hidden insights generation\)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Activate and configure AI Data Explorer skills \(Analytics exploration, Exploration summarization, Refine text in exploration, Data visualization generation\)

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Configure AI Search for dashboard insight generation

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr></tbody>
</table>## ADR doc summarization and actions

ADR skills are powered by the ADR Doc Summarization and Actions skill. The skill must be activated by an admin before use.

<table id="table_section_adr"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Generate a Now Assist summary of an ADR document from the Artifact content tab

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Elaborate selected text in an ADR document

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Shorten selected text in an ADR document

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Summarize selected text in an ADR document

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Use the Refine button to further elaborate or shorten generated content

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Insert generated content into the ADR record; copy generated summary text

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Use the ADR summarization skill

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

sn\_apm.apm\_read is in the default skill access list. Admins can modify role access from the Now Assist Admin console.

</td></tr></tbody>
</table>## Business application insights

The business application insights skill generates context-aware summaries and actionable insights for business applications. Insights automatically include contextual data from the page where they are generated.

<table id="table_section_ba_insights"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Generate insights from the business application details page

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Generate context-aware insights from the Business Portfolio page \(capability context, cross-capability impact, indicator scores, fiscal period\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Generate context-aware insights from the Application Rationalization bubble chart \(axis metrics, quadrant position, bubble size metric, planned disposition, fiscal period\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Generate context-aware insights from the Application Rationalization list view \(indicator scores, actual scores, fiscal period, connected demands\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

View insights in a side panel wherever business application details are shown

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Refresh generated insights after updating business application data

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Provide thumbs up or thumbs down feedback on generated insights

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr></tbody>
</table>## Compare Enterprise Modeling and Visualization diagrams

The diagram change analysis skill generates an AI summary of changes between two diagram versions, including an executive summary and a breakdown of added, modified, and removed shapes and relationships.

<table id="table_section_diag_compare"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Select two diagram versions to compare from the Compare versions pop-up window

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required. Neither role alone is sufficient to use this skill.

</td></tr><tr><td>

View the AI-generated executive summary of changes between two diagram versions

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr><tr><td>

View a breakdown of shapes, entities, and relationships that have been added, modified, or deleted

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr><tr><td>

View visual canvas highlights \(new shapes and lines in green, modified in yellow\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr><tr><td>

Change the diagram versions and regenerate the comparison summary

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr><tr><td>

Refresh the summary after changing the primary diagram version

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr><tr><td>

Copy the generated change summary; provide helpful or not helpful feedback

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td>

Both sn\_apm.apm\_user and sn\_apm.apm\_read are required.

</td></tr></tbody>
</table>## Elaborate or shorten content in form fields \(Refine text\)

The Refine text skill is available in the Description and Reasoning fields on forms for business applications, business capabilities, business processes, value stream stages, and information objects.

<table id="table_section_refine_text"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Elaborate or shorten text in the Description field of a business application

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Elaborate or shorten text in the Description field of a business capability, business process, value stream stage, or information object

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Generate reasoning content for the Reasoning field \(Planned Disposition section\) of a business application by entering prompts in the text box

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr><tr><td>

Elaborate or shorten existing text in the Reasoning field

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

 

</td><td align="center">

 

</td><td>

 

</td></tr></tbody>
</table>## Generate insights for EA Workspace dashboard widgets

The dashboard insights feature uses the AI Data Explorer and Query Generation skills to provide a conversational interface for querying and analyzing EA Workspace dashboard data. Both an EA Workspace role and the now\_assist\_explorer\_user role are required.

<table id="table_section_dashboard"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Use the Explore with AI icon on any supported dashboard widget to open the AI Data Explorer

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires an EA Workspace role \(sn\_apm.apm\_user or sn\_apm.apm\_read\) AND now\_assist\_explorer\_user. AI Data Explorer and Query Generation skills must be activated and AI Search must be configured.

</td></tr><tr><td>

Ask natural language questions about data from a single dashboard widget

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Perform trend analysis queries \(for example, how application counts changed over time\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Perform comparative queries \(for example, application counts across different technology types\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Perform specific metric queries \(for example, which application family is most used\)

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Use Standard analysis or Extended analysis mode

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Add the widget data to an exploration for Now Assist to generate its own insights

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Define a goal to improve the quality of generated insights; ask follow-up questions based on Now Assist suggestions

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr><tr><td>

Summarize generated insights; share, duplicate, or delete generated insights

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td align="center">

![Yes](../../application-portfolio-management/image/eaw-image/icon-check-mark-green.png)

</td><td>

Requires EA Workspace role AND now\_assist\_explorer\_user.

</td></tr></tbody>
</table>## Conversational experience \(Virtual Agent\)

The conversational experience skills let any authenticated user register business applications or digital integrations through a natural language chat interface in any application that supports Virtual Agent. No EA Workspace role is required.

<table id="table_section_conv_exp"><thead><tr><th>

Capability

</th><th align="center">

admin

</th><th align="center">

now\_assist\_explorer\_admin

</th><th align="center">

sn\_apm.apm\_user

</th><th align="center">

sn\_apm.apm\_read

</th><th align="center">

now\_assist\_explorer\_user

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Register a business application through Virtual Agent by providing details such as name, description, IT owner, business owner, category, and application type

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

No role required. Any authenticated user can access this skill. A Virtual Agent-enabled application such as the Employee Center must be installed. The conversational experience must be configured by an admin.

</td></tr><tr><td>

Register a digital integration through Virtual Agent by providing details such as subscriber business application, provider digital interface, IT owner, and description

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

No role required. Any authenticated user can access this skill. A Virtual Agent-enabled application must be installed and configured by an admin.

</td></tr><tr><td>

Use short or elaborate natural language instructions — Virtual Agent maps the provided context to the appropriate catalog item fields automatically

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

No role required.

</td></tr><tr><td>

Skip non-required fields during the conversational registration flow

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

No role required.

</td></tr><tr><td>

Review and modify the auto-populated form fields before submission

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td align="center">

 

</td><td>

No role required.

</td></tr></tbody>
</table>**Parent Topic:**[Configure Now Assist for Enterprise Architecture \(EA\)](../task/configure-now-assist-ea.md)

**Related topics**  


[Configure Now Assist for Enterprise Architecture \(EA\)](../task/configure-now-assist-ea.md)

[Configure AI Data Explorer and Query Generation skills](../task/configure-ai-data-explr-qry-genr-skills.md)

[Now Assist for Enterprise Architecture \(EA\)](../concept/now-assist-ea.md)

[Enterprise Architecture Workspace access roles](../../application-portfolio-management/reference/eaw-reference/eaw-access-roles.md)

[Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow](../concept/now-assist-aiagents-ea-diagramming-usecase.md)

