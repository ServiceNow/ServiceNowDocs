---
title: Healthcare Biomed case overview
description: Use the Healthcare Biomed case to create case types for biomed related healthcare operational requests.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Healthcare Biomed case overview

Use the Healthcare Biomed case to create case types for biomed related healthcare operational requests.

![A healthcare biomed case created for Care Team Operations for Biomed.](../image/hco_biomed_case.png)

If the Field Service Management \[com.snc.work\_management\] plugin is installed, Healthcare Biomed cases automatically generate related work orders which are assigned to supporting agents with the fulfiller role. If this plugin isn’t installed, support agents must fulfill the case itself.

By associating these cases with specific healthcare organizations, care team members can easily view all cases created for their team, unit, or organization.

Any updates, comments, or status changes made to the work order reflect in the case, and vice versa. When a work order is linked to a case, the fulfiller only manages the work order, and the case is then updated to reflect these changes.

## Work order auto-creation

![Work order auto creation from the Healthcare biomed case.](../image/cto-biomed-work-order-auuto.png)

Work orders are created automatically in synchronization with Healthcare Biomed cases. All information from the Healthcare biomed case is carried over into the work order.

## Comment synchronization

![Comment sync between Work orders and Healthcare biomed cases.](../image/cto-biomed-comment-sync.png)

Comments on the Healthcare Biomed case are viewable on the work order, and comments in the Compose panel of the work order are viewable on the Healthcare Biomed case.

## State synchronization

![State sync between work orders and healthcare biomed cases.](../image/cto-it-state-sync.png)

The state of both the work order and the healthcare case remains in synchronization throughout the entire fulfillment process. Use the Care Team Portal to track your case state in real time through viewing case details in the portal.

**Note:** In Care Team Operations for Biomed, case data only synchronizes with work orders and does not synchronize with work order tasks. Only updates made to the work order affects the associated case data.

