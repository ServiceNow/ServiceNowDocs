---
title: Implications of disabling SM state flows
description: State flows are used by SM applications to control how a work order or request automatically transitions from one state to the next. When state flows are disabled, various aspects of the ServiceNow system are also changed, as described here.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service management states, Service Management]
---

# Implications of disabling SM state flows

State flows are used by SM applications to control how a work order or request automatically transitions from one state to the next. When state flows are disabled, various aspects of the ServiceNow system are also changed, as described here.

Review the following implications before setting the **Enable state flows** configuration option to **Off**. After the configuration is saved, state flows cannot be re-enabled from the user interface.

When state flows are disabled, the state transition-related behavior of the following business rules, UI actions, and security rules are affected.

-   **Business rules on requests:**
    -   Group change validation
    -   Move tasks to pending assignment
    -   Request-driven dispatch
    -   Unassigned
    -   Verify work notes
-   **Business rules on tasks:**
    -   Apply dispatch method
    -   Populate schedule
    -   Populate schedule - new SOT \(service order task\)
    -   Transitions
    -   Unassigned
-   **The following business rules run partially:**
    -   The part of **Build scratchpad and display info messages** that shows an error message if a task is pending dispatch and auto-assignment fails is disabled.
    -   For the **Validate changes** business rule, the only part that runs is when the system checks for work notes and rolls them up.
-   **UI actions on requests:**
    -   When the **Spam** button on the request form is clicked, the state is not changed, but the work notes indicate that the request was closed as spam.
-   **UI actions on tasks:**
    -   Assign to me
    -   View task on map
    -   New
-   **Security rules:**
    -   State-based aspects of security rules no longer apply. For example, when state flows are enabled, the **Short description** field is not editable when a request or task is closed complete, incomplete, or canceled. When state flows are disabled, the **Short description** is always editable.
    -   Role-based aspects of security rules continue to apply when state flows are disabled.
-   **Additional changes when state flows are disabled:**
    -   The process flow formatter is removed from request and task forms.
    -   The **State** field can be edited on request and task forms.
    -   The following configuration fields are changed:
        -   **Process lifecycle** is set to **request-driven**.
        -   **Assignment method for requests** is set to **manual**.
        -   **Assignment method for tasks** is set to **manual**.
        -   **Approval for new request required** is disabled.
        -   **Qualification is required for new requests** is disabled.
        -   **Agent must accept or reject the assigned task** is disabled.
        -   **Use dispatch queue** is disabled.

-   **[Re-enable state flows](../task/t_ReEnableStateFlows.md)**  
When service management state flows have been disabled, they cannot be re-enabled from the user interface.

**Parent Topic:**[Service management states](../../it-services/concept/c_ServiceManagementStates.md)

