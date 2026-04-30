---
title: Configure boundary hierarchy
description: Establish parent-child relationships between authorization boundaries to improve boundary management, visibility, and organizational structure within Continuous Authorization and Monitoring. You can assign a parent boundary and associate multiple child boundaries to authorization boundary.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [View authorization boundary details, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Configure boundary hierarchy

Establish parent-child relationships between authorization boundaries to improve boundary management, visibility, and organizational structure within Continuous Authorization and Monitoring. You can assign a parent boundary and associate multiple child boundaries to authorization boundary.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_user, sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the lists icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

2.  From the Authorization boundaries under the Risk Management Framework \(RMF\) list, select an authorization boundary record.

3.  To add a parent boundary, select the **Parent boundary** from the **Details** list in the authorization boundary.

    ![Adding parent boundary.](../image/auth-bound-parent-boundary.png)

4.  To add a child boundary, select the **Child Boundaries** related list and perform the following steps:

    1.  Select **Add** to add child boundaries.

        ![Adding a child boundary.](../image/child_auth_boundary_add1.png)

    2.  Select one or more authorization boundaries and select **Add**.

        ![Adding Child Authorization Boundary.](../image/child_auth_boundary_add.png)

        You can add multiple child authorization boundaries.


## Result

You can view the child boundaries in the **Highlighted details** panel under the **Boundary hierarchy** section.

![Viewing child boundary hierarchy.](../image/child_auth_boundary_add2.png "Boundary hierarchy")

**Parent Topic:**[View authorization boundary details](auth-bound-overview-ws.md)

