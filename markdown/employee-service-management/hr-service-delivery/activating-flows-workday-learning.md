---
title: Activate schedule flows
description: Activate the schedule flow that interacts with Workday Learning to pull user profile information and tasks into a ServiceNow application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure HR Service Delivery Integration with Workday Learning, HR Service Delivery Integration with Workday Learning, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Activate schedule flows

Activate the schedule flow that interacts with Workday Learning to pull user profile information and tasks into a ServiceNow application.

## Before you begin

Role required: sn\_lrn\_workday.admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Flows** option.

3.  Select **Run Workday Integration Flow** in the available flows.

4.  Select **Activate**.

5.  In the **Trigger** field, specify the time and interval at which you want to automatically run the scheduled flow.

    This flow in turn triggers the subflows to automate tasks. To customize the sample flow, copy it to the required application scope.

    Available subflows include:

    |Subflow|Description|
    |-------|-----------|
    |Assign Course to Workday Learning|Assigns learning courses to the ServiceNow users.|
    |Pull Courses from Workday Learning|Retrieves details of the learning courses and maps courses from Workday Learning to ServiceNow.|
    |Pull User Activity from Workday Learning|Retrieves user course activity data from Workday Learning and saves it in the ServiceNow instance.|
    |Track Approval for Workday Learning|Retrieves details of learning todos from Workday Learning and saves it in the ServiceNow instance.|
    |Workday Learning User Mapping|Maps users between Workday Learning and ServiceNow instance|

    Once data is pulled into staging tables, transform maps move data into target tables. For more details, refer to [Use transform maps](../concept/use-transform-maps-wd-learning.md).


