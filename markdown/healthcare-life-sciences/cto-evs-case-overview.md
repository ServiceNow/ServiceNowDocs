---
title: Healthcare EVS case overview
description: Use the Healthcare EVS case \[sn\_cto\_evs\_case\] to create case types for environmental service support requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Healthcare EVS case overview

Use the Healthcare EVS case \[sn\_cto\_evs\_case\] to create case types for environmental service support requests.

## Healthcare Environmental Services case overview

![EVS case to work order flow.](../image/cto-evs-case.png)

If the Field Service Management \[com.snc.work\_management\] plugin is installed, Healthcare EVS cases automatically generate related work orders that are assigned to supporting agents with the fulfiller role. If this plugin isn’t installed, support agents must fulfill the case itself.

By associating these cases with specific healthcare organizations, care team members can easily view all cases created for their team, unit, or organization.

Any updates, comments, or status changes made to the work order reflects in the case, and vice versa. When a work order is linked to a case, the fulfiller only manages the work order, and the case is then updated to reflect these changes.

## Work order auto-creation

![Work order auto-creation from EVS cases.](../image/cto-work-order-creation.png)

Work orders are created automatically in synchronization with Healthcare EVS cases. All information from the Healthcare EVS case is carried over into the incident.

## Comment synchronization

![EVS case comment synchronization.](../image/cto-evs-comment-sync.png)

Comments on the Healthcare EVS case are viewable on the work order, and comments in the Compose panel of the work order are viewable on the Healthcare EVS case.

## State synchronization

![EVS case state synchronization.](../image/cto-evs-state-sync.png)

The state of both the work order and the healthcare case remains in synchronization throughout the entire fulfillment process. Use the Care Team Portal to track your case state in real time through viewing case details in the portal.

**Note:** In Care Team Operations for Environmental Services, case data only synchronizes with work orders and doesn’t synchronize with work order tasks. Only updates made to the work order affect the associated case data.

