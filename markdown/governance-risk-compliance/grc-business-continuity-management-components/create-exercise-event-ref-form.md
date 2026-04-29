---
title: Create Exercise Event form
description: Use the Create Exercise Event form in BCM UIB Workspace to add details about an Exercise event.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create an exercise, Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create Exercise Event form

Use the Create Exercise Event form in BCM UIB Workspace to add details about an Exercise event.

## Create Exercise Event form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Details tab

</td></tr><tr><td>

Short description

</td><td>

Brief description about the event.

</td></tr><tr><td>

Event type

</td><td>

Type of the event. For exercise events, the event type is **Exercise**.

</td></tr><tr><td>

State

</td><td>

Defaults to the **Pending** state.

</td></tr><tr><td>

Assigned to

</td><td>

User or users from the Assignment group. If the **Assignment group** field is empty, then select any user.

</td></tr><tr><td>

Description

</td><td>

Description of the exercise event.

</td></tr><tr><td>

Impact

</td><td>

Measure of the business criticality of the affected service. Available options are:-   **1 - High**
-   **2 - Medium**
-   **3 - Low**

</td></tr><tr><td>

Priority

</td><td>

Sequence in which an Incident or Problem needs to be resolved, based on impact and urgency. Available options are:-   **1 - Critical**
-   **2 - High**
-   **3 - Moderate**
-   **4 - Low**
-   **5 - Planning**
-   **None**

</td></tr><tr><td class="sub-head" colspan="2">

Planning

</td></tr><tr><td>

Planned Start

</td><td>

Planned start date for the exercise event in the **YYYY-MM-DD HH:mm:ss** format.

</td></tr><tr><td>

Plan Approvers

</td><td>

Plan approvers for the exercise event.

</td></tr><tr><td>

Result Approvers

</td><td>

Result approvers for the exercise event.

</td></tr><tr><td class="sub-head" colspan="2">

Scope

</td></tr><tr><td>

Exercise Method

</td><td>

Method for the exercise. Available options are:-   **Simulation**
-   **Tabletop**
-   **Walkthrough**
-   **Functional**

Technically, all exercises are treated the same way. However, only Functional exercises automatically generate tasks, while Simulation, Tabletop, and Walkthrough exercises do not have any technical differences in their implementation.**Note:** For exercise events, the exercise method is **Functional** by default.

</td></tr><tr><td>

Participants

</td><td>

Participants for the exercise.

</td></tr><tr><td>

Goals

</td><td>

Goals for the exercise.

</td></tr><tr><td>

Objectives

</td><td>

Objectives for the exercise.

</td></tr><tr><td class="sub-head" colspan="2">

Assets tab \(Added after the event has been created\)

</td></tr><tr><td>

Asset types

</td><td>

Type of the asset and its info.

</td></tr><tr><td>

Short description

</td><td>

Short description of the asset type.

</td></tr><tr><td>

State

</td><td>

State of the asset type.

</td></tr><tr><td>

Actual time taken

</td><td>

Actual time taken for the asset type.

</td></tr><tr><td>

Finalized RTO

</td><td>

Finalized RTO for the asset type.

 The finalized recovery time objective is the suggested downtime until normal operations can be available to users. If there is no adjusted RTO, this is the recovery time objective. If there is an adjusted RTO, this is the adjusted RTO.

</td></tr><tr><td>

Total effort

</td><td>

Total effort for the asset type.

</td></tr><tr><td>

Primary source

</td><td>

Primary source of the asset type.

</td></tr><tr><td>

Status in source

</td><td>

Status in source for the asset type.

</td></tr><tr><td>

Target recovery time \(RTO\)

</td><td>

Target recovery time \(RTO\) for the event asset. This field is read-only and it is filled out from the BIA. You can select the **Update dependency** UI action to pull value from latest non-archived BIA. Target recovery time is the finalized RTO value.

</td></tr><tr><td>

Recovery tier

</td><td>

Recovery tier for the event asset. This field is read-only and it is filled out from the BIA.

</td></tr><tr><td>

Target recovery point \(RPO\)

</td><td>

Target recovery point \(RPO\) for the event asset. This field is read-only and it is filled out from the BIA. Target recovery point is the finalized RPO value.

</td></tr><tr><td class="sub-head" colspan="2">

Plans

</td></tr><tr><td>

Plans associated with the event

</td><td>

Details of the plans such as Number, Short description, State, Actual time taken, Total effort, Type, and Parent.

</td></tr><tr><td class="sub-head" colspan="2">

Action items

</td></tr><tr><td>

Action items associated with the event

</td><td>

Ad-hoc action items of task and assessment type, associated with the event and their details such as Number, Short description, State, Assigned to, and Due date.

</td></tr><tr><td class="sub-head" colspan="2">

Similar tasks groups

</td></tr><tr><td>

Group of similar tasks associated with the event

</td><td>

Group of similar tasks, their names, and original tasks associated w

</td></tr><tr><td class="sub-head" colspan="2">

Event tasks

</td></tr><tr><td>

Event tasks associated with the event

</td><td>

Information on the event tasks such as Number, Short description, State, Impacted assets, Assigned to, Dependencies, Actual start, Actual end, Related activated plan, Similar tasks group, Phase.

</td></tr></tbody>
</table>**Parent Topic:**[Create an exercise](../task/start-exercise-event-in-uib-ws.md)

