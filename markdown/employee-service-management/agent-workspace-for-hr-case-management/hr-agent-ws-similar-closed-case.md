---
title: Display similar closed cases in Agent Workspace for HR Case Management
description: Help an HR agent resolve the current case by displaying similar closed cases.
locale: en-US
release: yokohama
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions in Agent Workspace for HR Case Management, Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Display similar closed cases in Agent Workspace for HR Case Management

Help an HR agent resolve the current case by displaying similar closed cases.

**Important:** This feature is available with the HR Professional and HR Enterprise packages when you activate Agent Workspace for HR Case Management and Predictive Intelligence applications.

## Similar Closed HR Cases

When the Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is trained:

-   Similar closed cases are displayed in **Similar Closed HR Cases** in the Related Search Results section. If there are three or more similar closed HR cases whose COE matches that of the current case, then the case with the highest confidence is displayed as a recommended HR case.
-   If there is no recommended HR Case, then the knowledge article that is attached to more than three similar closed cases is displayed as a recommended article. The recommended article can be attached to the current HR case.

## Auto training the predictive model

The Similar Closed HR Cases \(ml\_sn\_sn\_hr\_core\_global\_similar\_closed\_hr\_cases\) is configured and the predictive model is auto trained when all the following conditions are met:

-   The Agent Workspace for HR Case Management plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   The **glide.platform\_ml.auto\_training.enabled** system property is either set to true or absent.

**Parent Topic:**[Machine learning solutions in Agent Workspace for HR Case Management](hr-agent-ws-ml-solutions.md)

**Related topics**  


[Auto determination of HR service in Agent Workspace for HR Case Management](hr-agent-ws-auto-hrservice.md)

[Auto determination of assignment group in Agent Workspace for HR Case Management](hr-agent-ws-auto-assign-grp.md)

