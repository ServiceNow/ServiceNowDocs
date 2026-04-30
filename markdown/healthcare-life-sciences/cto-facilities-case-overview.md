---
title: Healthcare Facilities case overview
description: Use the Healthcare Facilities case \[sn\_cto\_facilities\_case\] to create case types for facilities support requests.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Healthcare Facilities case overview

Use the Healthcare Facilities case \[sn\_cto\_facilities\_case\] to create case types for facilities support requests.

![A healthcare Facilities case in CSM/FSM Configurable Workspace.](../image/cto-facilities-case-overview.png)

If the Field Service Management \[com.snc.work\_management\] plugin is installed, Healthcare Facilities cases automatically generate related work orders, which are assigned to supporting agents with the fulfiller role. If this plugin isn’t installed, support agents must fulfill the case itself.

By associating these cases with specific healthcare organizations, care team members can easily view all cases created for their team, unit, or organization.

Any updates, comments, or status changes made to the work order reflect in the case, and vice versa. When a work order is linked to a case, the fulfiller only manages the work order, and the case is then updated to reflect these changes.

## Work order auto-creation

![](../image/cto-facilities-work-order-creation.png)

Work orders are created automatically in synchronization with Healthcare Facilities cases. All information from the Healthcare Facilities case is carried over into the work order.

## Comment synchronization

![Comment synchronization in Healthcare EVS work orders.](../image/cto-facilities-comment.png)

Comments on the Healthcare Facilities case are viewable on the work order. Comments in the Compose panel of the work order are viewable on the Healthcare Facilities case.

## State synchronization

![State synchronization between EVS cases and work orders.](../image/cto-facilities-state-sync.png)

The state of both the work order and the healthcare case remains in synchronization throughout the entire fulfillment process. Use the Care Team Portal to track your case state in real time through viewing case details in the portal.

**Note:** In Care Team Operations for Facilities, case data only synchronizes with work orders and doesn’t synchronize with work order tasks. Only updates made to the work order affect the associated case data.

