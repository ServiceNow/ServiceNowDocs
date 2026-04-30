---
title: Customize Lists in Strategic Planning Workspace
description: Add custom tables to the Lists menu in Strategic Planning Workspace.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing Lists in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Customize Lists in Strategic Planning Workspace

Add custom tables to the Lists menu in Strategic Planning Workspace.

## Before you begin

-   Ensure that your application scope is set to **Portfolio Planning**.
-   [Enable adding custom tables to the Lists menu](../../portfolio-planning/task/enable-adding-custom-tables-to-the-lists-menu.md).

Role required: admin

## About this task

Lists menu in the Workspace homepage helps planning managers quickly find a record that they need. By default, this view shows the list of entities of all the planning items and lens available for this ServiceNow instance. If your planning managers need more categories or lists, you can add them.

For more information of configuring lists in a workspace, see [Lists](https://www.servicenow.com/docs/access?context=migration-lists&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **sys\_ux\_list\_menu\_config.list**.

2.  From the UX List Menu Configurations list, select **APW List Menu Configuration**.

3.  Select a new category or a new list.

    |Option|Action|
    |------|------|
    |**New category**|From the UX List Categories related list, select **New**.|
    |**New list**|From the UX Lists related list, select **New**.|

    **Tip:** Create a category first and then create a list.

4.  On the form, fill in the fields.

    -   [UX List Category form](../reference/ux-list-category-form.md).
    -   [UX List form](../reference/ux-list-form.md).
5.  Select **Submit**.

    Repeat this procedure until you've created all the custom categories and lists.


## What to do next

[Define audience for new lists in Strategic Planning](define-audience-for-new-lists-strategic-planning.md).

