---
title: View a metric result
description: Metric results contain values that represent an evaluated record's performance for a specific metric, based on a single evaluation from one user or from the execution of a script. Metric results contain actual values as well as calculated values. The system uses values from metric results to calculate category results.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a metric result

Metric results contain values that represent an evaluated record's performance for a specific metric, based on a single evaluation from one user or from the execution of a script. Metric results contain actual values as well as calculated values. The system uses values from metric results to calculate category results.

## Before you begin

Role required: assessment\_admin or admin

## About this task

If there is an active scripted metric when the assessment is generated, the system automatically produces a metric result for each associated assessable record. The system produces an additional metric result for each question a user answers on a completed assessment questionnaire. If multiple users complete questionnaires with the same questions on the same assessable records, the system produces metric results for each user's responses. For example, three users complete questionnaires that contain the same four questions about the Acme Corporation record. The system produces 12 metric results: one per user for each question.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Results** &gt; **Metric Results**.

2.  Open the metric result record you want to view.

    All fields on the form except **Updated** and **String value** are read-only.

<table id="table_odb_vcj_w4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment group

</td><td>

[Assessment group](../concept/c_AssessmentGroups.md) to which the metric result is associated.

</td></tr><tr><td>

Metric

</td><td>

Name of the metric to which these metric result values apply.

</td></tr><tr><td>

Data type

</td><td>

Data type of the metric.

</td></tr><tr><td>

Method

</td><td>

[method](../concept/c_AssessmentMetrics.md) of the metric.

</td></tr><tr><td>

Updated

</td><td>

Date and time the metric result was last updated.

</td></tr><tr><td>

Source

</td><td>

Source record of the assessable record evaluated.

</td></tr><tr><td>

Assigned to

</td><td>

User who completed the assessment questionnaire. This field is blank when the method is **Script**.

</td></tr><tr><td>

Instance

</td><td>

[Assessment instance](../concept/c_AssessmentInstances.md) completed by the **Assigned to** user. This field is blank when the method is **Script**.

</td></tr><tr><td>

Actual value

</td><td>

Unscaled value from a user response or script, depending on the method:

-   **Assessment**: Value obtained from the user response to the assessment instance question. The actual value is determined by the metric data type:
    -   **Checkbox**: The actual value is 0 if the check box is cleared and 1 if it is selected.
    -   **Choice** or **Likert Scale**: The actual value is equal to the Value of the metric definition associated with the chosen answer option.
    -   **Date**, **Date/Time,** or **String**: The actual value is -1 to indicate that these data types do not contribute to category result calculations.
    -   **Template**: The actual value is equal to the **Value** of the [template definition](../reference/r_MetricTemplates.md) associated with the chosen answer option.
    -   **Yes/No**: The actual value is 0 if the response is **No** and 1 if it is **Yes**.
-   **Script**: Value the script placed in the *actual\_result* variable.
 This field is hidden and left blank when the data type is **Duration**.

</td></tr><tr><td>

Duration value

</td><td>

Specific kind of actual value that is only applicable if the data type is **Duration**. The duration value is the value obtained by the script query from the **actual\_result** parameter, such as the average duration of outages for a vendor.

</td></tr><tr><td>

Scaled value

</td><td>

Appropriate value from the *scaled\_result* variable in the associated metric script. The code in a scripted metric defines a scaling scheme for the actual values it obtains. For example, a scripted metric queries the CMDB to return the number of configuration items \(CIs\) for a vendor. The code includes this scaling scheme, where**actual\_result** is the number of CIs, and **scaled\_result** is a representation of the quantity of CIs:

 ```
if (actual_result < 1)
	scaled_result = 0;
else if (actual_result < 1000)
	scaled_result = 1;
else if (actual_result < 10000)
	scaled_result = 2;
else if (actual_result < 25000)
	scaled_result = 3;
else if (actual_result < 100000)
	scaled_result = 4;
else
	scaled_result = 5;
```

 If the script detects 315 CIs for the vendor, the **Actual value** is 315 and the **Scaled value** is 1 for this metric result.

 **Note:** Although this field is visible only when the method is **Script**, the system populates the field with the **Actual value** when the method is **Assessment**, as the scaled value is used in the **Normalized value** calculation.

</td></tr><tr><td>

Normalized value

</td><td>

Adjusted value that accounts for weights, scale definition, minimum and maximum values, and other factors that impact the metric \(like the survey responses or the input value—the actual value given by the user\). See the example for **Normalized value** in [View an assessment category result](t_ViewACategoryResult.md).

</td></tr><tr><td>

String value

</td><td>

Value that displays the response as it appears on a questionnaire. In some cases this is the same as the **Actual value**, such as when the metric data type is **Percentage**. The string value is **N/A** for unanswered questions of certain data types. For the **Attachment** data type, the names of the attached files are displayed as comma-separated values.

</td></tr></tbody>
</table>
-   **[Assessment results](../reference/r_AssessmentResults.md)**  
In the Assessments application, when the system processes completed questionnaires or gathers values returned from scripted metric queries, it generates assessment result records called metric and category results.
-   **[Assessment Overview dashboard](../reference/r_AssessmentsOverviewModule.md)**  
The Assessment Overview dashboard displays various assessment reports, such as Assessable Records by Type, Total Metrics by Metric Type, and Assessments by State.
-   **[View assessment reports](view-assessment-report.md)**  
Use the Assessment Overview dashboard to view your assessment reports.
-   **[Assessment results calculation](../concept/c_AssessmentResultsCalculation.md)**  
For every assessment group, there are assessment results.
-   **[View a bubble chart for assessments](../../service-administration/task/t_view-bubble-chart-assessments.md)**  
Assessment administrators can view bubble charts to compare the relative standing of assessable records in three metric categories.

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)

