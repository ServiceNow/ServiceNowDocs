---
title: Add a participant to a scenario analysis
description: Add a participant to the scenario analysis first and then add the scenario event, services, issues, and so on. If you are the scenario analysis owner, you can add the stakeholders and reviewers to the scenario analysis in Operational Resilience Workspace. You can then collate the observations of all participants and monitor their responses to analyze the scenario.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/add-a-participant-to-the-scenario-event.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Enable the legacy scenario analysis flow, Legacy scenario analysis, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a participant to a scenario analysis

Add a participant to the scenario analysis first and then add the scenario event, services, issues, and so on. If you are the scenario analysis owner, you can add the stakeholders and reviewers to the scenario analysis in Operational Resilience Workspace. You can then collate the observations of all participants and monitor their responses to analyze the scenario.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All scenario analysis** and select the scenario analysis that you own.

2.  Create a participant on the scenario analysis record.

    1.  On the **Participants** tab of the scenario analysis, select **New**.

        The Create Participant form is displayed.

        The name of the scenario analysis is auto-filled by default.

    2.  In the **Participant** field, select a participant from the list.

        The **Role** field is filled in with a default role. You can change it if needed.

    3.  In the **Instruction** field, add instructions for the participant.

    4.  Select **Save**.

        The participant is now available to be added to any scenario event within this scenario analysis.

3.  On the **Scenario events** tab, open a scenario event, and then on the **Participants** tab of the scenario event, select **Add** to associate the participant with the event.

    **Note:** In the legacy scenario analysis flow, creating a participant from a scenario event is not supported. You create participants from the scenario analysis. If you select **New** on the **Participants** tab of a scenario event, the **Participant**, **Role**, and **Instruction** fields are read-only. You must create the participant on the scenario analysis, as described in the previous step, and then use **Add** here to select it from the list. You can't add the same participant to a scenario event more than once.

    When the scenario analysis is in the **Analyze** state and you add a participant to a scenario event, a response task is created for the participant.

    An email notification is also sent to the participant.

    On the **Responses** tab, the response task details are displayed. These details include the response task number, assigned participant name, and task state.

4.  On the **Responses** tab, fill in the fields.

    1.  Log in as the assigned user and update the impact duration in the **Impact Duration** field.

    2.  Add notes in the **Observation**, **Gap**, and **Recommendation** fields.

    3.  Modify the dependencies and scope for the scenario analysis response.

    4.  To save the scenario analysis response, select **Save**.

    5.  To mark the scenario analysis response as complete, select **Complete**.

        The state of the scenario analysis response is updated to **Closed Complete**.

    6.  Log out from the scenario analysis response record.

    For the descriptions of the field values on the scenario analysis response task form, see [Scenario analysis response task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/response-task-form.md).

5.  Log in as the owner of the scenario event.

6.  On the **Dependencies** tab, add a dependency for the scenario event.

7.  On the **Scope** tab, add the scope for the scenario event.

8.  On the **Issues** tab, select the issues that are associated with the event.

9.  Verify that the open response task is complete.

10. Verify that the **Potential start date time** and **Potential end date time** are filled in for the scenario event.

11. Update the state of the scenario event from **Draft** to **Completed**.


## What to do next

To associate an issue or operational vulnerability with the scenario analysis, see [Link issues and operational vulnerabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/add-an-issue-to-the-analysis.md).

