---
title: Legal name change configuration
description: Complete the legal name change configuration to allow employees to change their legal name through virtual agent conversation in Employee Center.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Legal name change configuration

Complete the legal name change configuration to allow employees to change their legal name through virtual agent conversation in Employee Center.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **All** &gt; **Workday Advanced Use Cases** &gt; **Legal Name Change** &gt; **Document Categories**.

2.  To pull the legal name change document categories from Workday into a ServiceNow application, click **Get Reference IDs**.

    A data source with a predefined script imports document categories into the Workday Reference ID List Staging \[sn\_hr\_workday\_adv\_reference\_id\_list\_staging\] table and from staging table into the Workday Reference ID List \[sn\_hr\_workday\_adv\_reference\_id\_list\] table.


## What to do next

1.  Navigate to **Workday Advanced Use Cases** &gt; **Legal Name Change** &gt; **Configuration**.
2.  On the Legal Name Change Configurations form, click **New**.
3.  To allow an employee to upload the name change document in Virtual Agent conversation in Employee Center, click the **Enable document upload** option and select a relevant document category.
4.  Click **Submit**.

