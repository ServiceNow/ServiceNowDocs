---
title: Generating tasks in KPI Composer
description: For each KPI Composer artifact in your project, you can generate a task to create an equivalent Performance Analytics element. All tasks are created with one action. The tasks are assigned automatically to the responsible group for implementing analytics.Assign the tasks in a KPI Composer project to a group. By default, tasks are assigned to the Analytics Implementers assignment group. You can add users and groups to this group, or you can select a different assignment group.Generate tasks for all sufficiently defined KPI Composer artifacts with a single action.KPI Composer tasks are defined in Task Definition \[sn\_kpi\_composer\_task\_definition\] records. When you generate tasks, you create these records or update their statuses.KPI Composer tasks utilize flows created with the ServiceNow AI Platform Flow Designer.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Generating tasks in KPI Composer

For each KPI Composer artifact in your project, you can generate a task to create an equivalent Performance Analytics element. All tasks are created with one action. The tasks are assigned automatically to the responsible group for implementing analytics.

Tasks can be generated to create the following Performance Analytics and Reporting elements based on the definitions in your KPI Composer project. The tasks are generated for each type of element in this order:

-   Breakdowns
-   Reports
-   Interactive Filters
-   Indicators
-   Widgets
-   Spotlight groups
-   Content Blocks
-   Dashboards

**Important:** To generate a task to create an element, the associated KPI Composer artifact definition must include all the required information. For example, to generate a task to create a breakdown or an automated indicator, the Name and the Facts Table must be specified in their definitions.

![Definition of the Priority breakdown showing Name and Facts Table values.](../image/kpi-comp-required-bkdown-info.png "Definition of the Priority breakdown showing required information for tasks")

**Parent Topic:**[Design your Performance Analytics solution with KPI Composer](designing-pa-solution.md)

## Assign KPI Composer tasks

Assign the tasks in a KPI Composer project to a group. By default, tasks are assigned to the Analytics Implementers assignment group. You can add users and groups to this group, or you can select a different assignment group.

### Before you begin

Role required: sn\_kpi\_composer.user, sn\_kpi\_composer.admin, admin

### About this task

All tasks in a KPI Composer project are assigned to the same assignment group. After you generate tasks, the group handles them through its normal workflow.

By default, tasks are assigned to the Analytics Implementers group, which is provided with KPI Composer. This group includes the pa\_admin role by default. Any users whom you add to this group are granted this role. Access this group from **User administration** &gt; **Groups**, or follow the **Analytics Implementers** link on the Tasks tile in the Review tab. You need the user\_admin role to edit this group. For more information about adding and removing users from this group, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

To change the assignment group, follow this procedure:

### Procedure

1.  Open your KPI Composer project.

2.  Open the **Review** tab.

3.  Locate the **Tasks** tile.

4.  Find and select the **Clear** icon next to the name of the current assignment group.

    ![Tasks tile in the Review tab of a KPI Composer project with the cursor on the Clear icon.](../image/kpi-comp-clear-asgmt-group.png)

5.  Confirm that you want to clear the assignment group.

6.  Begin typing the name of the assignment group you want.

    KPI Composer gives you a list of predicted matches.

    ![Typing part of the name of an assignment group and being offered matches.](../image/kpi-comp-new-assgmt-group.png)

7.  Select a group.


### What to do next

Generate tasks to assign them to the selected group.

## Generate tasks

Generate tasks for all sufficiently defined KPI Composer artifacts with a single action.

### Before you begin

-   Populate the Analytics Implementers group with users.
-   Complete designing your KPI Composer project. The necessary artifacts should all be defined. However, if you change something later, you can regenerate the tasks. Regenerating tasks is a good way to track their completion.

Role required: sn\_kpi\_composer.user, sn\_kpi\_composer.admin, admin

### Procedure

1.  Navigate to KPI Composer and open your fully defined project.

2.  Open the Review tab.

3.  Locate the Tasks tile.

4.  Select **Generate tasks**.


### Result

You generate tasks for creating Performance Analytics and Reporting artifacts. These tasks are assigned automatically to the Analytics Implementers assignment group.

### What to do next

View the tasks you have created. In the Tasks tile, you have links to active tasks, tasks on hold, and completed tasks. The links take you to the Task Definitions \[sn\_kpi\_composer\_task\_definition\] table.

## Task Definition records

KPI Composer tasks are defined in Task Definition \[sn\_kpi\_composer\_task\_definition\] records. When you generate tasks, you create these records or update their statuses.

You can access any existing Task Definition records from links on the Tasks tile of the Review tab. These links take you to a filtered list of records, as follows:

<table id="table_onw_z2t_hrb"><thead><tr><th>

Link

</th><th>

Filter

</th></tr></thead><tbody><tr><td>

Active Tasks

</td><td>

-   Project CONTAINS &lt;Your project name&gt;
-   Status in \(Create, Update\)
-   Waiting on dependencies = false

</td></tr><tr><td>

Tasks on hold

</td><td>

-   Project CONTAINS &lt;Your project name&gt;
-   Status in \(Create, Update\)
-   Waiting on dependencies = true

</td></tr><tr><td>

Completed tasks

</td><td>

-   Project CONTAINS &lt;Your project name&gt;
-   Status = OK

</td></tr></tbody>
</table>### Task statuses

When you run the task generator, it determines the status of all tasks. Task generation uses the following logic to create tasks and set their statuses:

1.  Does the KPI Composer artifact still exist? If not, the status is Deleted.
2.  Does the existing KPI Composer artifact have a valid definition? If not, the status is Incomplete.
3.  Does the valid KPI Composer artifact definition link to an existing ServiceNow AI Platform element, such as a Performance Analytics indicator or CMS content block? If not, the status is Create.
4.  If the linked element exists and the status was previously set to OK, was the artifact definition subsequently updated? If so, the status is Update.
5.  Otherwise, if the linked element exists, the status is OK.

![Logic of the task generation job resulting in a task definition record status of: Deleted, Incomplete, Create, OK, or Update.](../image/kpi-comp-task-definition.png)

### Artifact update tracking

Task generation checks all task definitions, including those with the status OK. If the artifact definition has changed since the task status was set to OK, the next task generation job changes the task status to Update. The fields in the artifact definition that are checked for changes depend on the artifact type. Changes to other, related artifacts can also result in the status changing to Update. The following table lists the fields and the related artifacts.

|Artifact definitions|Fields|Related artifact changes|
|--------------------|------|------------------------|
|Breakdown|Condition| |
|Facts Table| |
|Name| |
|Indicator|Aggregation|Added breakdown|
|Condition|Removed breakdown|
|Direction| |
|Facts Table| |
|Formula| |
|Frequency| |
|indicator Type| |
|Name| |
|Report|Aggregation| |
|Condition| |
|Description| |
|Facts Table| |
|Name| |
|Report Source| |
|Source Type| |
|Interactive Filter|UI control type| |
|Title| |
|Description| |
|Interactive filter| |
|PA Widget|Widget type| |
|Visualisation type| |
|Title| |
|Description| |
|Follow element| |
|Time series| |
|Artifacts| |
|Spotlight|Title| |
|Description| |
|Artifacts| |
|Dashboard|Name|Added breakdown|
|Description|Removed breakdown|
| |Changed canvas layout - reorder / delete / add canvas|

## Task flows

KPI Composer tasks utilize flows created with the ServiceNow AI Platform® Flow Designer.

KPI Composer provides two flows to manage the transition between task states:

-   KPI Composer - Analytics Task flow
-   KPI Composer - Task Definition flow

You can modify either of these flows in the Flow Designer. However, rather than modifying them directly, you should copy the flows and modify the copies. Make the copies active and deactivate the provided flows. The reason to do this is that updates to KPI Composer may include updates to the flows. If you change the provided flows, updates to them may fail. Instead, after an update, you can examine the provided flows for changes. Incorporate these changes in your copied flows.

The following diagrams summarize the provided flows:

![KPI Composer - Analytics Task Flow.](../image/kpi-comp-analytics-task-flow.png)

![KPI Composer - Task Definition flow](../image/kpi-comp-task-def-flow.png)

**Related topics**  


[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

