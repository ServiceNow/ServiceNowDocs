---
title: New Indicator form
description: Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# New Indicator form

Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.

## Indicator form fields

<table id="table_dnp_c5h_by"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application indicator.

</td></tr><tr><td>

Category

</td><td>

 

</td></tr><tr><td>

Short description

</td><td>

Short summary of the application indicator.

</td></tr><tr><td>

Direction

</td><td>

Business application with maximum or minimum values. Select Minimize if lower values are better. Select Maximize if higher values are better.

</td></tr><tr><td>

Result limit

</td><td>

The maximum number of records an indicator displays when running an associated script. This enables better performance of the Enterprise Architecture by not processing too many records.

</td></tr><tr><td>

Result Precision

</td><td>

Define how many decimal places are displayed for the indicator's calculated value in the scorecards and dashboards. For example, a result precision value of 0 means that the value is rounded to the nearest whole number.

</td></tr><tr><td>

Unit

</td><td>

A number, currency, time, duration in minutes, hours, days, month, or quarter, or rate.

 You can also create units as per your requirements.

</td></tr><tr><td>

Automatic refresh interval

</td><td>

The refresh interval to update the indicator scores within the defined time range.

</td></tr><tr><td>

Order

</td><td>

The position of the indicator in the sequential order of all other indicators while accessing an application or capability.

</td></tr><tr><td>

Frequency

</td><td>

Frequency determines the interval at which the data for the indicator source should be collected.The **Frequency** field isn’t available when **Performance Analytics** is selected from the **Data source** list.

</td></tr><tr><td>

Target maximum

</td><td>

Maximum value for the indicator. The **Target maximum** field isn’t available when **Assessments** is selected from the **Data source** list.

</td></tr><tr><td>

Active

</td><td>

Select the **Active** option to enable the indicator.

</td></tr><tr><td>

CI Class

</td><td>

CI type for which the score is generated.

</td></tr><tr><td>

Target minimum

</td><td>

Minimum value for the indicator.The **Target minimum** field isn’t available when **Assessments** is selected from the **Data source** list.

</td></tr><tr><td>

Consider Absolute Values

</td><td>

Option to consider values from the **Target maximum** and **Target minimum** fields. This field is available only when values are entered in the **Target maximum** and **Target minimum** fields.

 When the check box is cleared, values for target maximum and target minimum are considered based on the [intelligent logic](../../concept/application-score-profile.md).

</td></tr></tbody>
</table><table id="table_xmb_fst_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Defines the location from which the indicator receives data.

 -   **Performance Analytics**: Collects scores from indicators created in Performance Analytics. See [Performance Analytics indicators](https://www.servicenow.com/docs/access?context=c_Indicators&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).
-   **Custom Script**: Allows you to write a script that collects data from another application. Beneath the **Data Source** field, a sample script appears. Customize the script as needed.
-   **Query Condition**: Allows you to select a table to run filters on to obtain data.
-   **Assessments**: Allows you to evaluate, score, and rank records by assessing records in a table. See [Create metric types and generate assessable records](https://www.servicenow.com/docs/access?context=t_CreatMetricTypesAndGenAssessRecs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). To view results of survey assessments within Enterprise Architecture, see [Generate survey assessments and view results within APM](../../task/generate-survey-assessments-results-apm.md).
-   **Indicators**: Allows you to add dependent child indicators. Through the child indicators, data is gathered to the parent indicator.

For example, if the parent indicator is number of issues, the dependent indicators can be number of incident counts, number of problems, and changes. These dependent indicators are child indicators and the number of incidents, problems, and changes recorded are consolidated up to the parent indicator as the number of issues.


</td></tr><tr><td>

Indicator

</td><td>

The **Indicator** field appears when **Performance Analytics** is selected from the **Data source** list.Indicators are statistics that are used to measure current conditions and forecast trends.

 **Note:** If the collection frequency of the application indicator is not greater than the frequency at which the data of the Performance Analytic indicator are generated, then the system displays an error message: `Frequency of the indicator must always be greater than or equal to the frequency of the datasource configuration indicator`. For more information, see [Collection of PA indicator score data](../../concept/pa-indicators-jobs.md#CollectionPAIndicators).

</td></tr><tr><td>

Default breakdown

</td><td>

Name of the Performance Analytics breakdown.

</td></tr><tr><td>

Normalization script

</td><td>

A script to evaluate and score business applications and capabilities using standardized metrics. It involves using indicators that provide a normalized score for the condition they are evaluating. These indicators can be based on assessments, query conditions, custom scripts, or performance analytics.

</td></tr><tr><td>

Consolidation

</td><td>

Computational method for aggregating the values, a function such as sum, average, maximum, or minimum.Default is Average. For example, Average is the sum of the monthly values divided by the total number of months in a quarter.

 If you select Maximum or Minimum, then it’s the maximum value or the minimum value of a month in the quarter, respectively.

 If you select Sum, then it’s an aggregate of all monthly values in the quarter.

</td></tr><tr><td>

Assessment Metric Type

</td><td>

Type of metric that is used to assess the indicator.**Assessment Metric Type** field appears when the **Data source** is **Assessments**.

</td></tr><tr><td>

Assessment Metric Category

</td><td>

Category of the metric.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Click through URL navigation type|Select whether to view the application or capability indicator details in a new window, in the same window, or in a dialog box.|
|Click through URL script|The script associated with an indicator that allows users to select a URL and view the indicator data in a related application or dashboard. This enables quick access to relevant information, or actions related to the indicator data.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md)

