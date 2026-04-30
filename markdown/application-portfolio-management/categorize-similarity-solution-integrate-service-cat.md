---
title: Use similarity solution to categorize applications and integrate with service catalog
description: Use the machine-learning engine to suggest a category for a business application that you are registering into the APM inventory.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrate, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Use similarity solution to categorize applications and integrate with service catalog

Use the machine-learning engine to suggest a category for a business application that you are registering into the APM inventory.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

Using the Register a Business Application form to on-board an application in Enterprise Architecture \(formerly APM\) is similar to requesting an item from Service Catalog category.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Business Application Lifecycle Management** &gt; **Business Application Catalog**.

2.  Click the **Register a Business Application** card to register a new business application.

3.  Enter the details in the Register a Business Application form.

    Mandatory fields have a red asterisk \(\*\) beside them.

    |Field|Description|
    |-----|-----------|
    |Enter the name of the business application|Name of the business application that you are requesting or registering.|
    |Benefit or use of the business application|Purpose of the business application.|
    |IT Owner of the Business Application|Name of the IT owner of the application.|
    |Business Owner of the Business Application|Name of the business owner of the application.|

    ![Register a business application form with category suggested by ML](../image/MLSuggestedCategory.png "Register a business application")

    As you enter the name and the benefit of the business application, the similarity solution of the machine-learning algorithm is triggered to search for a similar business application from the business applications table \[cmdb\_ci\_business\_app\]. Once the engine finds similar records, you can see a message on top of the form indicating that the ML found similar records in the applications table. Based on the findings the engine suggests a category for the application that you are registering. It also displays the suggested category in the **Category of the business application** field under which the business application can possibly be grouped.

    If you choose to select the category predicted and suggested by the machine-learning solution, then the application category is stored in the **ML Predicted Category** field of the Business Application Requests table \[business\_app\_request\] for future analysis.

4.  Select the ML suggested category if it is suitable.

5.  Click **Submit**.


**Parent Topic:**[Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications](../concept/apm-integration.md)

