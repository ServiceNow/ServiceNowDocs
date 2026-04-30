---
title: Service management states
description: From creation until closure, SM application requests for work \(for example, work orders and facilities requests\), and their respective tasks follow a life cycle tracked by the State field in Field Service Management and Facilities Service Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Management]
---

# Service management states

From creation until closure, SM application requests for work \(for example, work orders and facilities requests\), and their respective tasks follow a life cycle tracked by the **State** field in Field Service Management and Facilities Service Management.

The life cycle is controlled through business rules and UI actions that are updated by the system automatically.

**Note:** The **State** field on the record is always read-only.

-   **[State flow customization](c_StateFlowCustomization.md)**  
State flows control the sequence in which records transition between states in Service Management applications.
-   **[State flow example](../task/t_StateFlowExample.md)**  
Your business processes might require work order tasks to be accepted automatically when dispatched to an agent.
-   **[Implications of disabling SM state flows](../../planning-and-policy/concept/c_ImpDsblStFl.md)**  
State flows are used by SM applications to control how a work order or request automatically transitions from one state to the next. When state flows are disabled, various aspects of the ServiceNow system are also changed, as described here.

**Parent Topic:**[Service Management](c_ServiceManagement.md)

**Related topics**  


[bundle-fsm.t_CustomizeAStateFlow]

