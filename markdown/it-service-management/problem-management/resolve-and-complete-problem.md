---
title: Resolve and complete a problem
description: Resolve the issue and add detailed note of the resolution for future reference.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Resolve and complete a problem

Resolve the issue and add detailed note of the resolution for future reference.

## Before you begin

-   Role required: admin, problem\_admin, problem\_coordinator, or problem\_manager
-   Activate the Problem Management Best Practice — Madrid — State Model \(com.snc.best\_practice.problem.madrid.state\_model\) to get the new best practice states and guided actions to navigate the lifecycle of a problem. For details, see [Activate Problem Management Best Practice — Madrid — State Model](act-pm-best-prac-madrid-state-mod.md).

## Procedure

1.  Click **Resolve**.

    ![fix in progress state](../image/pm-resolve.png)

    The problem enters the **Resolved** state with **Resolution code** as **Fix Applied**.

2.  Click **Complete**.

    ![resolved state](../image/pm-complete.png)

    The problem enters the **Closed** state with **Resolution code** as **Fix Applied**.

    **Note:**

    -   When a problem is closed or canceled, all related open problem tasks are canceled provided you select the problem management property **Cancel open Problem Tasks when closing a Problem** \(**problem.closed.cancel\_open\_tasks**\).
    -   When a problem is closed, you can still create problem tasks provided you select the problem management property **Can create a Problem Task on a Closed Problem?** \(**problem.closed.can\_create\_tasks**\).
    You can reanalyze the problem even after it is closed by clicking **Re-analyze**. The state of the problem changes from **Closed** to **Root Cause Analysis**. The following problem management properties controls who can reanalyze the problem:

    -   **Who can Re-analyze a Canceled Problem?** \(**problem.closed.role.reanalyze\_from\_canceled**\)
    -   **Who can Re-analyze a Risk Accepted \(Closed state\) Problem?** \(**problem.closed.role.reanalyze\_from\_closed\_riskaccepted**\)
    -   **Who can Re-analyze a Completed Problem?**\(**problem.closed.role.reanalyze\_from\_completed**\)
    When all the related tasks mentioned in the problem management property **List of related task records \(comma-separated\) to track as fixes for this Problem. Used to notify the Coordinator when the all of the related fix records are Completed or Canceled. E.g. incident.problem\_id, change\_request.parent** \(**problem.fix.records**\) are completed, a notification is sent to the problem coordinator regarding the same.

    **Note:** Changing this property to include new tables also requires you to create a corresponding Business Rule for the overall functionality to work seamlessly. For example, for the Change request, the Business Rule is **Check Related Problem Fixes - Change Req**.


**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

