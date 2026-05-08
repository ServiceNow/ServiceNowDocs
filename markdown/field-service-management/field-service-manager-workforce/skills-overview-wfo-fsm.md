---
title: Skills Overview in Workforce Optimization for Field Service
description: Use Skills Overview to analyze skill data, such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.Access Skills Overview from Manager Workspace using either the Scheduling application or the Teams application to analyze skill data.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Coaching, Workforce Optimization, Managing workforce, Use, Field Service Management]
---

# Skills Overview in Workforce Optimization for Field Service

Use Skills Overview to analyze skill data, such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.

The following image illustrates the information displayed on the Skills Overview main page, which includes different types of data based on skill such as the overall skill coverage and a skills hierarchy.![Skills Overview with user and skill information organized in tiles. Additionally, there is a pie chart depicting skill coverage.](../image/Skills-overview-teams.png)

## Use cases

<table id="table_m1n_xnm_v4b"><thead><tr><th>

User

</th><th>

Landing page use

</th></tr></thead><tbody><tr><td>

Skill Admin \[skill\_admin\]

</td><td>

-   Analyze all experts available for each skill.
-   Drill down into the skill hierarchy.
-   Number of skills assigned to users and tasks.
-   Mean time taken to resolve incidents for that skill.
-   Visualize how many users you have at different skill levels.

</td></tr></tbody>
</table>## Indicators

MTTR of incidents of skill - Mean time taken to resolve incidents with this skill.

## Breakdowns

The data displayed in the MTTR of incidents of skill indicator is calculated based on the skill used to resolve the incident.

## Reports

**Important:** The Pending Users and Assigned Tasks reports display when you enable the Coaching with Learning application from the ServiceNow® Store. To enable this application, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

<table id="table_r1n_xnm_v4b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned Users

</td><td>

![Assigned Users icon.](../../../reuse/reporting/image/single-score-sm.svg)

</td><td>

User Skill \[sys\_user\_has\_skill\]

</td><td>

The number of users who have the selected skill assigned to them.

</td></tr><tr><td>

Assigned Tasks

</td><td>

![Assigned Tasks icon.](../../../reuse/reporting/image/single-score-sm.svg)

</td><td>

Task Skill \[task\_m2m\_skill\]

</td><td>

The number of tasks for which this skill has been assigned.

</td></tr><tr><td>

Pending Users

</td><td>

![Pending Users icon.](../../../reuse/reporting/image/single-score-sm.svg)

</td><td>

Pending Users \[sn\_lc\_learning\_task\]

</td><td>

The number of users who are yet to be assigned the selected skill from the learning task.

</td></tr><tr><td>

Course Items

</td><td>

![Course Items icon.](../../../reuse/reporting/image/single-score-sm.svg)

</td><td>

Learning Course Item \[sn\_lc\_course\_item\]

</td><td>

The number of internal and external courses that have the skill associated with the course item.

</td></tr><tr><td>

Skill Overview Container

</td><td>

Visualization components

</td><td>

None

</td><td>

Contains the following components:-   Reports
-   Mean Time to Resolution \(MTTR\) indicator
-   Skill Coverage pie chart
-   Content tree
-   Skill Experts components

</td></tr><tr><td>

Skill Tree Connected

</td><td>

Tree

</td><td>

None

</td><td>

The skills hierarchy. If the selected skill does not have a skill hierarchy then the component will not display on the Skill Overview page.

</td></tr><tr><td>

Skill Experts

</td><td>

List

</td><td>

None

</td><td>

All users who are at the expert level for the skill.

</td></tr><tr><td>

Skill Coverage

</td><td>

Pie chart

</td><td>

None

</td><td>

The percentage as well as the number of users with different levels of expertise for the skill.

</td></tr></tbody>
</table>## Access Skills Overview from Manager workspace

Access Skills Overview from Manager Workspace using either the Scheduling application or the Teams application to analyze skill data.

### Before you begin

Role required: skill\_admin

### About this task

You can access Skills Overview from Manager Workspace using the Teams or Shift Scheduling application.

**Note:** You must enable the Coaching with Learning application to view the reports from the application. For information about enabling this application, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Access Skills Overview from either the Teams application or the Shift Scheduling application.

<table id="choicetable_a5f_ty2_hwb"><thead><tr><th align="left" id="d142624e492">

Application

</th><th align="left" id="d142624e495">

Actions

</th></tr></thead><tbody><tr><td id="d142624e501">

**Teams**

</td><td>

1.  Click the Teams icon \(![Teams icon.](../../itsm-manager-workspace/image/teams-icon.png)\).
2.  Select a team from the Field Service group list.
3.  Click the **More** tab and then select **Skills**.
4.  Select a skill from the Skill list.


</td></tr><tr><td id="d142624e540">

**Shift Scheduling**

</td><td>

1.  Click the Schedule icon \(![Schedule icon.](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).
2.  Click the **Team calendar** tab.
3.  Select an agent from the list of users.
4.  Click the **More** tab and then select **Skills**.


</td></tr></tbody>
</table>
### Result

Skills Overview displays the skill data, such as how many skills are assigned to users and tasks along with the data providing the number of experts for a particular skill and the overall skill coverage by your teams.

