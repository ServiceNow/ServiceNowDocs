---
title: Advanced OT Change Model playbook
description: Learn about the Advanced Operational Technology \(OT\) Change Model playbook stages that an OT change with approvals must go through until it’s completed.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Select a change model to fulfill change requests, Configure, Operational Technology Change Management, Operational Technology]
---

# Advanced OT Change Model playbook

Learn about the Advanced Operational Technology \(OT\) Change Model playbook stages that an OT change with approvals must go through until it’s completed.

## Initiate

The Initiate stage of an OT Change request lets you capture the details of the requested change and assign the change as necessary. This stage has three tasks.

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
|Risk|Amount of risk the change poses.|
|Impact|Measure of the effect that a change has on your industrial processes.|

|Field|Description|
|-----|-----------|
|Requested by|User who requests the change.|
|Assignment group|Assigned group that works on the change. The assignment group can be any group with the type OT.|
|Assigned to|User who works on this change. If the assignment group changes, the **Assigned to** field is cleared.|

## Plan

The Plan stage of an OT change request lets you add a justification for the change, an implementation plan, a risk and impact plan, a backout plan, a test plan, and a time to schedule the change. This stage has six tasks.

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
</table>## Approve

The Approve stage of an OT Change request lets reviewers approve or deny the OT Change. This stage includes only one task.

|Field|Description|
|-----|-----------|
|Approve button|If you're a reviewer shown in the table on the task form, select **Approve** to accept the change.|
|Deny button|If you're a reviewer shown in the table on the task form, select **Deny** to reject the change.|
|Comments|Additional information about the approval or denial of the change.|

For more information about change approvals, see [Operational Technology change approval](../reference/ot-change-approval.md).

## Implement

The Implement stage of an OT change request provides the details of the following tasks. You can mark this stage as complete when it's finished.

-   **Stop the function**

    If needed, mark as complete after you stop the function of the targeted OT devices.

-   **Ensure LOTO**

    Lockout/Target \(LOTO\) is a safety procedure to prevent accidental or unintentional start-up of machinery during maintenance or service. Mark as complete when LOTO is completed.

-   **Perform the change**

    Mark as complete when the change is performed on the targeted OT devices and completed.


## Post-implementation Review

The Post-implementation Review stage of an OT change request lets you check off the performed tasks, create additional OT change tasks for remaining work identified during the review, and mark the revoke LOTO process as complete.

|Field|Description|
|-----|-----------|
|Perform electrical check|Check box that you select after the electrical check has been completed.|
|Perform network check|Check box that you select after the network check has been completed.|
|Perform quality check|Check box that you select after the quality check has been completed.|
|Perform safety check|Check box that you select after the safety check has been completed.|

|Field|Description|
|-----|-----------|
|OT Change Tasks|List of the change tasks that are related to the OT change.|
|State|State of the OT change. The state moves and tracks changes through several stages of resolution.|
|Assigned to|User who works on this change. If the assignment group changes, the **Assigned to** field is cleared.|
|Short description|Brief description of the change task.|

-   **Revoke LOTO**

    After the change is implemented and reviewed, mark as complete when the lockout-target is revoked.


## Spin-off Tasks

The Spin-off Tasks stage lists all the change tasks in the Post Implementation Review that must be completed.

## Close

The Close stage lets you close the change record after the change is completed.

|Field|Description|
|-----|-----------|
|Close code|Reason that the change record was closed.|
|Close notes|Additional details about closing the change record.|

**Parent Topic:**[Select a change model to fulfill change requests](../task/select-change-model.md)

