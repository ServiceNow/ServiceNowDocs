---
title: Discovering similar knowledge articles for HR cases
description: Discover similar information across knowledge articles based on the short description of the HR case and the text in the related search results. Display such similar knowledge articles to an HR agent to resolve a case.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Discovering similar knowledge articles for HR cases

Discover similar information across knowledge articles based on the short description of the HR case and the text in the related search results. Display such similar knowledge articles to an HR agent to resolve a case.

## Similar knowledge articles

The similarity solution takes the short description of the case and compares them to the short description, description, and text fields of the published articles to provide the similar knowledge articles.

When the Similar Knowledge Articles for HR Case \(ml\_sn\_sn\_hr\_core\_global\_case\_to\_articles\) is configured and the predictive model is trained, the **Similar Knowledge Articles** option is displayed on an HR case. This option displays the most relevant knowledge articles to an HR agent to resolve an HR case.![Relevant knowledge articles for an HR case](../image/attach-knowledge-article-to-hr-case-1.png)

## Auto training the predictive model

The Similar Knowledge Articles for HR Case solution definition is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence for Contextual Search \(com.snc.contextual\_search\_ml\) plugin is installed.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

You can also [manually train the predictive model](hr-predictive-intelligence-train.md) if it is not auto trained by default.

**Parent Topic:**[Machine learning solutions for HR Service Delivery](../concept/predictive-intelligence-for-hr-service-delivery-1.md)

