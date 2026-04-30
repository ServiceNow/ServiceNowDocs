---
title: Auto determination of assignment group
description: Auto determine the assignment group for a case. Enable an HR agent to transfer the case to correct assignment group rather than having to spend significant time manually identifying groups for HR cases.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Auto determination of assignment group

Auto determine the assignment group for a case. Enable an HR agent to transfer the case to correct assignment group rather than having to spend significant time manually identifying groups for HR cases.

**Important:** This feature is available with the HR Professional and HR Enterprise packages when you activate the HR Service Delivery and Predictive Intelligence applications. To use this feature, enable the **sn\_hr\_core.case\_auto\_assignment** system property.

## Auto-determined assigned group displayed in a banner

After you create a case, the Auto Assignment Group for HR Cases solution definition auto determines the assignment group for a case based on the Short description, Description, Opened for Title, Opened for Location Name, and HR service of the case. The appropriate assignment group for the case is displayed in a banner.

**Important:** The banner is not displayed if:

-   You have manually assigned the case to an assignment group.
-   The assignment group is not identified for the case.
-   The case is not in the ready or draft state.

## Auto training the predictive model

By default the Auto Assignment Group for HR Cases solution definition is configured and the predictive model is auto trained when all of the following conditions are met.

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   There are 10000 records of HR case study matching the filters defined in the solution definition.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

You can [manually train the predictive model](hr-predictive-intelligence-train.md) if it is not auto trained by default. After you manually train the predictive model, navigate to the **HR AI configuration** module, open the Case Assignment group record, and map the configured solution definition.

**Parent Topic:**[Machine learning solutions for HR Service Delivery](../concept/predictive-intelligence-for-hr-service-delivery-1.md)

