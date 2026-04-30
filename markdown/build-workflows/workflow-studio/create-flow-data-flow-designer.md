---
title: Create Flow Data action
description: Collect data from agents interacting with a Workspace playbook. Use this data to create reusable activities for process owners using Playbooks.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create Flow Data action

Collect data from agents interacting with a Workspace playbook. Use this data to create reusable activities for process owners using Playbooks.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Definition

</td><td>

Reference.Data Definition\[sys\_flow\_data\_definition\]

</td><td>

Reference to the Data Definition record used to collect data for the flow. Each Data Definition record has a set of Flow Data Variables to store data. For example, the Create Task Data Definition record collects values for Task records.

</td></tr><tr><td>

Assigned To

</td><td>

Reference.User\[sys\_user\]

</td><td>

User responsible for completing the task associated with the Playbooks activity.

</td></tr><tr><td>

Assignment Group

</td><td>

Reference.Group\[sys\_user\_group\]

</td><td>

User group responsible for completing the task associated with the Playbooks activity.

</td></tr><tr><td>

Wait for user input

</td><td>

Choice

</td><td>

Option to prompts Playbooks users to determine if the activity pauses for input in a playbook during runtime. Options include:-   **Yes** - Pause the activity and prompt end users for input
-   **No** - Don't pause the activity for end user input

</td></tr></tbody>
</table>## Outputs

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Flow Data\[sys\_flow\_data\]|Reference to the Flow Data record created from end user input in a playbook activity during runtime.|

## Send Email with user input Activity

![Send Email with user input Activity subflow where step 1 is a sample configuration of the Create Flow Data action.](../images/example-create-flow-data-01.png)

Send Email with user input Activity is a subflow that gathers the information needed to create and send an email. This subflow provides data for the corresponding Playbooks activity. The subflow uses the Create Flow Data action to gather information from the person running the activity. This example configures the Create Flow Data action to use the Email Data Definition record, which includes variables for an email subject and body. The action is also configured to use the subflow inputs for Assigned To and Assignment Group to determine who can enter flow data.

![The Send Email action is configured to use the body variable from the Create Flow Data action as the body of the email.](../images/example-create-flow-data-02.png)

The subflow waits until the Create Flow Data record is in the Complete state before sending an email. The Send Email action is configured to use the body variable from the Create Flow Data action as the body of the email.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

