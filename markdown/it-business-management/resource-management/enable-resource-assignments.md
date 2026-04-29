---
title: Enable attribute-based resource assignments
description: Enable the property to work on attribute-based resource assignments to request efforts for your planning items.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migration of resource plans and cost plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Enable attribute-based resource assignments

Enable the property to work on attribute-based resource assignments to request efforts for your planning items.

## Before you begin

-   If a project, demand, or a task has at least one attribute-based resource plan, Resource plans related list is hidden.
-   If a project, demand, or a task has at least one resource plan without any attribute-based resource assignments, Resource plans related list is visible.
-   If a project, demand, or a task has no resource plans and the **sn\_pw.enable\_resource\_planning** property is enabled, Resource assignments related list is available, else, Resource plans related list will be available.
-   If a project, demand, or a task has at least one attribute-based resource assignment, **New** and **Manage** options are hidden for Resource plans.
-   If a project, demand, or a task has at least one resource plan without any attribute-based resource assignments, **New** and **Manage** options are available for Resource plans.
-   If a project, demand, or a task has no resource plans and the **sn\_pw.enable\_resource\_planning** property is enabled, **New** and **Manage** options are hidden for Resource plans, else, they will be available.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

2.  Filter the name field to locate and open **sn\_pw.enable\_resource\_planning**.

3.  Change the scope of the instance to **Project Workspace**.

4.  Clear the Value field and enter **true**.

5.  Select **Update**.


**Parent Topic:**[Migration of resource plans, operational resource plans, and cost plans](../concept/rsrc-plans-rsrc-asgmnts.md)

