---
title: Field controls in state flows
description: You can define controls for individual fields that are enforced when a record transitions between states.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define state flows, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Field controls in state flows

You can define controls for individual fields that are enforced when a record transitions between states.

The Field Controls section of the State Flow form enables you to determine what happens if the system detects a specified state transition. Field controls also allow you to define what happens if the end state is the same state the form is opened in. The control is applied only to existing fields on the form. State flows can’t add fields to the form.

For example, you might want the **Problem** field to be visible when an incident moves to the **Awaiting Problem** state. If the incident state changes to **Awaiting User Info**, you hide the **Problem** field and make the **Caller** field required.

Configure state flow records with an ending state only and create the correct behavior for every ending state you want to control. This verifies that the field controls are set properly when the user selects a new state, and also when the user returns a record's **State** field to the original state. Only specify a full state transition, with both a starting and ending state, when you want a particular behavior for that precise state transition.

**Note:** State flows use client scripts to enforce field controls. It's possible that your settings can be changed by existing UI policies, which execute after client scripts.

