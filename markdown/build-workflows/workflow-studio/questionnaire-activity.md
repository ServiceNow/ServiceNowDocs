---
title: Questionnaire activity
description: Collects inputs from a user during a playbook run to use later in the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/questionnaire-activity.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Questionnaire activity

Collects inputs from a user during a playbook run to use later in the playbook.

The questionnaire activity replaces the Collect User Data activity, but does not require you to create a data definition. Use the questionnaire activity if:

-   You don't have a table already,
-   You don't need to run reports on the collected data,
-   And you don't need to use the data outside of the playbook.

If you already have a table to store the collected data, use the [Record Form activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/user-form-activity.md).

## Roles and availability

This activity is available as a common activity. Users with pd\_author can add this activity to a playbook.

## Questionnaire

In the **Questionnaire** tab, you can:

-   Add and edit questions for agents to respond to

    **Note:**

    Editing a questionnaire changes the activity definition. Playbook executions already in progress continue to use the questionnaire as it was when the execution started.

-   Control which user or user group has access to submit the questionnaire

To learn more about adding or configuring questions, see [Create a new questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/create-questionnaire.md).

## Editing

## Required questions and skipping

Runtime users can skip a questionnaire activity. Required questions are validated when a user submits the questionnaire, not when they skip it. If a user skips the activity, nothing is submitted and no validation runs. Marking a question as required doesn't prevent a user from skipping the activity.

To require that users complete a questionnaire, remove the skip action from the activity. Marking questions as required doesn't achieve this on its own.A questionnaire displays as read-only if it has no submit action. An action counts as a submit action when **Form fields required** is selected on it.

## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Flow Data|Reference to record containing collected data. Use the pill-picker to dot-walk to **Outputs** &gt; **Record** &gt; **Vars** to see all collected data. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/dot-walking-examples.md).|

-   **[Create a questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/create-questionnaire.md)**  
Create and insert a new questionnaire for agents to respond to.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

