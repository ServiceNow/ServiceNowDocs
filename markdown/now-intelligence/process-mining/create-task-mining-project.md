---
title: Create Task Mining project
description: Generate a Task Mining project analysis from the Process Mining Workspace by selecting a process flow node.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Task Mining, Integration, Activate, Process Mining, Platform Analytics]
---

# Create Task Mining project

Generate a Task Mining project analysis from the Process Mining Workspace by selecting a process flow node.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.admin, or sn\_tm\_core.power\_user

Creating a Task Mining project enables you to get task-level insights across workstation apps, including third parties. You can create a Task Mining project either from the Analyst workbench or the Opportunity details page of Process Mining. The integration preserves traceability between process-level insights and task-level findings, avoiding fragmented analysis and reducing navigation between tools.

**Important:** To create a Task Mining project from Process Mining, you must have the Task Mining \(sn\_tm\_core\) plugin installed and configured. For more information, see [Configuring Task Mining](../../task-mining/concept/configuring-task-mining.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Select the project you want to create a Task Mining analysis for.

    **Note:** Ensure that your project table is not be in the promin.task\_mining.blocked.tables property.

3.  Select a node on the graph from the Analyst workbench.

    A window is displayed with details related to the node.

    Alternately, you can select the Task Mining tab on the Opportunity details page. Select an improvement opportunity, and then select **Create project** on the page.

    ![Create Task Mining project from Opportunity details tab](../image/tm-opp-det.png)

4.  Select **Create project** in the Task Mining section.

    ![Create Task Mining project from Analyst Workbench](../image/tm-analyst-wrkb.png)

    The project summary page is displayed with project details and task scope auto-populated. A list of workstation users whose activity data you must collect is generated. For more information on Task Mining projects, adding users, and collecting workstation activity, see [Defining the scope of Task Mining projects](../../task-mining/concept/managing-projects.md).

    ![Project summary](../image/tm-project-summ.png)

5.  Select the users whose data you want to collect.

6.  Select **Create project**.

    A notification is displayed when the project is created and ready to use.

7.  Select the Associated projects icon ![](../image/icon-asso-proj.png) from the right pane.

    A list of Task Mining projects associated with the Process Mining project is displayed.

8.  Select **View project** for the project you created.

    The project opens in the Task Mining Workspace. For information on Task Mining analyses, see [Task Mining analyses](../../task-mining/concept/task-mining-dashboard.md). After project creation once the analysis becomes available, we can view the task mining user activity dashboard for the selected list of users by clicking **View project**.

    You can also create a draft project, and continue project creation later from the Associated projects section.


## What to do next

Run a mining job to generate a project analysis. Using categorization, refine the presentation of the project data and share your analysis. For more information, see [Generating a project data analysis](../../task-mining/concept/mining-a-task-mining-project.md).

**Parent Topic:**[Integration with Task Mining](integration-taskmining.md)

**Related topics**  


[Categorize workstation activities to simplify analysis](../../task-mining/task/define-default-categorization-rules.md)

