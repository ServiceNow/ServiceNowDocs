---
title: Assignment workbench overview
description: The assignment workbench enables customer service managers to assign tasks to agents efficiently and intelligently. The workbench uses configurable criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking. Managers can view these results and click one button to assign a task.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Customer Service Management]
---

# Assignment workbench overview

The assignment workbench enables customer service managers to assign tasks to agents efficiently and intelligently. The workbench uses configurable criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking. Managers can view these results and click one button to assign a task.

The assignment workbench displays all the relevant information for task assignment, including:

-   A list of the agents in the task assignment group.
-   The matching criteria used to evaluate the agents.
-   An overall ranking for each agent in the assignment group.
-   A filter with the current assignment group and the skills identified for the task, including any mandatory skills.

![Task Assignment Workbench displaying suggested team members, their skills, availability, and assigned cases.](../image/CaseAssignWorkbench.png "Assignment Workbench")

Agents are ranked from 1 to any number based on the criteria configured for the workbench. The more criteria that matches, the higher an agent's rank. When the criteria for two agents is the same, the agents have the same rank. Point to an agent's rank to display the details.

Use the filter to change the assignment group and to add or remove skills. Changes to the assignment group or to the skills lists are reflected immediately in the workbench:

-   Changing the assignment group displays a different list of agents.
-   Adding or removing skills can change the agent ranking.

If you are using the [mandatory skills](configure-mandatory-skills-feature.md) feature, the agents displayed in the assignment workbench are filtered by the skills in the **Mandatory Skills Added** list and then ranked by the other matching criteria.

**Note:** Agents cannot add or remove mandatory skills or make a skill not mandatory.

## Configuring the assignment workbench

The assignment workbench configuration is stored in a matching rule that is based on the **Selection criteria** matching type. The default configuration uses the **Recommendation for Case Assignment** matching rule, which includes three of the four default matching criteria:

-   Availability Today
-   Matching Skills
-   Assigned Cases

Based on these matching criteria, the workbench calculates and displays an overall rank for each agent in the group. You can modify or create matching criteria and the **Recommendation for Case Assignment** matching rule as needed or you can create your own configuration following these steps:

1.  Create one or more matching criteria.
2.  Create a matching rule with the **Selection criteria** matching type.
3.  Open the matching rule and add the desired matching criteria.

If you are using mandatory skills, you must replace the **Matching Skills** criterion in this matching rule with the **Matching Skills - Mandatory Skills Support** criterion to match agents with mandatory skills required for a case.

## Using the assignment workbench

Access the assignment workbench by clicking the Find Agents icon \(![Find Agents icon.](../image/FindAgentsIcon.png)\) next to the **Assigned to** field on the task form.

**Note:** The state of the current record determines the availability of the Find Agents icon. The icon is available for records in the **Open**, **Awaiting**, and **Cancelled** states, and if the user has write access for the **Assigned to** field. The icon is not available for records in the **New** or **Closed** states or when the **Assigned to** field is read-only for the current user.

Sort the list of agents by any of the matching criteria by clicking the desired column header, which reorders the suggested agents based on the selected criteria.

Select a different assignment group from the **Group** list in the filter. The list of agents is updated based on the selection. If the selected group does not contain any agents, a message is displayed to select another group.

Add or remove skills from the **Skills** list in the filter. These selections are reflected in the **Matching Skills** column.

Skills that have been identified as mandatory for a task are displayed in the **Mandatory Skills Added** list. These selections are also reflected in the **Matching Skills** column. You cannot add or remove skills from this list.

Select an agent and click **Assign** to assign the task. The workbench closes and returns to the Case form. The **Assigned to** field is updated with the selected agent. Click **Save** on Case form to save this assignment.

## Plugins

The Assignment Workbench plugin \(com.snc.assignment\_workbench\) is activated as part of Customer Service Management.

The Case Assignment Workbench Demo plugin \(com.snc.case\_assignment\_workbench\_demo\) provides demo data for the workbench.

## Tables

Assignment Workbench adds the following tables.

<table id="table_mtm_mmc_mkc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Matching Criteria\[matching\_dimension\]

</td><td>

Stores the matching criteria that can be used to create a configuration for the assignment workbench.

</td></tr><tr><td>

Select Criteria\[matching\_dimension\_for\_assignment\]

</td><td>

Stores the matching criteria for an assignment workbench configuration matching rules.

</td></tr><tr><td>

Matching Rule\[matching\_rule\]

</td><td>

Stores matching rules, including the matching rules that configurations for the assignment workbench.

</td></tr></tbody>
</table>## User Roles

Assignment Workbench adds the following roles.

<table id="table_bxx_zpb_kt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Assignment workbench\[assignment\_workbench\]

</td><td>

Provides access to the assignment workbench for customer service agents and consumer service agents.

</td><td>

Skill user\[skill\_user\]

</td></tr></tbody>
</table>## Properties

Assignment Workbench adds the following properties.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignment\_workbench.find.agents.title

</td><td>

Title for the macro button.-   Type: string
-   Default value: Find Agents
-   Location: **Routing and Assignment** &gt; **Properties**

</td></tr><tr><td>

assignment\_workbench.new.window

</td><td>

When enabled, opens the assignment workbench in a new window. -   Type: true \| false
-   Default value: false:
-   Location: **Routing and Assignment** &gt; **Properties**

</td></tr><tr><td>

assignment\_workbench\_no\_of\_agents

</td><td>

Number of agents per page. \(To get better performance, do not use more than 50 agents per page.\)-   Type: choice list
-   Default value: 30
-   Location: **Routing and Assignment** &gt; **Properties**

</td></tr></tbody>
</table>**Related topics**  


[Configure assignment workbench](../task/configure-assignment-workbench.md)

