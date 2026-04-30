---
title: Remove or release members and equipment from your crew
description: Remove or release crew members and equipment from your crews on the ServiceNow Agent application.Remove members or equipment from your planned crew so they can be assigned to other crews or tasks.Remove members or equipment from a task crew so they can be assigned to other crews or tasks.Release task crew members from work order tasks that are in the Work in Progress state.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Crew, ServiceNow Agent mobile app, Use, Field Service Management]
---

# Remove or release members and equipment from your crew

Remove or release crew members and equipment from your crews on the ServiceNow Agent application.

## Remove members or equipment from your planned crew

Remove members or equipment from your planned crew so they can be assigned to other crews or tasks.

### Before you begin

To remove equipment, administrators must activate the Field Service Resource Scheduling plugin \(com.snc.resource\_scheduling\). For more information, see [Activate Resource Scheduling](../task/activate-equipment-scheduling.md).

Role required: wm\_agent and crew\_moderator

### Procedure

1.  Navigate to **My work** &gt; **My crews**.

2.  Select the crew or equipment that you want to remove.

3.  Tap the **Remove** icon \(![Remove icon.](../image/trash-mobile-icon.png)\).

4.  Tap **Remove**.


## Remove members or equipment from a task crew

Remove members or equipment from a task crew so they can be assigned to other crews or tasks.

### Before you begin

To remove equipment, administrators must activate the Field Service Resource Scheduling plugin \(com.snc.resource\_scheduling\). For more information, see [Activate Resource Scheduling](../task/activate-equipment-scheduling.md).

Role required: wm\_agent and crew\_moderator

### Procedure

1.  Navigate to **My work** &gt; **My Tasks**.

2.  Select the work order task where the task crew member or equipment is assigned.

3.  Find the member or equipment that you want to remove, and tap the **Remove** icon \(![Remove icon.](../image/trash-mobile-icon.png)\).

    **Note:** If the task is in the Work in Progress state, **Remove** is replaced with **Release**.

4.  Tap **Remove**.


## Release a task crew member

Release task crew members from work order tasks that are in the Work in Progress state.

### Before you begin

**Release** only shows if the work order task is in the Work in Progress state. If not, task crew members must be removed. For more information, see [Remove members or equipment from a task crew](remove-members-eq-crew.md#).

-   
Role required: wm\_agent and crew\_moderator

### Procedure

1.  Navigate to **My work** &gt; **My tasks**.

2.  Select the work order task where the task crew member is assigned.

3.  Find the task crew member that you want to release, and tap the **Edit** icon \(![Edit icon.](../image/edit-mobile-icon.png)\).

4.  Tap **Release**.

    A confirmation message appears. To proceed with the action, tap **Release**. To cancel, tap **Cancel**.


