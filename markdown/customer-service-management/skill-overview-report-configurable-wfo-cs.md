---
title: Skills Overview in Workforce Optimization for Customer Service
description: Use Skills Overview to analyze skill data such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/skill-overview-report-configurable-wfo-cs.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Coaching, Coaching, Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Skills Overview in Workforce Optimization for Customer Service

Use Skills Overview to analyze skill data such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.

Access Skills Overview from the Teams application:

1.  Go to **Workspaces** &gt; **Manager Workspace**.
2.  Click the Teams icon \[Omitted image "teams-icon.png"\] Alt text: Teams icon..
3.  Select a team.
4.  Click the **Skills** tab.
5.  Select a skill.

You can access the Skills Overview page when you click on a skill in a user profile page in any Workforce Optimization for Customer Service application.

**Note:** You must enable the Coaching With Learning application to view the reports from the application. For enabling this application, see [Activate Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/request-configurable-wfo-cs.md).

\[Omitted image "skills-overview-new.png"\] Alt text: Skill overview page displaying a skill assigned to tasks, agents, on-call experts, and a pie chart of skill coverage experience level dispersal.

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
-   The mean time taken to resolve incidents for that skill.
-   Visualize how many users you have at different skill levels.

</td></tr></tbody>
</table>## Indicators

MTTR of incidents of skill - Mean time taken to resolve incidents with this skill.

## Breakdowns

The indicator is broken down by Skill.

## Components

<table id="table_qsw_cz5_v4b"><thead><tr><th>

Component Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill Overview Container \[sn-manager-skill-overview-container\]

</td><td>

Visualization components

</td><td>

Contains the following components:-   Reports
-   Mean Time to Resolution \(MTTR\) indicator
-   Skill Coverage pie chart
-   Content tree
-   Skill Experts components

</td></tr><tr><td>

Skill Tree Connected \[sn-manager-skill-tree-connected\]

</td><td>

Tree

</td><td>

Displays the skill hierarchy. If the selected skill does not have a skill hierarchy then the component will not display on the Skill Overview page.

</td></tr><tr><td>

Skill Experts \[sn-manager-skill-experts-connected\]

</td><td>

List

</td><td>

Displays all users who are at the expert level for the skill.

</td></tr><tr><td>

Skill Coverage \[now-uxf-visualization-connected\]

</td><td>

Pie-chart

</td><td>

Displays the percentage as well as the number of users with different levels of expertise for the skill.

</td></tr></tbody>
</table>## Reports

**Important:** The Pending Users and Assigned Tasks reports display when you enable the Coaching with Learning application from the ServiceNow® Store. To enable this application, see [Activate Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/request-configurable-wfo-cs.md).

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Assigned Users|\[Omitted image "single-score-sm.svg"\] Alt text: Single score icon.|User Skill \[sys\_user\_has\_skill\]|The number of users who have the selected skill assigned to them.|
|Assigned Tasks|\[Omitted image "single-score-sm.svg"\] Alt text: Single score icon.|Task Skill \[task\_m2m\_skill\]|The number of tasks for which this skill has been assigned.|
|Pending Users|\[Omitted image "single-score-sm.svg"\] Alt text: Single score icon.|Pending Users \[sn\_lc\_learning\_task\]|The numbers of users who are yet to be assigned the selected skill from the learning task.|
|Course Items|\[Omitted image "single-score-sm.svg"\] Alt text: Single score icon.|Learning Course Item \[sn\_lc\_course\_item\]|The number of internal and external courses that have the skill associated with the course item.|

**Parent Topic:**[Using Coaching in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/coaching-configurable-wfo-cs.md)

