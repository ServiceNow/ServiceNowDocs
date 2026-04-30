---
title: Similar closed cases in HR Service Delivery Agent Workspace
description: Help an HR agent resolve the current case by displaying similar closed cases.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions for HR Service Delivery Agent Workspace, Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Similar closed cases in HR Service Delivery Agent Workspace

Help an HR agent resolve the current case by displaying similar closed cases.

**Important:** This feature is available with the HR Professional and HR Enterprise packages when you activate HR Service Delivery Agent Workspace and Predictive Intelligence applications.

## Similar Closed HR Cases

When the Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is trained:

-   Similar closed cases are displayed in **Similar Closed HR Cases** in the Related Search Results section. If there are three or more similar closed HR cases whose COE matches that of the current case, then the case with the highest confidence is displayed as a recommended HR case.
-   If there is no recommended HR Case, then the knowledge article that is attached to more than three similar closed cases is displayed as a recommended article. The recommended article can be attached to the current HR case.

## Auto training the predictive model

The Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Workspace \(com.sn\_hr\_agent\_workspace\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

**Parent Topic:**[Machine learning solutions for HR Service Delivery Agent Workspace](agent-ws-hr-prediction-service.md)

