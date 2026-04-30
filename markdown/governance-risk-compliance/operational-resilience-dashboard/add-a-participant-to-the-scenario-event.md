---
title: Add a participant and monitor the responses
description: Add a participant to the scenario analysis first and then add the scenario event, services, issues, and so on. If you are the scenario analysis owner, you can add the stakeholders and reviewers to the scenario analysis in Operational Resilience Workspace. You can then collate the observations of all participants and monitor their responses to analyze the scenario.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Conducting a scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a participant and monitor the responses

Add a participant to the scenario analysis first and then add the scenario event, services, issues, and so on. If you are the scenario analysis owner, you can add the stakeholders and reviewers to the scenario analysis in Operational Resilience Workspace. You can then collate the observations of all participants and monitor their responses to analyze the scenario.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All scenario analysis** and select the scenario analysis that you own.

2.  Navigate to the **Participants** tab in the scenario event form and then either add a participant from an available list or add a new participant.

    |Step|Description|
    |----|-----------|
    |**Select __Add__.**|Add a participant from the available list of participants for the scenario analysis.|
    |**Select __New__.**|Add a participant to the scenario event.|

    1.  Select **New**.

        The Create New Participant form is displayed as shown in the following example.

        ![Create a participant for the scenario analysis.](../image/create-new-participant-for-scenario-analysis.png)

        The name of the scenario analysis is auto-filled by default.

    2.  In the **Participant** field, select a participant from the list in the Participant form.

        When you select a participant, the role is auto-filled in the Role field.

    3.  In the **Instruction** field, add instructions for the participant.

    4.  Select **Save**.

        You can view the tabs on the Participant form as shown in the following example.

        ![Tabs on the Participant form.](../image/scenario-events-associated-with-participant.png)

        When you create a scenario event and add a participant to it, a response task is automatically created for the participant. The following example shows that when a participant is assigned to a scenario event, a response task is created.

        An email notification is automatically sent to the participant.

        On the **Responses** tab of scenario analysis responses, the details of the response task such as the response task number, name of the assigned participant, and state of the response task are displayed. An email notification is sent to the assigned user.

3.  On the **Responses** tab, fill in the fields.

    1.  Log in as the assigned user of the scenario analysis response and update the impact duration of the scenario analysis response in days, hours, minutes, seconds in the **Impact Duration** field.

    2.  Add notes in the **Observation**, **Gap**, and **Recommendation** fields.

    3.  Modify the dependencies and scope for the scenario analysis response.

    4.  To save the scenario analysis response, select **Save**.

    5.  To mark the scenario analysis response as complete, select **Complete**.

        The state of the scenario analysis response is updated to **Closed Complete**.

    6.  Log out from the scenario analysis response record.

    For the descriptions of the field values on the scenario analysis response task form, see [Scenario analysis response task form](../reference/response-task-form.md).

4.  Log in as the owner of the scenario event.

5.  On the **Dependencies** tab, add a dependency for the scenario event.

6.  On the **Scope** tab, add the scope for the scenario event.

7.  On the **Issues** tab, select the issues that are associated with the event.

8.  Ensure that the open response task is complete.

9.  Verify that the **Potential start date time** and **Potential start date time** are filled in for the scenario event.

10. Update the state of the scenario event from **Draft** to **Completed**.


## What to do next

To associate an issue or operational vulnerability with the scenario analysis, see [Link issues and operational vulnerabilities](add-an-issue-to-the-analysis.md).

