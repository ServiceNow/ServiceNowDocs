---
title: Installed with state flows
description: Several types of components are installed with state flows.Tables are added with state flows.Business rules are added with state flows.Script includes are added with state flows.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [State flows, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with state flows

Several types of components are installed with state flows.

**Parent Topic:**[State flows](../concept/c_StateFlows.md)

## Tables installed with state flows

Tables are added with state flows.

|Table|Description|
|-----|-----------|
|State Flow \[sf\_state\_flow\]|Contains state flow definitions. This table contains all state flow definitions, including those for work orders and work order tasks.|
|Work Order Flow \[sf\_work\_order\]|Contains state flow definitions for work orders. This table is installed when Field Service Management is activated.|
|Work Task Flow \[sf\_work\_task\]|Contains state flow definitions for work order tasks. This table is installed when Field Service Management is activated.|

## Business rules installed with state flows

Business rules are added with state flows.

<table id="table_BusinessRules"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assert Field Uniqueness in State Flow

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Ensures that business rules and UI actions are not accidentally copied to new state flows.

</td></tr><tr><td>

Check Client Script

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Adds a client script to new records.

</td></tr><tr><td>

Check Event Rule

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Adds or deletes event rules, as the event field is updated.

</td></tr><tr><td>

Check Work Notes Rule

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Adds or deletes work note rules, as the work notes for a state flow are updated.

</td></tr><tr><td>

Create Business Rule

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Automatically creates a business rule when automatic conditions or script are present.

</td></tr><tr><td>

Create script for Field controls

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Create scripts for field controls, when they are in use.

</td></tr><tr><td>

Create UI Action

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Automatically creates a UI action when manual conditions or script are filled in.

</td></tr><tr><td>

Delete Related Elements

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

When state flows are deleted, delete all related client scripts, business rules, UI actions and overrides.

</td></tr><tr><td>

Remove script for Field controls

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

If all field controls are disabled, see if any of the client scripts should be removed.

</td></tr><tr><td>

State Change

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

Get the correct state choice value when the state is changed.

</td></tr><tr><td>

Update dependent records

</td><td>

State Flow \[sf\_state\_flow\]

</td><td>

When a state flow is made active or inactive, ensure the business rule and UI actions are made active or inactive as well.

</td></tr></tbody>
</table>## Script includes installed with state flows

Script includes are added with state flows.

|Script include|Description|
|--------------|-----------|
|StateFlow|Implements state flows and supports creation of state flow elements, such as business rules, UI actions, dictionary overrides, and client scripts.|
|StateFlowAJAX|Allows access to state flow functionality from client scripts.|

