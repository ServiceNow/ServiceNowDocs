---
title: Network inventory change request form
description: The Change Request form enables you to create and modify the change activities for the Telecom Inventory change models in the Design and Assign function.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Network inventory change request form

The Change Request form enables you to create and modify the change activities for the Telecom Inventory change models in the Design and Assign function.

<table id="table_tni_change_request_field"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Change request number.

</td></tr><tr><td>

Requested by

</td><td>

User who has requested the change. This field is available in the Change Requests list view so that you can see who requested a particular change.

</td></tr><tr><td>

Service

</td><td>

Business service that you want to make available for the change request.

</td></tr><tr><td>

Service offering

</td><td>

Service option that consists of one or more service commitments that uniquely define the level of service. You can select different levels of performance and features for a service through service offerings. You must select a service to filter the available service offerings.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the change applies to.

</td></tr><tr><td>

Risk

</td><td>

Risk level for the change.Select one of the following options:

-   **High**
-   **Moderate**
-   **Low**

</td></tr><tr><td>

Impact

</td><td>

Measure of the effect of a change on business processes.

</td></tr><tr><td>

Short description

</td><td>

Summary of the change.

</td></tr><tr><td>

Description

</td><td>

Description of the change in detail.

</td></tr><tr><td>

Model

</td><td>

Change model that is associated with the Telecom Network Inventory change request. After selecting the change model tile, the associated model appears in this field. You can also manually select one of the following options:

 -   **Add Interface Card**

Change model that is used to add an interface card in an equipment slot.

-   **Create Inventory Equipment**

Change model that is used to add equipment when using an inventory template in a site or equipment holder.

-   **Create Logical Connection**

Change model that is used to create a logical connection between two network interfaces.

-   **Create Physical Connection**

Change model that is used to create a physical connection between two network interfaces.

-   **Emergency**

Change model that is used for the Telecom Network Inventory emergency changes.

-   **GPON Broadband Service**

Change model that is used to fulfill a GPON broadband order request.

-   **Normal**

Change model that is used for the Telecom Network Inventory normal changes.


 **Note:** These change models are available in the **Change** &gt; **Create New** &gt; **Create a change request** window.

</td></tr><tr><td>

Assignment group

</td><td>

Group working on the change request.

</td></tr><tr><td>

Assigned to

</td><td>

User that the change is assigned to. If an assignment rule applies, the change is automatically assigned to the appropriate user or group.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Planned start date|Projected start date for the implementation. The planned start date can be the current date or a future date. The default value for this field is the current date. To change the planned start date, click the calendar icon and select a new date.|
|Planned end date|Projected end date for the implementation. The planned end date must be after the planned start date. The default value for this field is one day after the planned start date. To change the planned end date, click the calendar icon and select a new date.|
|CAB required|Option that designates if this change request requires a Change Advisory Board \(CAB\) approval before implementation.|
|CAB date|CAB approval date for the implementation.|
|Actual start date|Actual start date for the implementation. The actual start date can be on or before the planned start date.|
|Actual end date|Actual end date for the implementation. The actual end date can be before the planned start date but not before the actual start date.|
|CAB delegate|User who attends the Change Advisory Board \(CAB\) meeting to describe the change.|
|CAB recommendation|Notes or recommendations that are related to the CAB meeting.|

|Field|Description|
|-----|-----------|
|Watch list|User who gets the notifications about the change request. Add the names of the users who receive notifications and can view the watch topic.|
|Additional comments \(Customer visible\)|Option that designates if the work notes need to be shared with the user who requested the change.|
|Work notes|Work notes for the change request.|
|Work notes list|Users who can get the notification about the work notes.|

<table id="table_tni_change_request_closure"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Close code

</td><td>

Close code that best describes the reason you are closing this change request. Select one of the following options:-   **Successful**
-   **Unsuccessful with issues**
-   **Unsuccessful**

</td></tr><tr><td>

Close notes

</td><td>

Any additional notes that describe the outcome of closing this change request.

</td></tr></tbody>
</table><table id="table_tni_change_task"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Change task identification number.

</td></tr><tr><td>

Change request

</td><td>

Change request number under which this change task was created.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) to which the change is applied.

</td></tr><tr><td>

Request type

</td><td>

Type of change request, based on the network inventory models.

</td></tr><tr><td>

Short description

</td><td>

Short description for this order task.

</td></tr><tr><td>

Description

</td><td>

Description of this order task.

</td></tr><tr><td>

State

</td><td>

State of this change task. Select one of the following options:-   **Pending**

Task is waiting for an action from the user.

-   **Open**

No action is taken on this task yet.

-   **In Progress**

Task processing is in progress.

-   **Closed**

Change task is complete.

-   **Canceled**

Change task has been canceled.


</td></tr><tr><td>

Assignment group

</td><td>

Name of the group name that is responsible for this task. Click the search icon \(![Search icon.](../image/search.png)\) to select a group from the list.

</td></tr><tr><td>

Assigned to

</td><td>

Depending on the selected group, the users who are assigned to the list are shown. Click the search icon \(![Search icon.](../image/search.png)\) to see the list of users.

</td></tr><tr><td>

Work notes

</td><td>

Free-form work order note text.

</td></tr><tr><td>

Update

</td><td>

Option to save changes that you made to the order task.

</td></tr><tr><td>

Close Task

</td><td>

Option to change the state of the order task to **Closed**.

</td></tr><tr><td>

Delete

</td><td>

Option to delete this order task.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

