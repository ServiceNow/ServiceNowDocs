---
title: View tasks of a third-party system
description: View tasks that are pulled from the third-party system into Enterprise Service Management Integrations Framework.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Enterprise Service Management Integrations Framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# View tasks of a third-party system

View tasks that are pulled from the third-party system into Enterprise Service Management Integrations Framework.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

## Procedure

1.  Navigate to **All** &gt; **Integrations Framework** &gt; **Todos**.

2.  View details of tasks.

    |Field|Description|
    |-----|-----------|
    |Integration todo ID|Unique identifier for the integration Todo.|
    |Todo description|Description of the Todo or task in the third-party system.|
    |Todo state|State of the Todo or task in ServiceNow system, such as Open or Closed.|
    |Active|Option indicating whether the Todo or task is active in the third-party system.|
    |Assigned to|User to whom the Todo or task is assigned.|
    |External Status|Status of the Todo or task in external system.|
    |Extension System|Option indicating the origin of Todo or task.|
    |Domain|Option indicating that domain separation is enabled for this table.|
    |Approving|Option to approve a document that is pulled from a ServiceNow system or a third-party system. On selecting this option, a window appears that allows you to specify a table and select a document from the table.|

    **Important:**

    -   By default, the Auto Flush data retention policy removes to-dos after seven days. If you do not want the to-dos to be removed from the table:
        1.  Navigate to **System Maintenance** &gt; **Table Cleanup** and select **sn\_hr\_integr\_fw\_todo\_inbound**.
        2.  To inactivate the retention policy, deselect the **Active** checkbox.
        3.  To specify a different condition in the retention policy, add a script in the **Condition** field.
    -   If you want use the Pulled Integration To-do table to pull to-dos or tasks from a third-party system, then you must create an implementation of this extension point: sn\_hr\_integr\_fw.TodoTransformHelper.

