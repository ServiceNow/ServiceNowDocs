---
title: State flows
description: State flows enable an administrator to customize transitions from one state to another in tables derived from the Task \[task\] table and configure the system to perform work during transitions to specific states.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# State flows

State flows enable an administrator to customize transitions from one state to another in tables derived from the Task \[task\] table and configure the system to perform work during transitions to specific states.

An example of a state transition is when the **State** field in an incident changes from **Active** to **Awaiting User Info**. An administrator might want to trigger an event during this transition or make a specific field mandatory when the incident reaches the end state.

State transitions in the Field Service Management application were reimplemented to use state flows. For information about customizing Field Service Management state flows, see State flow customization.

-   **[Installed with state flows](../reference/r_InstalledWithStateFlows.md#)**  
Several types of components are installed with state flows.
-   **[Use state flows](c_UseStateFlows.md)**  
You can create custom state flows for any table that uses states.
-   **[Domain separation and State Flows](domain-separation-state-flows.md)**  
Domain separation is unsupported in State Flows. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Exploring Service Administration](../../service-administration/concept/c_ServiceAdministration.md)

