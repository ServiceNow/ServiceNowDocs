---
title: Installed with State Model
description: Several types of components are installed with the State Model.State Model adds the following tables.State Model adds the following role.Add, modify, and delete state models for task tables.State Model adds the following script include.State Model adds the following client script.State Model adds the following business rules.
locale: en-US
release: zurich
product: State Management
classification: state-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [State Management, Configure core features, Administer]
---

# Installed with State Model

Several types of components are installed with the State Model.

## Tables installed with State Model

State Model adds the following tables.

<table id="table_xhy_hv4_2bb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State Model\[sys\_state\_model\]

</td><td>

Defines the name of the state model and which table the state model targets. Also defines the condition for applying the state model to records and any common condition for moving from any state to any other state.

</td></tr><tr><td>

State Transition\[sys\_state\_transition\]

</td><td>

Defines how each record in the target table transitions to \(the enter condition\) and/or from \(the exit condition\) each state predefined for that table.

</td></tr></tbody>
</table>## Roles installed with State Model

State Model adds the following role.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

|State Model Administrator|Description|Contains roles|
|-------------------------|-----------|--------------|
|\[state\_model\_admin\]|Allows users to add, modify, and delete state models for task tables.|None|

### State model Administrator \[state\_model\_admin\]

Add, modify, and delete state models for task tables.

#### Contains Roles

List of roles contained within the role.

None.

#### Groups

List of groups this role is assigned to by default.

None.

#### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Script includes installed with State Model

State Model adds the following script include.

|Script include|Description|
|--------------|-----------|
|TableChoiceUtils|Utility class to get the choice list of a table field.|

## Client scripts installed with State Model

State Model adds the following client script.

<table id="table_rgt_ys4_2bb"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Populate State Choices

</td><td>

State Transition\[sys\_state\_transition\]

</td><td>

Populates the **State** field choices in the targeted record.

</td></tr></tbody>
</table>## Business rules installed with State Model

State Model adds the following business rules.

<table><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set the display value for state

</td><td>

State Transition \[sys\_state\_transition\]

</td><td>

Sets the **State** field value based on the state model for the table.

</td></tr><tr><td>

Set the table to pick choices

</td><td>

State Transition\[sys\_state\_transition\]

</td><td>

Caches the **State** field value from the first table in the hierarchy for further rule processing.

</td></tr></tbody>
</table>