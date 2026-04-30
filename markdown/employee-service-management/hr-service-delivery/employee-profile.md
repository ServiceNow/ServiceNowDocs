---
title: Employee Profile table
description: The Employee Profile \(sn\_employee\) plugin provides an Employee Profile \(sn\_employee\_profile\) table that makes the employment start date and employment end date fields available outside of HR Service Delivery. For example, the table can be used with Strategic Portfolio Management to update the resource capacity of users.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Employee Profile table

The Employee Profile \(sn\_employee\) plugin provides an Employee Profile \(sn\_employee\_profile\) table that makes the employment start date and employment end date fields available outside of HR Service Delivery. For example, the table can be used with Strategic Portfolio Management to update the resource capacity of users.

## Overview

Use the Employee Profile \(sn\_employee\_profile\) table to make the **employment\_start\_date** and **employment\_end\_date** fields available outside of HR Service Delivery.

Learn more about the [Employee profile](../../employee-center/concept/employee-profile-portal.md).

|Field|Description|
|-----|-----------|
|user|Reference to the User \(sys\_user\) table.|
|employment\_start date|Represents the employment start date.|
|employment\_end\_date|Represents the employment end date.|

## If you are using Employee Profile with HR Service Delivery

When you activate the Employee Profile plugin, the following fields are pulled from the HR Profile \(sn\_hr\_core\_profile\) table to populate the Employee Profile \(sn\_employee\_profile\) table.

|Field|Description|
|-----|-----------|
|employment\_start\_date|Represents the employment start date.|
|employment\_end\_date|Represents the employment end date.|

**Sync employee profile from HR profile** is a one-time scheduled job that will pull all users with their corresponding employment\_start\_date and employment\_end\_date values from the HR Profile table upon plugin activation. Subsequent updates will be made by the **Synchronize fields to HR profile** and **Synchronize fields to employee profile** business rules.

**Note:** If you need to run the one-time scheduled job again, make sure to first activate the job and allow for the invalidated RCA before running it. Do not run the job on a scheduled basis.

## Activation information

You must activate the Employee Profile \(sn\_employee\) plugin to use the Employee Profile table with your application.

**Note:** If you are using the table with Strategic Portfolio Management, see [Update the resource capacity](https://www.servicenow.com/docs/access?context=update-resource-capacity&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

-   **[Activate Employee Profile](../task/activate-employee-profile.md)**  
You can activate the Employee Profile plugin \[sn\_employee\] if you have the admin role.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

