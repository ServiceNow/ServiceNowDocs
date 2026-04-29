---
title: Discovering similar closed cases for HR cases
description: Help an HR agent resolve the current case by displaying similar closed cases.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Discovering similar closed cases for HR cases

Help an HR agent resolve the current case by displaying similar closed cases.

## Similar Closed HR Cases

When the Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is trained, the **Similar Closed HR cases** option is displayed on an HR case. This option displays the most relevant HR closed cases to an HR agent to help resolve the current HR case.

![Similar Closed HR cases option on the Related Search Results in HR case.](../image/similar-closed-cases.png "Similar Closed HR Cases")

## Auto training the predictive model

The Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence for Contextual Search \(com.snc.contextual\_search\_ml\) plugin is installed.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set either set to true or absent.

**Parent Topic:**[Machine learning solutions for HR Service Delivery](predictive-intelligence-for-hr-service-delivery-1.md)

