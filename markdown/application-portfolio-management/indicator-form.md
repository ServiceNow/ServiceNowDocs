---
title: Indicator form
description: Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Indicator form

Application indicators are business metrics that assess the applications across dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value.

**Important:**

Starting with the Xanadu release, the application indicators module is moved to the Enterprise Architecture Workspace. To learn more, see [Configure indicators](../concept/eaw-concept/eaw-configure-indicators.md). To view the updated indicator form fields, see [Create new indicator form](eaw-reference/eaw-create-new-indicator-form.md).

Role required: sn\_apm.apm\_admin

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

Unit

</td><td>

A number, currency, time, duration in minutes, hours, days, month, or quarter, or rate.

 You can also create units according to your requirements.

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

Direction

</td><td>

Business application with maximum or minimum values. Select Minimize if lower values are better. Select Maximize if higher values are better.

</td></tr><tr><td>

Target minimum

</td><td>

Minimum value for the indicator.The **Target minimum** field isn’t available when **Assessments** is selected from the **Data source** list.

</td></tr><tr><td>

Consider Absolute Values

</td><td>

Option to consider values from the **Target maximum** and **Target minimum** fields. This field is available only when values are entered in the **Target maximum** and **Target minimum** fields.

 When the check box is cleared, values for target maximum and target minimum are considered based on the [intelligent logic](../concept/application-score-profile.md).

</td></tr><tr><td>

Short description

</td><td>

Short summary of the application indicator.

</td></tr></tbody>
</table><table id="table_l5n_1my_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default breakdown

</td><td>

Name of the Performance Analytics breakdown.

</td></tr><tr><td>

Data source

</td><td>

Defines the location from which the indicator receives data.

 -   **Performance Analytics**: Collects scores from indicators created in Performance Analytics. See [Performance Analytics indicators](https://www.servicenow.com/docs/access?context=c_Indicators&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).
-   **Custom Script**: Allows you to write a script that collects data from another application.
-   **Query Condition**: Allows you to select a table to run filters on to obtain data.
-   **Assessments**: Allows you to evaluate, score, and rank records by assessing records in a table. See [Create metric types and generate assessable records](https://www.servicenow.com/docs/access?context=t_CreatMetricTypesAndGenAssessRecs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). To view results of survey assessments within APM, see [Generate survey assessments and view results within APM](../task/generate-survey-assessments-results-apm.md).
-   **Indicators**: Allows you to add dependent child indicators. Through the child indicators, data is gathered to the parent indicator.

For example, if the parent indicator is number of issues, the dependent indicators can be number of incident counts, number of problems, and changes. These dependent indicators are child indicators and the number of incidents, problems, and changes recorded are consolidated up to the parent indicator as the number of issues.


</td></tr><tr><td>

Indicator

</td><td>

The **Indicator** field appears when **Performance Analytics** is selected from the **Data source** list.Indicators are statistics that are used to measure current conditions and forecast trends.

 **Note:** If the collection frequency of the application indicator isn’t greater than the frequency at which the data of the Performance Analytic indicator is generated, then the system displays an error message: `Frequency of the indicator must always be greater than or equal to the frequency of the datasource configuration indicator`. For more information, see [Collection of PA indicator score data](../concept/pa-indicators-jobs.md#CollectionPAIndicators).

</td></tr><tr><td>

Consolidation

</td><td>

Computational method for aggregating the values, a function such as sum, average, maximum, or minimum.Default is Average. For example, Average is the sum of the monthly values divided by the total number of months in a quarter.

 If you select Maximum or Minimum, then it’s the maximum value or the minimum value of a month in the quarter, respectively.

 If you select Sum, then it’s an aggregate of all monthly values in the quarter.

</td></tr><tr><td>

Custom script

</td><td>

The **Custom Script** field appears when **Custom Script** is selected from the **Data source** list.An example custom script is:

```
var results = {};
 var applications = [];
 var incidentCount = 0;
 
 var applicationsGr = new GlideRecord("cmdb_ci_business_app");
 applicationsGr.addQuery('active', true);
 applicationsGr.query();
 //for each application get incident count at business service level
 while(applicationsGr.next()) {
    incidentCount = 0;
    
    var gr = new GlideRecord("incident");
    gr.addEncodedQuery("opened_atBETWEEN"  + startDate  + "@" +   endDate);
    gr.addQuery('cmdb_ci_business_app', applicationsGr.getUniqueValue());   
    gr.query();
    
    incidentCount = gr.getRowCount();
    var appInfo = {};
    appInfo.appId = applicationsGr.getUniqueValue();
    appInfo.weight = incidentCount;
    applications.push(appInfo);
    }
 results.applications = applications;
 results;

```

</td></tr><tr><td>

Assessment Metric Type

</td><td>

Type of metric that is used to assess the indicator.**Assessment Metric Type** field appears when the **Data source** is **Assessments**.

</td></tr><tr><td>

Assessment Metric Category

</td><td>

Category of the metric.

</td></tr><tr><td>

Query table

</td><td>

Table from which the queries are filtered.

</td></tr><tr><td>

Query conditions

</td><td>

The conditions based on which the query is filtered.

</td></tr><tr><td>

Aggregate field

</td><td>

The field from the selected table is displayed for the records that match the query conditions.

</td></tr><tr><td>

Aggregate type

</td><td>

Type of aggregation applied for calculation of indicator scores.The available options are:

-   **Sum**
-   **Count**
-   **Avg**
-   **Min**
-   **Max**

</td></tr><tr><td>

Group by

</td><td>

Categorize the data returned by the query, based on values of a specific field in the query table. For example, if you want to group the data by the life cycle stage status of applications, select Life Cycle Stage.

</td></tr><tr><td>

Consolidation field

</td><td>

The field from the query table on which the computational method for aggregating the values is applied.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Create or edit an indicator to assess an application](../task/create-application-indicators.md)

