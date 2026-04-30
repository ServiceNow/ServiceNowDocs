---
title: Legacy SLA fields
description: Previously, only a single SLA could be attached to a task via the Escalation engine. The information for the SLA was stored in the task table using the SLA Due, Made SLA, and Escalation fields.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Level Agreement \(Legacy\) engines, Service Level Management reference, Service Level Management, IT Service Management]
---

# Legacy SLA fields

Previously, only a single SLA could be attached to a task via the Escalation engine. The information for the SLA was stored in the task table using the **SLA Due**, **Made SLA**, and **Escalation** fields.

The Task SLA engine now enables multiple SLAs to be attached to a single task, making the earlier task fields redundant. Their equivalents are in the **task\_sla** table for each SLA attached to the task.

-   **Task SLA**, **Breach time**: This is equivalent to the SLA Due field
-   **Task SLA**, **Has breached**: This will be true if the SLA has breached, the opposite of **Made SLA** field.
-   There is no equivalent field for **Escalation** field. Notifications can be sent via the SLA workflow and an increase in priority can trigger additional SLAs to be attached to the task.

**Note:** The **Business Duration** field is neither part of the Escalations Engine nor the Task SLA Engine.

The fields on the **Task** are considered legacy and are not updated by the Task SLA engine. In case these fields are being updated, the legacy Escalation engine may still be running. This can happen if you have upgraded from Express or a previous instances.

To prevent the Escalation engine from running, set the **com.snc.sla.run\_old\_sla\_engine** property to false. If this property is set to false and the fields are still being updated, check the customizations made to your instance.

**Parent Topic:**[Service Level Agreement \(Legacy\) engines](c_GetStartedWithSLAs.md)

