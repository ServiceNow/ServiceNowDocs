---
title: Components installed with Portfolio SAFe
description: Several types of components are installed with activation of the Agile - Scaled Agile Framework - Portfolio SAFe plugin \(com.snc.sdlc.portfolio\_safe\), including tables and user roles.
locale: en-US
release: yokohama
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Portfolio SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Components installed with Portfolio SAFe

Several types of components are installed with activation of the Agile - Scaled Agile Framework - Portfolio SAFe plugin \(com.snc.sdlc.portfolio\_safe\), including tables and user roles.

## Roles installed

<table id="table_cpw_ctr_b2b0"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

SAFe admin\[safe\_admin\]

</td><td>

-   Edits, creates, and deletes SAFe ART, epics, features, stories, and program increments.
-   Has read-only access to SAFe teams.

</td><td>

-   safe\_art\_user
-   safe\_scrum\_master
-   safe\_product\_owner

</td></tr><tr><td>

SAFe portfolio user\[sn\_portfolio\_safe.safe\_portfolio\_user\]

</td><td>

Maintains the portfolio backlog and can edit, create, and delete SAFe epics, features, and stories.

</td><td>

safe\_art\_user

</td></tr><tr><td>

SAFe scrum product owner\[safe\_product\_owner\]

</td><td>

-   Maintains the team backlog and can edit, create, and delete SAFe stories.
-   Has read-only access to SAFe ART, teams, epics, and features.
-   Has read-only access to SAFe program increments.

</td><td>

safe\_story\_creator

</td></tr><tr><td>

SAFe ART user\[safe\_art\_user\]

</td><td>

-   Maintains the ART backlog and can edit, create, and delete SAFe epics, features, stories, and program increments.
-   Edits SAFe teams.
-   Has read-only access to SAFe ART.

</td><td>

safe\_story\_creator

</td></tr><tr><td>

SAFe scrum master\[safe\_scrum\_master\]

</td><td>

-   Edits, and deletes SAFe stories.
-   Edits SAFe teams.
-   Has read-only access to SAFe ART, epics, features, and program increments.

</td><td>

safe\_story\_creator

</td></tr><tr><td>

SAFe scrum user\[safe\_scrum\_user\]

</td><td>

Can view all elements of SAFe, but cannot create, edit, or manage records of any type.

</td><td>

None

</td></tr><tr><td>

SAFe scrum story creator\[safe\_story\_creator\]

</td><td>

-   Edits, creates, and deletes SAFe stories.
-   Has read-only access to SAFe ART, teams, epics, features, and program increments.

</td><td>

safe\_story\_editor

</td></tr><tr><td>

SAFe scrum story editor\[safe\_story\_editor\]

</td><td>

-   Arranges stories within the team backlog using the drag and drop feature.
-   Edits SAFe stories.
-   Has read-only access to SAFe ART, teams, epics, features, and program increments.

</td><td>

-   safe\_scrum\_user
-   rm\_scrum\_task\_admin

</td></tr></tbody>
</table>## Tables installed

<table id="table_dqt_pnp_kcb0"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAFe epic\[sn\_safe\_epic\]

</td><td>

Information about epics.

</td></tr><tr><td>

SAFe feature\[sn\_safe\_feature\]

</td><td>

Information about features.

</td></tr><tr><td>

Agile Release Train\[sn\_safe\_program\]

</td><td>

Information about ART.

</td></tr><tr><td>

Program Increment\[sn\_safe\_program\_increment\]

</td><td>

Information about program increments.

</td></tr><tr><td>

SAFe ART team\[sn\_safe\_program\_m2m\_group\]

</td><td>

Relationships between groups and ART.

</td></tr><tr><td>

SAFe ART Member\[sn\_safe\_program\_member\]

</td><td>

Information about members within an ART.

</td></tr><tr><td>

SAFe ART Sprint\[sn\_safe\_program\_sprint\]

</td><td>

Sprint schedules of teams within the ART.

</td></tr><tr><td>

SAFe ART VTB Board\[sn\_safe\_program\_vtb\_board\]

</td><td>

Records displayed on the ART level, Board tab.

</td></tr><tr><td>

SAFe Scrum Task\[sn\_safe\_scrum\_task\]

</td><td>

Information about SAFe scrum tasks.

</td></tr><tr><td>

SAFe Sprint\[sn\_safe\_sprint\]

</td><td>

Information about sprints.

</td></tr><tr><td>

SAFe Story\[sn\_safe\_story\]

</td><td>

Information about stories.

</td></tr><tr><td>

SAFe PI Objectives\[sn\_safe\_pi\_objective\]

</td><td>

Stores the SAFe PI objectives.

</td></tr><tr><td>

SAFe team predictability measure\[sn\_safe\_pi\_m2m\_group\]

</td><td>

Stores the business value achieved per team from PI objectives which is used for team-level predictability measure data.

</td></tr><tr><td>

Portfolios\[pm\_portfolio\]

</td><td>

Information about portfolios.

</td></tr><tr><td>

Portfolio SAFe VTB board\[sn\_portfolio\_safe\_vtb\_board\]

</td><td>

Records displayed on the portfolio level, Board tab.

</td></tr><tr><td>

SAFe Team VTB Board\[sn\_safe\_team\_vtb\_board\]

</td><td>

Records displayed on the Team level, Board tab.

</td></tr></tbody>
</table>**Parent Topic:**[Portfolio SAFe](../concept/portfolio-overview.md)

**Related topics**  


[Define a portfolio](../task/create-SAFeportfolio.md)

[SAFe Board—Portfolio level](../concept/portfolio-tabs.md)

