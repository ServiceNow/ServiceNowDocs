---
title: Set business hours for tasks in Jeopardy Management
description: Use the sn\_ind\_tmt\_orm.order\_task\_schedule system property to set business hours for tasks in Jeopardy Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/set-business-hrs-jmtasks.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Set business hours for tasks in Jeopardy Management

Use the sn\_ind\_tmt\_orm.order\_task\_schedule system property to set business hours for tasks in Jeopardy Management.

## Before you begin

The application scope must be set to Order Management.

Role required: admin

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **sn\_ind\_tmt\_orm.order\_task\_schedule** system property.

3.  In the **Value** field, enter `true`.

    **Note:** The default value for the property is set to **False**.

4.  Select **Update**.

    Business hours are used for tasks in Jeopardy Management.


**Related topics**  


[Jeopardy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/jeopardy-management.md)

[Monitoring order jeopardy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/monitoring-jeopardy-management.md)

