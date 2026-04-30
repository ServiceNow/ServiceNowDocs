---
title: Define the workflow states for a privacy case
description: Define the workflow states for a privacy case that govern the lifecycle of the case.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create state model transition, Configure, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Define the workflow states for a privacy case

Define the workflow states for a privacy case that govern the lifecycle of the case.

## Before you begin

Role required: sn\_privacy\_case.privacy\_case\_admin

## About this task

A privacy case typically goes through the following workflow states that can be configured in the Privacy Case Management application:

-   New: The case has been opened and is in the initial stage of review.
-   Triage: The case is being evaluated to determine the appropriate course of action.
-   Investigate: The case is being actively investigated to gather information and evidence.
-   Resolve: The case is being worked on to find a resolution.
-   Post case review: A review of the case is being done after it is resolved.
-   Close: The case is closed and is no longer active.
-   Cancel:The case is cancelled and it is no longer being pursued.

These states can vary depending on the organization's privacy case management process.

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **State Models**.

2.  Open the state model that you created and want to add the workflow for.

3.  On the GRC workflow states context menu, select **New**.

4.  On the form, fill in the fields.

<table id="table_ok4_tfv_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

Name of the workflow state. Choices are the following:-   **New**
-   **Triage**
-   **Investigate**
-   **Resolve**
-   **Post case review**
-   **Close**
-   **Canceled**


</td></tr><tr><td>

Model

</td><td>

State model that uses this workflow state. This field is automatically set to the state model name.

</td></tr><tr><td>

Application

</td><td>

Name of the application this state model applies to. This field is automatically set to **GRC: Privacy Case Management**.

</td></tr><tr><td>

Display type

</td><td>

Display type of the workflow state. Choices are the following:-   **As node**: Display as a parent state.
-   **As sub-level**: Display as a sub-state of the parent state.


</td></tr><tr><td>

Stepper label

</td><td>

Label to be displayed on the stepper component for the state.

</td></tr><tr><td>

Parent model state

</td><td>

Parent state for the sub-level state. This field appears only when **As sub-level** is selected from **Display type**.

</td></tr><tr><td>

Is optional

</td><td>

Option to select the state as optional. This field appears only when **As node** is selected from the **Display type** field.

</td></tr></tbody>
</table>5.  Create the other states similarly.

6.  Select **Submit**.


**Parent Topic:**[Create state model transition](prm-create-state-model-transition.md)

