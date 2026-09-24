---
title: Add a scenario event
description: Add a scenario event to the scenario analysis and analyze its impact on the business service. By adding the participants, dependencies, services, issues to the scenario analysis in Operational Resilience Workspace, you can determine the impact of the scenario event on the business service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-a-scenario-event.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Adding a scenario event to the analysis, Enable the legacy scenario analysis flow, Legacy scenario analysis, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
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

        For the descriptions of the field values on the Scenario event form, see [Scenario event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sce-event-form.md).

        In the **Scenario events** tab, the selected scenario event is displayed.

3.  Open the scenario event from the list.

    The scenario event form is displayed as shown in the following example.

    \[Omitted image "sce-event-form.png"\] Alt text: Scenario event form.

4.  On the **Participants** tab in the scenario event form, select **Add** to associate an existing participant with the scenario event.

    **Note:** The **Participant**, **Role**, and **Instruction** fields are read-only if you try to create a participant directly from the Participants tab of a scenario event. You must first create the participant on the **Participants** tab of the scenario analysis, and then select **Add** here to associate it with the scenario event. For more information about creating a participant, see [Add a participant and monitor the responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/add-a-participant-to-the-scenario-event.md).

    1.  Select **Add**.

        A dialog displays the participants that were previously created on the scenario analysis.

    2.  Select the required participant from the list and select **Add**.

        The participant is added to the scenario event. A response task is automatically created for the participant, and an email notification is automatically sent to the participant.

5.  On the **Responses** tab, select the response task and on the form, fill in the fields.

    1.  Complete the open response task and select **Complete**.

        The response task is completed and the state of the response task is updated to **Closed Complete**.

    On the **Responses** tab, the details of the response task such as the response task number, name of the assigned participant, and state of the response task are displayed. For the descriptions of the field values on the scenario analysis response task form, see [Scenario analysis response task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/response-task-form.md).

6.  On the **Dependencies** tab, select **Add** to add a dependency or select **Add scope related dependency** for the scenario event.

7.  On the **Scope** tab, select **Add** to add the scope or select **Add dependency related scope** for the scenario event.

8.  On the **Issues** tab, select the issues that are associated with the event.

9.  Log in as an owner of the scenario analysis, navigate to the open scenario event, and update its state from **Draft** to **Completed**.

10. Update the **Potential start date time** and **Potential end date time**.

    The scenario event form is displayed.


## Result

The state of the scenario analysis is updated to **Analyze**.

