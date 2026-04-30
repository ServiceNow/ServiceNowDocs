---
title: Configuring HR Service Delivery Integration with Workday
description: Pull Workday tasks or to-dos on regular scheduled basis or on manual basis for provided date range into ServiceNow instance. This allows the employees to view all their to-dos in a single place, Employee Center.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery Integration with Workday

Pull Workday tasks or to-dos on regular scheduled basis or on manual basis for provided date range into ServiceNow instance. This allows the employees to view all their to-dos in a single place, Employee Center.

## Application setup

-   Activate the HR Service Delivery Integration with Workday application from ServiceNow Store. This automatically activates the Workday HR Spoke.
-   Set up [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) .
-   Activate the HR Service Delivery Integrations Framework from ServiceNow Store. HR Service Delivery Integration with Workday uses Enterprise Service Management Integrations Framework to pull tasks from Workday into ServiceNow. For more information on HR Service Delivery Integrations Framework, see [Enterprise Service Management Integrations Framework](hr-integrations-framework.md).


## To-dos settings

Store one-time configuration parameters for pulling tasks from Workday into ServiceNow. For more information, see [Configure Workday to-dos](../task/config-w.md).

**Note:** The **HRSD Framework Integration** and **HRSD Integration Framework Complete** to-dos configurations help to display Workday tasks in the To-dos page in Employee Center. For more information on these to-dos configurations, navigate to **Employee Center** &gt; **To-dos Configuration**.

## Schedule flow activation

Activate and run the schedule flow that pulls tasks into ServiceNow. For more information, see [Activating schedule flows](../task/activate-w-schedule-flow.md).

