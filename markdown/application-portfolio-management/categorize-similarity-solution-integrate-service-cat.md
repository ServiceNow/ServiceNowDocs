---
title: Categorize applications with similarity solution - Legacy
description: Use the machine-learning engine to suggest a category for a business application that you are registering into the Enterprise Architecture inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/categorize-similarity-solution-integrate-service-cat.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Categorize applications with similarity solution - Legacy

Use the machine-learning engine to suggest a category for a business application that you are registering into the Enterprise Architecture inventory.

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

    As you enter the name and benefit of the business application, the similarity solution triggers. The machine-learning algorithm searches for similar business applications in the business applications table \[cmdb\_ci\_business\_app\]. When the engine finds similar records, a message appears on the form. Based on the findings, the engine suggests a category for the application you are registering. The suggested category displays in the **Category of the business application** field.

    If you select the category predicted by the machine-learning solution, the application category is stored in the **ML Predicted Category** field of the Business Application Requests table \[business\_app\_request\]. This data is used for future analysis.

4.  Select the ML suggested category if it is suitable.

5.  Click **Submit**.


**Parent Topic:**[Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/apm-integration.md)

