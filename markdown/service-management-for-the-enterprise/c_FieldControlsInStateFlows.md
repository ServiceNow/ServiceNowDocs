---
title: Field controls in state flows
description: You can define controls for individual fields that are enforced when a record transitions between states.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [State flow customization, Service management states, Service Management]
---

# Field controls in state flows

You can define controls for individual fields that are enforced when a record transitions between states.

Settings in the Field Controls section of the State Flow form enable you to apply field controls when the system detects a specified state transition or when the end state is the current state when the form is opened. The control is applied only to existing fields on the form. State flows cannot add fields to the form.

For example, you might want the **Problem** field to be visible when an incident moves to the **Awaiting Problem** state. If the incident state changes to **Awaiting User Info**, you hide the **Problem** field and make the **Caller** field mandatory.

Configure state flow records with an ending state only and create the correct behavior for every ending state you want to control. This ensures that the field controls are set properly when the user selects a new state, and also when the user returns a record's **State** field to the original state. Only specify a full state transition, with both a starting and ending state, when you want a particular behavior for that precise state transition.

**Note:** State flows use client scripts to enforce field controls. It is possible that your settings can be changed by existing UI policies, which execute after client scripts.

**Parent Topic:**[State flow customization](c_StateFlowCustomization.md)

**Related topics**  


[Request states](../../planning-and-policy/reference/r_SMRequestStates.md)

[Request task states](../../planning-and-policy/reference/r_SMRequestTaskStates.md)

