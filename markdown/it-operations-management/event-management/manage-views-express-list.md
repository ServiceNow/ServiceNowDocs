---
title: Configuring Express List views for users and user groups
description: Centrally control what users monitor by predefining views in Express List and assigning them to users and user groups.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configuring Express List views for users and user groups

Centrally control what users monitor by predefining views in Express List and assigning them to users and user groups.

As an Event Management admin, you can create Express List views to ensure that users focus on specific services, priorities, or alerts. Event Management enables you to define the filters, column order, and filter attributes for an Express List view and then assign the view to individual users and user groups.

Users belonging to a group can only see the predefined views you assigned to that group and their own saved views. If a user belongs to multiple groups, they can see the views you assigned to all of these groups. Users can switch between views and modify and save all views except their assigned default view. However, they can't override settings in any of their assigned views and modify or share their default view.

The filter conditions builder enables you to configure AND and OR conditions between attributes.

![Express List view filter conditions sample.](../image/manage-views-filter-conditions.png "Express List view filter conditions")

For example, the admin can configure conditions that allow the user to see only alerts that are not assigned to an assignment group or in maintenance. In the example, the alerts must also contain a value of email\_sid and must be from one of the specified sources.

-   **[Create a predefined Express List view for users](../../event-management/task/manage-views-express-list-admin.md)**  
Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view and assign it to individual users or user groups.
-   **[Assign users and groups to predefined Express List views](../../event-management/task/assign-operator-view-in-express-list.md)**  
Assign individual users and user groups to preconfigured Express List views to make sure that they focus on specific services, priorities, or alerts.

**Parent Topic:**[Manage and monitor alerts](../../event-management/concept/c_EMAlert.md)

**Related topics**  


[Create a predefined Express List view for users](../../event-management/task/manage-views-express-list-admin.md)

[Identify an assigned Express List view](../task/manage-views-express-list-operator.md)

