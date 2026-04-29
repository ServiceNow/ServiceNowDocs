---
title: Discovering knowledge articles and catalog items for employees
description: Discover all the users who have a similar profile as the employee who has logged in to Employee Service Center. Identify the top viewed knowledge articles and top submitted catalog items by those users. Display the top three knowledge articles and top three catalog items to the employee.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Discovering knowledge articles and catalog items for employees

Discover all the users who have a similar profile as the employee who has logged in to Employee Service Center. Identify the top viewed knowledge articles and top submitted catalog items by those users. Display the top three knowledge articles and top three catalog items to the employee.

## Top three knowledge articles and top three catalog items

When the User Profile Based Recommendation \(ml\_sn\_sn\_hr\_core\_global\_user\_profile\_based\_recommendation\) solution definition is configured and the predictive model is trained, the top three knowledge articles and top three catalog items are displayed to an employee in Employee Service Center and HR Ticket page.

![The top viewed knowledge articles and top submitted catalog items as displayed to an employee.](../image/KBarticles-catalogitems.png)

## Auto training the predictive model

By default, the User Profile Based Recommendation solution definition is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   The**glide.platform\_ml.auto\_training.enabled** system property is set to true.

You can [manually train the predictive model](../task/hr-predictive-intelligence-train.md) if it is not auto trained by default. After you manually train the predictive model, navigate to the **HR AI configuration** module, open the Similar users group record, and map the configured solution definition.

## Configuring widget options

You can also configure the following widget options:

-   **User prediction count**: Number of similar users discovered by the predictive model. By default, the top 25 similar users are discovered for the user.
-   **Recent activity cut off days**: Number of days considered by the predictive model for querying the articles and catalog items. By default, the last 30 days activity is checked from the Knowledge Use table, Requested Items table, and Items Produced Records table.

To configure the widget options, navigate to the **Service Portal Configuration** module, select the widget editor, search for **Relevant for you**, and click **Edit Option Schema**.

**Parent Topic:**[Machine learning solutions for HR Service Delivery](predictive-intelligence-for-hr-service-delivery-1.md)

