---
title: Business rules installed with Facilities Move Management
description: A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installed with Facilities Move Management, Activate Facilities Move Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Business rules installed with Facilities Move Management

A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.

Facilities Move Management adds the following business rules.

<table id="table_ngl_zwx_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Force Workflow Update

</td><td>

Enterprise Move Request Task\[enterprise\_move\_request\_task\]

</td><td>

Forces workflow to trigger on close

</td></tr><tr><td>

Move to/from Facility Spaces only

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Only allows facility space \(fm\_space\) as to or from location

</td></tr><tr><td>

Pending Assignment - Update Task State

</td><td>

Move Task\[move\_task\]

</td><td>

Sets state to pending assignment

</td></tr><tr><td>

Set request to WIP

</td><td>

Enterprise Move Request Task\[enterprise\_move\_request\_task\]

</td><td>

Set request to work in progress when a task is started

</td></tr><tr><td>

Keep request scenario reference in synch

</td><td>

Enterprise Move Scenario\[enterprise\_move\_scenario\]

</td><td>

Update scenario on enterprise move request

</td></tr><tr><td>

Move Catalog out of draft

</td><td>

Move Request\[move\_request\]

</td><td>

If the request was created through the facilities catalog, set the state to **Ready**

</td></tr><tr><td>

Move users and assets

</td><td>

Enterprise Move Request Task\[enterprise\_move\_request\_task\]

</td><td>

Update user and asset location

</td></tr><tr><td>

Set Requested by user

</td><td>

Move Request\[move\_request\]

</td><td>

Set caller and requested by user

</td></tr><tr><td>

Enforce Building when floor is populated

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Prevent the selection of a building that does not contain a floor

</td></tr><tr><td>

Set Building when floor is populated

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Set the building when one of its floors are selected

</td></tr><tr><td>

Do not remove scenario from move request

</td><td>

Enterprise Move Request\[enterprise\_move\_request\]

</td><td>

Maintain the scenario with the move request

</td></tr><tr><td>

Trigger workflow on update

</td><td>

Move Task\[move\_task\]

</td><td>

Force workflow to start

</td></tr><tr><td>

Prevent non-space to\_location

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Ensure the **to location** is a facilities space \(fm\_space\)

</td></tr><tr><td>

Prevent Duplicates

</td><td>

Enterprise Move Detail\[move\_detail\]

</td><td>

Do not allow the same move detail record to be added more than once

</td></tr><tr><td>

Set Move Request

</td><td>

Enterprise Move Request Task\[enterprise\_move\_request\_task\]

</td><td>

Set the parent request

</td></tr><tr><td>

Check for open tasks

</td><td>

Enterprise Move Request\[enterprise\_move\_request\]

</td><td>

Prevent a request from being closed when tasks are still open

</td></tr><tr><td>

Autopopulate Move Delegator

</td><td>

Enterprise Move Delegator\[move\_delegator\]

</td><td>

Set the delegator

</td></tr><tr><td>

Add messaging

</td><td>

Enterprise Move Request\[enterprise\_move\_request\]

</td><td>

Add help messaging on the move request

</td></tr><tr><td>

Uncheck task options

</td><td>

Enterprise Move Request\[enterprise\_move\_request\]

</td><td>

 

</td></tr><tr><td>

Set Assigned

</td><td>

Enterprise Move Request Task\[enterprise\_move\_request\_task\]

</td><td>

Set the state to Assigned when Assigned to is not empty and State is Pending Assignment

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Move Management](r_InstallWFacMoveMgmt.md)

