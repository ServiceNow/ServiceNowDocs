---
title: Estimated time to resolve HR cases
description: Determine the Estimated Time to Resolve a Case \(ETTR\) for a case by analyzing similar closed cases in the past for better visibility and transparency.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Recommend estimated time to resolve, Implement, HR Predictive Intelligence Workbench, Integrate with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Estimated time to resolve HR cases

Determine the Estimated Time to Resolve a Case \(ETTR\) for a case by analyzing similar closed cases in the past for better visibility and transparency.

Machine learning predicts the estimated time to resolve a case \(ETTR\) based on attributes of a case such as its short description, category, priority, assignment group, and so on. For more information about configuring the machine learning regression solution definition for ETTR, see [HR PIWB template: Recommend estimated time to resolve](../task/hr-piwb-ettr.md)

To make predictions, you can use the existing ETTR solution definition or change some of the default settings such as the fields, a filter, and the training frequency.

By analyzing the resolution time for similar closed cases in the past, the ETTR capability offers the following benefits:

-   Gives employees better transparency and set expectations on resolution time for their cases.
-   Helps agents in prioritization of work and measure performance.
-   Provides data that can help managers with insights into SLA management and estimated time to resolve for cases.

## ETTR for HR Cases

On configuring Estimated HR Case Resolution Time \(ml\_sn\_sn\_hr\_core\_global\_hr\_case\_resolution\_time\) and training the predictive model, you can see the **HR Case Resolution Time** option. See the **Estimated time to resolve** value from:

-   Employee portal view and Now Mobile view
-   Agent workspace
-   Platform view with a list of cases
-   Case configuration view for admins

For more information, see [Viewing ETTR predictions](create-regression-solution-hr.md)

## ETTR predictive model

The Estimated HR Case Resolution Time \(ml\_sn\_sn\_hr\_core\_global\_hr\_case\_resolution\_time\) is configured and the predictive model is auto trained when all the following conditions are met:

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence for Contextual Search \(com.snc.contextual\_search\_ml\) plugin is installed.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

Business rules and system properties

Verify the following system properties and business rules:

-   Use or configure the following system properties and corresponding values to display the ETTR values per your requirement:
    -   **ml\_sn\_sn\_hr\_core.COE\_ETTR\_display\_agent**
    -   **ml\_sn\_sn\_hr\_core.COE\_ETTR\_display\_employee**
    -   **ml\_sn\_sn\_hr\_core.estimated\_resolution\_time\_confidence\_level**
-   Use or configure the **Predict Estimated Resolution Time** business rule per your business needs.

## ETTR model

Regression solutions such as ETTR enable you to predict a point estimate and prediction interval. This capability informs the agent, employee, and service owners on the estimated resolution time for a case based on the time taken to resolve similar issues historically.

-   **Actual resolution time**: Stores the actual time of resolution of a particular case. This field stores the resolution time from opening to closing of the case.

    **Note:** When you upgrade, run this **Populate Actual Resolution Time** schedule job once for populating the actual resolution time for existing HR cases. For all upcoming cases, the business rule **Populate Actual Resolution Time** automatically generates the resolution time.

-   **Max ETTR**: Indicates the maximum estimated resolution time in days for case completion. Estimate is based on the time taken for resolving similar HR cases.
-   **Min ETTR**: Indicates the minimum estimated resolution time in days for case completion. Estimate is based on the time taken for resolving similar HR cases.
-   **ETTR in days**: Stores the point estimated resolution time in days for case completion.

**Parent Topic:**[HR PIWB template: Recommend estimated time to resolve](../task/hr-piwb-ettr.md)

**Related topics**  


[Viewing ETTR predictions](create-regression-solution-hr.md)

