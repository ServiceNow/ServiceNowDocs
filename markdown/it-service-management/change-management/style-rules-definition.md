---
title: Style rules definition
description: You can create a style span to specify the color for different events in a change schedule. Style spans in a schedule help to quickly identify characteristics of a change based on a field value from the Change Request.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Style rules definition

You can create a style span to specify the color for different events in a change schedule. Style spans in a schedule help to quickly identify characteristics of a change based on a field value from the Change Request.

Change Schedules includes several base styles to ensure every schedule has span styles to begin with. By default, Blackout Schedules are represented by a gray color, Maintenance schedules are represented by a light blue color and change requests are represented by either red \(risk = High\), orange \(risk = moderate\), or green \(risk = low\).

To define style rules, you must activate Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).

You can define styles in multiple ways, such as from the Default Style Rules, Change Schedule definitions, or from the Span Style window in the Change Schedule timeline.

**Note:** All style rule tables extend the Style Rule Core table \[chg\_soc\_style\_rule\_core\].

-   **[Define default style rules](../task/def-stl-rules-from-stl-rules-table.md)**  
You can define style rules from the Default Style Rules module when you want the style rules to be used by change schedules globally and not for any specific application.
-   **[Define style rules from Change Schedule Definitions](../task/def-stl-rules-from-chng-sch-def.md)**  
You can define style rules from change schedule definitions when you want the style rules to be applied to the change schedule related to the change schedule definition.
-   **[Define style rules from Change Schedules View](../task/define-style-rules-from-view.md)**  
You can create style rules from the change schedules view when you want the style rules to be applied to the specific change schedule where it is defined.

**Parent Topic:**[Change schedules](change-schedule.md)

**Related topics**  


[Change schedules view](change-schedules-view.md)

[Create a change schedule from the Change Schedules page](../task/create-chng-sch-from-chng-sch-page.md)

[Create a change schedule from the change schedule definition](../task/create-chng-sch-from-chng-sch-def.md)

[Add related tasks to a change schedule](../task/add-related-tasks-to-chng-schedule.md)

