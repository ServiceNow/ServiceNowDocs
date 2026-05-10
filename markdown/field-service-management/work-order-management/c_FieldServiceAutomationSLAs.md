---
title: Field Service Management SLAs
description: ServiceNow SLAs track the service level provided by groups and individuals.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Field Service Management SLAs

ServiceNow SLAs track the service level provided by groups and individuals.

When you create a work order, the system automatically assigns it a default [Service Level Management concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/service-level-management-concepts.md) based on priority level. If you change the priority of the work order, the system cancels the current SLA and applies the SLA appropriate for the new priority. The SLA timer continues to run even if the priority is changed. The three default SLAs used for work orders are:

|SLA|Description|
|---|-----------|
|WM - 5 business days|Assigned to work orders with a priority level of 4 \(Low\)|
|WM - Next business day|Assigned to work orders with a priority level of 3 \(Moderate\)|
|WM - Same business day|Assigned to work orders with a priority level of 2 \(High\) or 1 \(Critical\)|

Users with the wm\_admin role can create and edit SLAs or delete them from work orders. Changes to an SLA are used in new work orders, but they do not affect existing work orders that use the SLA.

**Note:** The SLA applies to the work order. All associated work order tasks must be completed within the SLA time period to meet the SLA.

SLA details show on the task card in the task panel and the calendar in the Dispatcher Workspace. The number on the card in the task panel is the amount of time remaining before the SLA is breached. The horizontal line that appears under the task in the calendar view is a task bar. The bar and the number in the task panel, indicate the state of task SLA with different colors based on the following SLA durations.

|SLA duration|Bar color|
|------------|---------|
|Below 50%|Green|
|In-between 50% and 75%|Yellow|
|In-between 75% and 100%|Orange|
|Above 100% \(breached\)|Red|
|Paused|Gray|

**Related topics**  


[Manage a work order SLA](../task/t_ManageAWorkOrderSLA.md)

