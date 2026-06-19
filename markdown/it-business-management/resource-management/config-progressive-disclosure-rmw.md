---
title: Configure progressive disclosure for the resource board
description: Limit the number of users loaded on the resource board in the Resource Management Workspace to reduce performance impact on instances with large user datasets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/resource-management/config-progressive-disclosure-rmw.html
release: zurich
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [progressive disclosure, resource board performance, resource management workspace, system property, user loading limit]
breadcrumb: [Configure, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure progressive disclosure for the resource board

Limit the number of users loaded on the resource board in the Resource Management Workspace to reduce performance impact on instances with large user datasets.

## Before you begin

Role required: admin

## About this task

The resource board in Resource Management Workspace loads up to 200 users by default. If your organization manages many users and the board is experiencing performance impact, set the **com.snc.resource\_management.progressive\_disclosure** property to **false** to reduce the initial load to 100 users.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

2.  Filter the Name field to locate and open **com.snc.resource\_management.progressive\_disclosure**.

3.  In the Value field, enter **false**.

    Setting the value to **false** limits the resource board to load 100 users. The default value is **true**, which loads up to 200 users.

4.  Select **Update**.


## Result

The resource board loads a maximum of 100 users. To restore the default behavior and load up to 200 users, set the property value back to **true**.

**Parent Topic:**[Configure Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/resource-management/configure-rmw.md)

