---
title: Create the category and table
description: After the request has been submitted, a catalog administrator can approve or reject the request.
locale: en-US
release: yokohama
product: Service Creator
classification: service-creator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage a service, Service Creator, Build workflows]
---

# Create the category and table

After the request has been submitted, a catalog administrator can approve or reject the request.

## Before you begin

Role required: admin

## About this task

Approving the request creates a new table for the service category, adds an application to the application navigator using the Category name as the application label, and sets the State of the service category to Published to Catalog.

## Procedure

1.  Navigate to **All** &gt; **Service Creator** &gt; **Category Requests**.

2.  Open a record with a **State** of **Requested**.

3.  Review the requested service category. ServiceNow provides a suggested **Table name** based on the **Department**.

    If a service category exists with the specified category name or table name, a message appears under that field. Use a unique value for these fields.

4.  Click **Create Category and Table** to approve the request or **Reject** to reject the request.

    If notifications are enabled for the instance, the service category **Manager** is notified of the approval or rejection.

    ![Service Creator Approve Category](../image/ServiceCreatorApproveCategory.png)

    After publishing the service category, you can access the new table by navigating to the new application in the application navigator, or by clicking the **View Task List** related link on the Service Category form.


**Related topics**  


[Manage a service](t_ManagingServices.md)

