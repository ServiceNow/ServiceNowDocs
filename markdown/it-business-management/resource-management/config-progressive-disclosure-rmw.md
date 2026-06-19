---
title: Configure progressive disclosure for the resource board
description: Configure whether the resource board in the Resource Management Workspace uses progressive disclosure to load users incrementally or loads all 200 users at once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/config-progressive-disclosure-rmw.html
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [progressive disclosure, resource board performance, resource management workspace, system property, user loading limit]
breadcrumb: [Configure, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure progressive disclosure for the resource board

Configure whether the resource board in the Resource Management Workspace uses progressive disclosure to load users incrementally or loads all 200 users at once.

## Before you begin

Role required: admin

## About this task

The resource board in Resource Management Workspace uses progressive disclosure by default to load users incrementally and reduce performance impact. Setting the **com.snc.resource\_management.progressive\_disclosure** property to **false** disables this behavior and loads all 200 users at once, which may affect performance on instances with large user datasets.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

2.  Filter the Name field to locate and open **com.snc.resource\_management.progressive\_disclosure**.

3.  In the Value field, enter **false**.

    Setting the value to **false** disables progressive disclosure and loads all 200 users at once, which may be slower on instances with large user datasets. The default value is **true**, which enables progressive disclosure for faster initial load.

4.  Select **Update**.


## Result

The resource board loads all 200 users at once. To restore progressive disclosure and improve load performance, set the property value back to **true**.

**Parent Topic:**[Configure Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/configure-rmw.md)

