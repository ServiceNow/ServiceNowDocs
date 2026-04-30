---
title: Offboard agents on the Field Service Contractor Portal
description: Offboard agents of the contractor company to terminate their services.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contractor Portal, Completing work orders on the web interface, Use, Field Service Management]
---

# Offboard agents on the Field Service Contractor Portal

Offboard agents of the contractor company to terminate their services.

## Before you begin

Before offboarding an agent, ensure that agents do not have items pending with the following status:

-   Tasks in the **Work In Progress** state.
-   Transfer orders in the **In Transit** state
-   Parts in the **In Stock** state or **Pending Transfer** sub state in their personal stockroom.

Role required: wm\_ext\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **Agents**.

2.  From the **Service Organization External Staffs** list, select the agent that you want to offboard.

3.  Click **Offboard Agent**.


## Result

The agent is offboarded successfully.

After receiving the offboarding request:

-   Assigned and accepted tasks from the agent's work list are reassigned to the manager who initiated the offboarding request.
-   The offboarding agent cannot be assigned new tasks
-   New transfer orders cannot be created in the agent's personal stockroom
-   The agent cannot log in to the Field Service Contractor Portal.
-   Email or SMS notifications are no longer sent to the agent.
-   The agent is automatically removed from the additional manager role and responsibilities.

