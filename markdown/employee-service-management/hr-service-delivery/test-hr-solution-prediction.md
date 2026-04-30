---
title: Test an HR solution prediction
description: Test the solution prediction by sending emails to the general email address for HR requests. Verify that the corresponding HR cases are automatically categorized to the appropriate HR service.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Auto-case creation from an email, Machine learning solutions for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Test an HR solution prediction

Test the solution prediction by sending emails to the general email address for HR requests. Verify that the corresponding HR cases are automatically categorized to the appropriate HR service.

## Before you begin

Role required: sn\_hr\_core.admin or sn\_hr\_core.case\_reader

## Procedure

1.  Send an email to the general email address for HR requests.

    **Note:** To verify the general email address for HR requests, navigate to **HR Administration** &gt; **Properties**, and view the **General email address for HR requests** property.

2.  Navigate to **HR Case Management** &gt; **All HR Cases**, and open one of the modules, such as **Assigned to me** or **Open**.

3.  Open the applicable record.

4.  Verify that the HR case was automatically categorized to the appropriate COE and HR service.


## What to do next

If you need to retrain and review your predictive model, see [Create and train a solution definition](https://www.servicenow.com/docs/access?context=create-solution-definition&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and [Review classification solution statistics](https://www.servicenow.com/docs/access?context=review-solution-statistics&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

