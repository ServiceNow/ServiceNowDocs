---
title: Customize Lists in Portfolio Planning Workspace
description: Add custom tables to the Lists menu in Portfolio Planning Workspace.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customizing Lists in Portfolio Planning Workspace, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Customize Lists in Portfolio Planning Workspace

Add custom tables to the Lists menu in Portfolio Planning Workspace.

## Before you begin

Role required: admin

-   Ensure that your application scope is set to **Portfolio Planning**.
-   [Enable adding custom tables to the Lists menu](enable-adding-custom-tables-to-the-lists-menu.md).

## About this task

Lists menu in the Workspace homepage helps planning managers quickly find a record that they need. By default, this view shows the list of entities of all the planning items and lens available for this ServiceNow instance. If your planning managers need more categories or lists, you can add them.

For more information of configuring lists in a workspace, see [Lists](https://www.servicenow.com/docs/access?context=migration-lists&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

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

    -   [UX List Category form](../reference/ux-list-category-form-portfolio-planning.md).
    -   [UX List form](../reference/ux-list-form-portfolio-planning.md).
5.  Select **Submit**.

    Repeat this procedure until you've created all the custom categories and lists.


