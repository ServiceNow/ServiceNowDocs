---
title: Configuring HR Service Delivery Integration with Workday
description: Pull Workday tasks or to-dos on regular scheduled basis or on manual basis for provided date range into ServiceNow instance. This allows the employees to view all their to-dos in a single place, Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/w-todos.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Integration with Workday, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery Integration with Workday

Pull Workday tasks or to-dos on regular scheduled basis or on manual basis for provided date range into ServiceNow instance. This allows the employees to view all their to-dos in a single place, Employee Center.

## Application setup

-   Activate the HR Service Delivery Integration with Workday application from ServiceNow Store. This automatically activates the Workday HR Spoke.
-   Set up [Workday HR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/workday-hr-spoke.md) [Workday HR Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/workday-hr-spoke.md) .
-   Activate the HR Service Delivery Integrations Framework from ServiceNow Store. HR Service Delivery Integration with Workday uses Enterprise Service Management Integrations Framework to pull tasks from Workday into ServiceNow. For more information on HR Service Delivery Integrations Framework, see [Enterprise Service Management Integrations Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/hr-integrations-framework.md).


## To-dos settings

Store one-time configuration parameters for pulling tasks from Workday into ServiceNow. For more information, see [Configure Workday to-dos](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/config-w.md).

**Note:** The **HRSD Framework Integration** and **HRSD Integration Framework Complete** to-dos configurations help to display Workday tasks in the To-dos page in Employee Center. For more information on these to-dos configurations, navigate to **Employee Center** &gt; **To-dos Configuration**.

## Schedule flow activation

Activate and run the schedule flow that pulls tasks into ServiceNow. For more information, see [Activating schedule flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/activate-w-schedule-flow.md).

