---
title: Create a scenario analysis
description: Create a scenario analysis for the business service in Operational Resilience Workspace. You can analyze the impact of the scenarios and associated events. You can then calculate the disruptions and determine if any of your services are breached.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Conducting a scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a scenario analysis

Create a scenario analysis for the business service in Operational Resilience Workspace. You can analyze the impact of the scenarios and associated events. You can then calculate the disruptions and determine if any of your services are breached.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

If you have the sn\_oper\_res.manager role, you can create a scenario analysis. Only the owner of the scenario analysis and the user with the sn\_oper\_res.admin role can edit the analysis. After you review the analysis, you can request an approval. When the analysis is in the **Approved** state​, you can close it.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace**, select the list icon ![List icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\) and then navigate to **All scenario analysis**.

2.  To create a scenario analysis, select **New**.

    The Create New Scenario analysis form is displayed.

3.  In the Scenario analysis panel, enter the name, description, and goal for the scenario analysis.

    The number for the scenario analysis is auto-filled by the system.

4.  In the **Analysis start date** field in the Milestones panel, enter the start date for the analysis in the **YYYY-MM-DD HH:mm:ss** format.

    Participants receive a notification link to access the record in the Operational Resilience Workspace and start their analysis on the Analysis start date.

5.  In the **Plan approver** field in the Assignees panel, select the plan approver for the analysis.

6.  In the **Analysis approver** field, select the owner, plan approver, and analysis approver for the analysis.

    The logged-in user is automatically assigned as the owner of the analysis.

    For the descriptions of the field values on the User New record form, see [Create New Scenario analysis form](../reference/scenario-analyses-reference-in-ws.md).

    A sample scenario analysis form is shown in the following example.

    ![Sample scenario analysis form.](../image/sce-analysis-form-in-ws.png "Sample scenario analysis form")

7.  To start a Sidebar discussion on the scenario analysis, select **More actions** and select **Discuss**.

    1.  Add the subject for the discussion and add participants that have access to the record.

    2.  Include a brief message for the participants.

    3.  Select **Start discussion**.

8.  To delete the scenario analysis, select **Delete**, confirm the deletion, and select **OK**.

9.  To save the scenario analysis, select **Save**.


## Result

The scenario analysis is saved and its state is updated to **Draft**.

The following example shows that on the **Details** tab, you can see the details about the scenario analysis, its important dates, and assignees.

![Details tab on the scenario analysis form.](../image/updated-scenario-analysis-form.png "Details tab on the scenario analysis form")

## What to do next

Add the scenario events, scope, assets, and participants to the analysis. You must associate at least one scope to begin the analysis. For more information on adding a scope and dependencies, see [Associate a scope and define the dependencies](add-service-event-participant-to-analysis-in-ws.md).

