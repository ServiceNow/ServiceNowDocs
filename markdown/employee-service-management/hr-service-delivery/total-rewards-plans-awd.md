---
title: Set up plans for Total Rewards
description: Complete the one time set up of pulling plans, such as employee benefits plan, compensation plan, insurance plan, from Workday into the ServiceNow application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up total rewards, Configure, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up plans for Total Rewards

Complete the one time set up of pulling plans, such as employee benefits plan, compensation plan, insurance plan, from Workday into the ServiceNow application.

## Before you begin

Role required: sn\_hr\_workday\_adv.admin

## Procedure

1.  Navigate to **All** &gt; **Workday Advanced Use Cases** &gt; **Total Rewards** &gt; **Plans Available**.

2.  Click **Get Reference IDs** to pull the plans from Workday into ServiceNow tables.

    **Note:** The plans from Workday are pulled into Workday Reference ID List Staging \[sn\_hr\_workday\_adv\_reference\_id\_list\_staging\] table and from staging table into Workday Reference ID List \[sn\_hr\_workday\_adv\_reference\_id\_list\] table.

3.  On the form, view the fields:

    |Field|Description|
    |-----|-----------|
    |Descriptor|Description of the plan that is pulled from Workday.|
    |Descriptor ID|Descriptor ID of the plan that is pulled from Workday.|
    |Workday ID|Unique identifier that is generated from Workday.|
    |Reference ID Type|Reference ID of the plan that is pulled from Workday. For example, Compensation Plan ID, Health Care Coverage Plan ID, and Insurance Coverage Plan ID.|


