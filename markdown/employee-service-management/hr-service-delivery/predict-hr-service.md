---
title: Auto determination of HR service
description: Auto determine the HR service for a case. Enable an HR agent to transfer the case to the appropriate HR service rather than having to spend significant time manually triaging cases to appropriate HR services.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integrate with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Auto determination of HR service

Auto determine the HR service for a case. Enable an HR agent to transfer the case to the appropriate HR service rather than having to spend significant time manually triaging cases to appropriate HR services.

**Important:** This feature is available with the HR Professional and HR Enterprise packages when you activate the HR Service Delivery and Predictive Intelligence applications. If you do not want to use this feature, disable the **sn\_hr\_core.case\_auto\_categorization** system property.

## Auto-determined HR service displayed in a banner

After you create a case, the HR Case Classification solution definition auto determines the HR service based on the short description of the case. The appropriate HR service for the case is displayed in a banner.

**Important:** The banner is not displayed if:

-   you have logged the case under the correct HR service
-   you have manually transferred or auto-transferred the case
-   case is not in the ready or draft state

You can also transfer the case from one HR service to another, without losing the case number or content, using the link on the banner. The auto-determined HR service is selected by default on the Transfer case window. You can ignore the auto-determined HR service for the case, choose to transfer the case to a different HR service, or continue with the HR service that was provided earlier.

## Auto training the predictive model

The HR Case Classification solution definition is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   There are 10000 records of HR case study matching the filters defined in the solution definition.
-   The**glide.platform\_ml.auto\_training.enabled** system property is set to true.

You can [manually train the predictive model](../task/hr-predictive-intelligence-train.md) if it is not auto trained by default. Later, navigate to the **HR AI configuration** module, open the HR Case Classification record, and map the configured solution definition.

