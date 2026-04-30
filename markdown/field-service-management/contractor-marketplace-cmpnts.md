---
title: Field Service Marketplace components
description: Several types of components are installed with the activation of the Field Service Marketplace feature including tables, roles, system properties, business rules, and script includes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Marketplace components

Several types of components are installed with the activation of the Field Service Marketplace feature including tables, roles, system properties, business rules, and script includes.

## Tables

Field Service Marketplace adds the following tables:

<table id="table_vrp_5lq_21c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Marketplace engagement method\[marketplace\_engagement\_method\]

</td><td>

This table has the basic rules for engaging with contractors. The engagement methods define the ways contractors can respond to the marketplace requests.

</td></tr><tr><td>

Marketplace request\[marketplace\_request\]

</td><td>

This table establishes the relationship between engagement method and work order tasks. This table is populated by the dispatcher with all relevant fields to progress the request.

</td></tr><tr><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

This table maintains distinct records for each contractor, offering the dispatcher the capability to choose contractors permitted to participate in a marketplace request.

</td></tr><tr><td>

Marketplace response\[marketplace\_response\]

</td><td>

This table is designated to gather responses from all contractors regarding their pricing, as well as the intended start and completion dates for the task.

</td></tr><tr><td>

Eligible engagement method\[eligible\_engagement\_method\]

</td><td>

This table defines the list of eligible engagements for a marketplace task filter.

</td></tr></tbody>
</table>## Roles

Field Service Marketplace adds the following roles:

|Role|Description|
|----|-----------|
|sn\_mktplace\_core.mktplace\_admin|Administrator role can create marketplace engagement methods.|
|sn\_mktplace\_core.mktplace\_requestor|Requestor role can push tasks to the marketplace.|
|sn\_mktplace\_core.mktplace\_fulfiller|Fulfiller role can respond to marketplace requests.|

## System properties

Field Service Marketplace adds the following system properties:

The following table lists the system properties that are required to set up Field Service Marketplace. Navigate to **All**System Properties list

<table id="table_xr5_hwt_g1c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_mktplace.maximum\_number\_of\_contractors

</td><td>

Maximum number of contractors to fetch and show for a Marketplace request. -   **Type**: Integer
-   **Default value**: 10

</td></tr><tr><td>

sn\_fsm\_mktplace.use\_playbook\_experience\_for\_marketplace

</td><td>

Property to use playbook experience for marketplace.-   **Type**: true/false
-   **Default value**: true

</td></tr><tr><td>

sn\_fsm\_mktplace.wot\_fields\_to\_restrict\_update

</td><td>

Comma separated fields to restrict update when Work Order Task is pushed to marketplace. 1.  **Type**: String
2.  **Default values**: location,asset,work\_type,estimated\_work\_duration,estimated\_travel\_duration,estimated\_end,expected\_start,expected\_travel\_start,window\_start,window\_end,schedule\_lock

</td></tr></tbody>
</table>## Task Filters

Field Service Marketplace adds the following task filters:

<table id="table_fll_gv4_zbc"><thead><tr><th>

Task Filter

</th><th>

Conditions

</th><th>

Criterion

</th><th>

Function

</th></tr></thead><tbody><tr><td>

Marketplace tasksEnsure that the Field Service Marketplace plugin is active. For more information, see [Activate Field Service Marketplace](../task/activate-contractor-marketplace.md).

Demo data is provided with this plugin.

</td><td>

-   State is pending dispatch
-   Location is populated

</td><td>

Matching skills of contractorsDistance between task and contractors

</td><td>

Eligible for marketplace assignment.

</td></tr></tbody>
</table>## Business rules

Field Service Marketplace adds the following business rules:

<table id="table_tqb_24q_21c"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Restrict order change marketplace task

</td><td>

Work Order\[wm\_order\]

</td><td>

Blocks suspension of a work order when one of its tasks is pushed to the marketplace.

</td></tr><tr><td>

Restrict fields for marketplace task

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Blocks updates to certain work order task fields.

</td></tr><tr><td>

Cancel mp request on task cancellation

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Cancels any open marketplace request when the work order task is cancelled.

</td></tr><tr><td>

Restrict marketplace task with assigned

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Blocks a work order task with an assignment group populated and marketplace task set to true.

</td></tr><tr><td>

Restrict updates to marketplace flag

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Disables changing marketplace task flag of the work order task to false.

</td></tr><tr><td>

Disable changes when open request exists

</td><td>

Marketplace engagement method\[marketplace\_engagement\_method\]

</td><td>

Disallows changes to the engagement method when an open marketplace is using it.

</td></tr><tr><td>

Disable cost/time update from list

</td><td>

Marketplace engagement method\[marketplace\_engagement\_method\]

</td><td>

Validates edits of time and cost fields on the marketplace engagement method table list view.

</td></tr><tr><td>

Cancel all assignments and responses

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Cancels marketplace assignments and inactivate marketplace responses when a marketplace request is canceled.

</td></tr><tr><td>

Validate request insertion

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Blocks the creation of a new marketplace request when an open request exists.

</td></tr><tr><td>

Set assignments to timeout on close

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Updates the state of marketplace assignment records when a marketplace request is closed.

</td></tr><tr><td>

Create MP Assignment records in draft

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Creates marketplace assignments in the draft state when a marketplace request is created.

</td></tr><tr><td>

Check end time is more than start

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Validates start and end times of the marketplace request.

</td></tr><tr><td>

Cancel old flow on request end update

</td><td>

Marketplace request\[marketplace\_request\]

</td><td>

Cancels the old flow responsible for tracking the request end time, when the end time is updated.

</td></tr><tr><td>

Validate assignment insertion

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

Blocks the creation of a new assignment record for a request that isn’t open. Blocks duplicate assignment records for an open request.

</td></tr><tr><td>

Inactivate responses when withdrawn

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

If withdrawn, inactivates response of contractor.

</td></tr><tr><td>

Check close condition

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

Handles closing marketplace request and flow data records based on its close condition.

</td></tr><tr><td>

Unaward assignments when task is awarded

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

When a task is awarded to a contractor, other contractors' assignment records are marked unawarded.

</td></tr><tr><td>

Query on Assignment for Task

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

Query business rule on marketplace assignment table

</td></tr><tr><td>

Assigned from marketplace

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

When a task is awarded to a contractor, closes the request and updates the work order task with the necessary details. Updates the work order task scheduling method to marketplace.

</td></tr><tr><td>

Override wait duration on rejection

</td><td>

Marketplace assignment\[marketplace\_assignment\]

</td><td>

For a progressive push request, this BR will override the set wait duration when the current fulfiller receiving the bid, rejects the request

</td></tr><tr><td>

Disable negative in response duration

</td><td>

Marketplace response\[marketplace\_response\]

</td><td>

Disables insertion of responses with negative duration and checks response's start and end with work order task window start and end.

</td></tr><tr><td>

Update Assignment to accept

</td><td>

Marketplace response\[marketplace\_response\]

</td><td>

When a response is received, update the assignment record state of that contractor to accepted.

</td></tr><tr><td>

Validate response insertion

</td><td>

Marketplace response\[marketplace\_response\]

</td><td>

Blocks insertion of response if the work order task's "Is Fixed Window" flag is true and the response's start and end don’t fall within the work order task window. Blocks creation of responses for requests that aren’t open. Inactivates the previous response when a new response is received from the contractor.

</td></tr><tr><td>

Query on Response for Task

</td><td>

Marketplace response\[marketplace\_response\]

</td><td>

Query business rule on marketplace response table.

</td></tr><tr><td>

Evaluate response

</td><td>

Marketplace response\[marketplace\_response\]

</td><td>

This BR will help in evaluating the response received for a request, provided the selected engagement method has a response evaluation flow.

</td></tr><tr><td>

Set group resource type for contractors

</td><td>

Task Filter\[dynamic\_schedule\_task\_filter\]

</td><td>

This BR will set the resource type to sys\_user\_group for contractor or marketplace task filters.

</td></tr><tr><td>

Validate eligible engagement changes

</td><td>

Eligible engagement method\[eligible\_engagement\_method\]

</td><td>

This BR will validate any insertion or updates made to the eligible engagement method table.

</td></tr></tbody>
</table>## Script includes

Field Service Marketplace adds the following script includes:

|Script include|Description|
|--------------|-----------|
|MarketplaceCoreUtil|Contains util methods used for generic Marketplace core workflows.|
|FSMMarketplaceUtil|Contains util methods used for FSM specific workflows of Marketplace.|
|FSMMarketplacePlaybookUtil|Contains util methods used for Playbook workflow of Marketplace.|
|FieldServiceMarketplaceConstants|Holds constants.|
|MarketplaceCoreAjaxHelper|Contains util methods used in Marketplace Core client-side scripts.|
|FSMMarketplaceAjaxHelper|Contains util methods used in FSM Marketplace client-side scripts.|
|FSMMarketplaceCspUtil|Util file that holds methods used in Playbook's CSP.|
|FieldServiceMarketplaceDaoBase|The base dao for field service marketplace entities. All the entities can extend this class to re-use the common functionalities|
|FieldServiceMarketplaceEligibleEngagementsDao|Contains all the queries and insertion made on eligible\_engagement\_method table|
|MarketplaceTaskProcessorWOTImpl|Work order task implementation for MarketplaceTaskProcessorExtPoint|
|MarketplaceTaskProcessorBase|This class contains default implementation for MarketplaceTaskProcessor. It extends MarketplaceTaskProcessorPicker to choose the correct implementation of the MarketplaceTaskProcessorExtPoint.|
|MarketplaceTaskAssignment|This class will contain custom implementations for MarketplaceTaskAssignment. This will be the class that will be used for making any method invocations|
|MarketplaceTaskAssignmentBase|This class contains default implementation for MarketplaceTaskAssignment. It extends MarketplaceTaskAssignmentPicker to choose the correct implementation of the MarketplaceTaskAssignmentExtPoint.|
|FieldServiceMarketplaceEngagementDao|Contains all the queries and insertion made on marketplace\_engagement\_method table|
|FieldServiceWorkManagementDao|Contains all the Work Management related queries|
|MarketplaceEntityValidator|This class will contain custom implementations for MarketplaceEntityValidator. This will be the class that will be used for making any method invocations|
|MarketplaceEntityValidatorBase|This class contains default implementation for MarketplaceEntityValidator. It extends MarketplaceEntityValidatorPicker to choose the correct implementation of the MarketplaceEntityValidatorExtPoint.|
|MarketplaceTaskProcessor|This class will contain custom implementations for MarketplaceTaskProcessor. This will be the class that will be used for making any method invocations|
|FieldServiceMarketplaceResponseDao|Contains all the queries and insertion made on marketplace\_response table|
|MarketplaceDynamicSchedulingUtil|This is a util containing methods to be shipped when dynamic scheduling is installed along with marketplace|
|MarketplaceEntityValidatorAssignmentImpl|Marketplace Assignment Implementation for MarketplaceEntityValidatorExtPoint|
|FieldServiceMarketplacePlaybookDao|Contains all the queries and insertion made on all playbook related tables|
|MarketplaceTaskAssignmentWOTImpl|Work order task implementation for MarketplaceTaskAssignmentExtPoint|
|FieldServiceMarketplaceRequestDao|Contains all the queries and insertion made on marketplace\_request table|
|MarketplaceEntityValidatorRequestImpl|Marketplace Request Implementation for MarketplaceEntityValidatorExtPoint|
|MarketplaceEntityValidatorResponseImpl|Marketplace Response Implementation for MarketplaceEntityValidatorExtPoint|
|FieldServiceMarketplaceAssignmentDao|Contains all the queries and insertion made on marketplace\_assignment table|
|FSMMarketplaceGlobalUtil|Script Includes containing utils to be run at a global scope for marketplace module|
|MarketplaceTaskAssignmentPicker|Script include to choose the implementation of the MarketplaceTaskAssignmentExtPoint|
|MarketplaceCoreExtPointUtil|Utililty used by the marketplace module to retrieve extension points|
|MarketplaceTaskProcessorPicker|Script include to choose the implementation of the MarketplaceTaskProcessorExtPoint|
|MarketplaceCoreConstants|Script Include to hold the constants for marketplace core plugin|
|MarketplaceEntityValidatorPicker|Script include to choose the implementation of the MarketplaceEntityValidatorExtPoint|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

