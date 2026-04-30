---
title: ITSM Predictive Intelligence Workbench dashboard
description: ITSM Predictive Intelligence Workbench provides the Predictive Intelligence for Incidents dashboard to enable you to measure the value of using machine learning to automate your IT business processes. Monitor use case models and view associated statistics. Effectively demonstrate business value to stakeholders with dashboard views.
locale: en-US
release: xanadu
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [ITSM Predictive Intelligence Workbench, IT Service Management]
---

# ITSM Predictive Intelligence Workbench dashboard

ITSM Predictive Intelligence Workbench provides the Predictive Intelligence for Incidents dashboard to enable you to measure the value of using machine learning to automate your IT business processes. Monitor use case models and view associated statistics. Effectively demonstrate business value to stakeholders with dashboard views.

**Important:**

Starting with the Xanadu release, ITSM Predictive Intelligence Workbench is being prepared for future deprecation. It will be completed deprecated and will no longer be supported from the **Yokohama** release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../../product/task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Know exactly what stage your model workflows are in with automated comments on specific ServiceNow® Performance Analytics indicators. Comments appear on the **Actual Net Automation** indicators. Model stages comments include, when the model is integrated, when an integration is removed, when an existing model is changed to a new model, and when retraining is complete.

![Predictive Intelligence for Incidents dashboard Business Value tab](../../../product/itsm-predictive-intel-workbench/image/PIWBBusinessValue-part1.png "Business Value tab")

![Predictive Intelligence for Incidents dashboard Monitoring Models tab](../../../product/itsm-predictive-intel-workbench/image/PIWBMonitoringModels-pt1.png "Monitoring Models tab")

You can view the Net Automation Threshold graph on the **Monitoring Models** tab. This threshold is a computation of the difference between estimated net automation and the underperformance property values. Thresholds are calculated daily and notifications are sent to stakeholders when thresholds are breached.

View automatic comments on the **Actual Net Automation** indicator at various stages of the model monitoring. A comment is generated when any of the following model criteria exists:

-   Model is integrated
-   Model integration is removed
-   Existing model is changed to a new model
-   Integrated model is retrained

![Predictive Intelligence for Incidents dashboard Model Statistics tab](../../../product/itsm-predictive-intel-workbench/image/PIWBModelStatistics.png "Model Statistics tab")

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Process architect, process owner, or machine learning advocate: Visualize operational and automation metric performance​.

 Communicate machine learning value to stakeholders to increase the automation capabilities of predictive intelligence.

</td><td>

Predictive Intelligence Workbench manager or viewer\[piwb\_manager\]

 \[piwb\_viewer\]

</td><td>

Ability to measure the value of using **Predictive Intelligence** to automate ITSM processes.

</td></tr></tbody>
</table>## Indicators

-   **Prediction Coverage for Incident**

    The score for this indicator is calculated according to the formula: `if ([[Number of attempted predictions based on Created Today for Incident]]==0){0}else{[[Number of applied predictions based on Created Today for Incident]]/[[Number of attempted predictions based on Created Today for Incident]]*100}`.

-   **Number of predicted results based on final value date for incident**

    The number of predicted results is based on the final value date for an incident. The score is measured daily as unit \#.

-   **Net Automation for Incident**

    The score for this indicator is calculated according to the formula: `[[Prediction Precision for Incident]]*[[Prediction Coverage for Incident]]/100`.

-   **Number of applied predictions based on Created Today for Incident**

    Number of applied predictions based on Created Today for Incident is measured daily as unit \#.

-   **Number of attempted predictions based on Created Today for Incident**

    Number of attempted predictions based on Created Today for Incident is measured daily as unit \#.

    The goal for this indicator is to maximize the quality of predictions.

-   **Prediction Precision for Incident**

    The score for this indicator is calculated according to the formula: `if ([[Number of predicted results based on final value date for Incident]]==0){0}else{[[Number of successful predictions not skipped based on final value date for Incident]]/[[Number of predicted results based on final value date for Incident]]*100}`.

-   **Estimated Net Automation**

    Estimated net automation measured daily as unit %.

-   **Number of successful predictions not skipped based on final value date for Incident**

    Number of successful predictions not skipped based on final value date is measured daily as unit \#. It is the count on data source MLPredictorResults.FinalValueDate.Incident, which is using the table: ml\_predictor\_results.

-   **Number of Predicted for Incidents**

    Number of Predicted for Incidents is measured daily as unit \#. It is the count on data source MLPredictorResults.CreatedToday.Incident, which is using the table: ml\_predictor\_results.


## Breakdowns

Use Case.

## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predictions Skipped

</td><td>

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

% Estimated Precision. Estimated precision measured as unit %, based off the data the model was trained on.

</td></tr><tr><td>

Predictions Skipped

</td><td>

Line![Line icon](../../../reuse/reporting/image/line-trend.svg)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Predictions Skipped \(num\). Number of \_\_\_, due to low confidence.

</td></tr><tr><td>

Class Distribution - Training Data

</td><td>

Bar![Bar icon](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_classes

</td><td>

Predictions Skipped \(line\).

</td></tr><tr><td>

% Estimated Precision

</td><td>

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_solutions

</td><td>

Predicted Correctly \(num\). Number of \_\_\_, comparing initial predicted value to final record value.

</td></tr><tr><td>

Classes Excluded due to Low Distribution

</td><td>

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_excluded\_classes

</td><td>

Predicted Correctly \(line\).

</td></tr><tr><td>

Class Distribution - Actual

</td><td>

Bar![Bar icon](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Predicted Incorrectly \(num\).Number of \_\_\_, comparing initial predicted value to final record value.

</td></tr><tr><td>

Predicted Correctly

</td><td>

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Predicted Incorrectly \(line\).

</td></tr><tr><td>

Predicted Correctly

</td><td>

Line![Line icon](../../../reuse/reporting/image/line-trend.svg)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Class Distribution, Training Data.Distribution of classes in data that the solution was trained on.

</td></tr><tr><td>

Predicted Incorrectly

</td><td>

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Class Distribution, Actual. Current distribution of classes in live data.

</td></tr><tr><td>

Predicted Incorrectly

</td><td>

Line![Line icon](../../../reuse/reporting/image/line-trend.svg)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_predictor\_results

</td><td>

Predicted Classes. Number of values the model can return as a prediction.

</td></tr><tr><td>

Prediction Classes

</td><td class="icon">

Single Score![Single score icon](../../performance-analytics/image/single-score.png)

</td><td>

sn\_piwb\_itsm\_conte\_dbv\_ml\_classes

</td><td>

Classes Excluded due. Number of values the model was not confident enough to return as a prediction, due to not enough data.

</td></tr></tbody>
</table>**Note:** Regarding source tables, all indicators and reports are built off of newly added database views, combining ServiceNow platform Predictive Intelligence tables with Predictive Intelligence Workbench use case tables. With these new views, you can filter platform data by use case to better understand its impact on your metrics. All database views for this content application have a prefix of sn\_piwb\_itsm\_conte\_dbv.

