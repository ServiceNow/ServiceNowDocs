---
title: Add a scenario event
description: Add a scenario event to the scenario analysis and analyze its impact on the business service. By adding the participants, dependencies, services, issues to the scenario analysis in Operational Resilience Workspace, you can determine the impact of the scenario event on the business service.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Adding a scenario event to the analysis, Conducting a scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a scenario event

Add a scenario event to the scenario analysis and analyze its impact on the business service. By adding the participants, dependencies, services, issues to the scenario analysis in Operational Resilience Workspace, you can determine the impact of the scenario event on the business service.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All scenario analysis** and select the scenario analysis that you own.

2.  On the **Scenario events** tab, select **Add**, select an event from the list, and select **Add** again.

    1.  Select **Add**.

    2.  In the Scenario events form, select an event from the list and select **Add**.

        For the descriptions of the field values on the Scenario event form, see [Scenario event form](../reference/sce-event-form.md).

        In the **Scenario events** tab, the selected scenario event is displayed.

3.  Open the scenario event from the list.

    The scenario event form is displayed as shown in the following example.

    ![Scenario event form.](../image/sce-event-form.png)

4.  Navigate to the **Participants** tab in the scenario event form and then either add a participant from an available list or add a new participant.

    |Step|Description|
    |----|-----------|
    |**Select __Add__.**|Add a participant from the available list of participants for the scenario analysis.|
    |**Select __New__.**|Add a participant to the scenario event.|

    1.  Select **New**.

        The Create New Participant form is displayed.

        The name of the scenario analysis is auto-filled by default.

    2.  In the **Role** field, select a role for the participant.

        The following options are available for the role: HR, Legal, Finance, Technology, People, Data, Security, Supplier Tier1, Supplier Tier2.

    3.  In the **Participant** field, select a participant from the list in the Participant form.

        When you select a participant, the role is auto-filled in the Role field.

    4.  In the **Instruction** field, add instructions for the participant.

    5.  Select **Save**.

        When you create a scenario event and add a participant to it, a response task is automatically created for the participant. An email notification is automatically sent to the participant.

5.  On the **Responses** tab, select the response task and on the form, fill in the fields.

    1.  Complete the open response task and select **Complete**.

        The response task is completed and the state of the response task is updated to **Closed Complete**.

    On the **Responses** tab, the details of the response task such as the response task number, name of the assigned participant, and state of the response task are displayed. For the descriptions of the field values on the scenario analysis response task form, see [Scenario analysis response task form](../reference/response-task-form.md).

6.  On the **Dependencies** tab, select **Add** to add a dependency or select **Add scope related dependency** for the scenario event.

7.  On the **Scope** tab, select **Add** to add the scope or select **Add dependency related scope** for the scenario event.

8.  On the **Issues** tab, select the issues that are associated with the event.

9.  Log in as an owner of the scenario analysis, navigate to the open scenario event, and update its state from **Draft** to **Completed**.

10. Update the **Potential start date time** and **Potential start date time**.

    The scenario event form is displayed.


## Result

The state of the scenario analysis is updated to **Analyze**.

