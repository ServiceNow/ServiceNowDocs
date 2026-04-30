---
title: Basic OT Change Model playbook
description: Learn about the Basic Operational Technology \(OT\) Change Model playbook stages that an OT change without approvals must go through until it’s completed.
locale: en-US
release: xanadu
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Select a change model to fulfill change requests, Configure, Operational Technology Change Management, Operational Technology]
---

# Basic OT Change Model playbook

Learn about the Basic Operational Technology \(OT\) Change Model playbook stages that an OT change without approvals must go through until it’s completed.

## Initiate

The Initiate stage of an OT change request lets you capture the details of the requested change and assign the change as necessary. This stage has three tasks.

|Field|Description|
|-----|-----------|
|Short description|Brief description of the change.|
|Description|Details of the change.|
|Category|Type of change.|
|Site|Site where the change takes place.|
|Watch list|Users who receive notifications about this change when comments are added.|
|Work notes list|Users who receive notifications about this change when work notes are added.|

|Field|Description|
|-----|-----------|
|Priority|Impact and urgency to identify how quickly the change should be addressed.|
|Risk|Amount of risk that the change poses.|
|Impact|Measure of the effect that a change has on your industrial processes.|

|Field|Description|
|-----|-----------|
|Requested by|User who requests the change.|
|Assignment group|Assigned group that works on the change. The assignment group can be any group with the type OT.|
|Assigned to|User who works on this change. If the assignment group changes, the **Assigned to** field is cleared.|

## Plan

The Plan stage of an OT Change request lets you add a justification for the change, an implementation plan, a risk and impact plan, a backout plan, a test plan, and a time to schedule the change. This stage has six tasks.

|Field|Description|
|-----|-----------|
|Justification|Reason why the change must take place.|

|Field|Description|
|-----|-----------|
|Implementation plan|Details of how to implement the requested change.|

|Field|Description|
|-----|-----------|
|Risk and impact analysis|Details of any risk and impact factors that are related to this change.|

|Field|Description|
|-----|-----------|
|Backout plan|Details of how to reverse the change in place if necessary.|

|Field|Description|
|-----|-----------|
|Test plan|Details of how to test the implemented change.|

<table id="table_edj_nxm_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned start date

</td><td>

Date that the change takes place.**Note:** You can also choose an available downtime slot on the calendar by selecting the **Scheduling Assistant** button to fill in the planned start date field automatically.

</td></tr><tr><td>

Planned end date

</td><td>

Date that the change ends.**Note:** You can also choose an available downtime slot on the calendar by selecting the **Scheduling Assistant** button to fill in the planned end date field automatically.

</td></tr></tbody>
</table>## Implement

The Implement stage of an OT change request provides the details of the following task. You can mark this stage as complete when it's finished.

-   **Perform the change**

    Mark as complete when the change is performed on the targeted OT devices and completed.


## Close

The Close stage lets you close the change record after the change is completed.

|Field|Description|
|-----|-----------|
|Close code|Reason that the change record was closed.|
|Close notes|Additional details about closing the change record.|

**Parent Topic:**[Select a change model to fulfill change requests](../task/select-change-model.md)

