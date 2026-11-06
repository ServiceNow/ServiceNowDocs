---
title: Style rules definition
description: You can create a style span to specify the color for different events in a change schedule. Style spans in a schedule help to quickly identify characteristics of a change based on a field value from the Change Request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/style-rules-definition.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Style rules definition

You can create a style span to specify the color for different events in a change schedule. Style spans in a schedule help to quickly identify characteristics of a change based on a field value from the Change Request.

Change Schedules includes several base styles to ensure every schedule has span styles to begin with. By default, Blackout Schedules are represented by a gray color, Maintenance schedules are represented by a light blue color and change requests are represented by either red \(risk = High\), orange \(risk = moderate\), or green \(risk = low\).

To define style rules, you must activate Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).

You can define styles in multiple ways, such as from the Default Style Rules, Change Schedule definitions, or from the Span Style window in the Change Schedule timeline.

**Note:** All style rule tables extend the Style Rule Core table \[chg\_soc\_style\_rule\_core\].

-   **[Define default style rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/def-stl-rules-from-stl-rules-table.md)**  
Define style rules from the Default Style Rules module to apply them to all change schedules rather than to a specific application.
-   **[Define style rules from Change Schedule Definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/def-stl-rules-from-chng-sch-def.md)**  
Define style rules from a change schedule definition to apply them to the change schedule that's related to the definition.
-   **[Define style rules from the change schedules view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/define-style-rules-from-view.md)**  
Create style rules from the change schedules view to apply them to the specific change schedule where they're defined.

**Parent Topic:**[Change schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-schedule.md)

**Related topics**  


[Change schedules view]()

[Create a change schedule from the Change Schedules page]()

[Create a change schedule from the change schedule definition]()

[Add related tasks to a change schedule]()

