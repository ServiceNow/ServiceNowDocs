---
title: Data types for assessments
description: Metric data types have functions that depend on the method that you select.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Data types for assessments

Metric data types have functions that depend on the method that you select.

<table id="table_jkh_gtr_z4"><thead><tr><th>

Data type

</th><th>

Compatible methods

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

Assessment

</td><td>

On questionnaires, users attach one or more files to a question.

</td></tr><tr><td>

Checkbox

</td><td>

Assessment

</td><td>

On questionnaires, users select a check box next to a statement or leave it cleared.

![Check box](../../survey-administration/image/CheckboxDataType.png "Check box")

 Set the **Scale definition** field to **High** if a selected check box equates to a good score.

</td></tr><tr><td>

Choice

</td><td>

Assessment

</td><td>

On questionnaires, users select a value from a list of custom answer options. Create a metric definition for each answer option.![Choice](../images/ChoiceDataType.png "Choice")

</td></tr><tr><td>

Date

</td><td>

Assessment

</td><td>

On questionnaires, users select a date.![Date](../images/DateDataType.png "Date")

</td></tr><tr><td>

Date/Time

</td><td>

Assessment

</td><td>

On questionnaires, users select a date and time.![Date/Time](../images/DateTimeDataType.png "Date/Time")

</td></tr><tr><td>

Duration

</td><td>

Script

</td><td>

When the script runs, the system populates the **Duration value** and **Scaled value** fields on the Metric Result form with the appropriate values from the *actual\_result* and *scaled\_result* variables in the metric script.

</td></tr><tr><td>

Likert Scale

</td><td>

Assessment

</td><td>

On questionnaires, users select a value from a custom scale of answer options. Create a metric definition for each answer option, which is represented by a radio button on the scale. A Likert scale metric that evaluates an application's ease of use might have the metric definitions **Easy**, **Average**, and **Difficult**.If you want to reuse a series of answer options for multiple metrics, create a metric template and use the Template data type instead of the Likert Scale data type.

![Likert Scale](../images/LikertScaleDataType.png "Likert Scale")

</td></tr><tr><td>

Number

</td><td>

Assessment, Script

</td><td>

**Assessment**: On questionnaires, users enter a number. ![Number](../images/NumberAssessmentDataType.png "Number")

 **Script**: When the script runs, the system populates the **Actual value** and **Scaled value** fields on the [Metric Result](../task/t_ViewAMetricResult.md) form with the appropriate values from the *actual\_result* and *scaled\_result* variables in the metric script.

</td></tr><tr><td>

Percentage

</td><td>

Assessment, Script

</td><td>

**Assessment** On questionnaires, users enter a number.

![Percentage](../images/PercentageAssessmentDataType.png "Percentage")

 **Script** When the script runs, the system populates the **Actual value** and **Scaled value** fields on the Metric Result form with the appropriate values from the *actual\_result* and *scaled\_result* variables in the metric script.

</td></tr><tr><td>

String

</td><td>

Assessment

</td><td>

On questionnaires, users enter text. The size of the string field depends on the String option you select:

![String](../../survey-administration/image/StringSingleLineDataType.png "String")

 ![String single line wide data type](../../survey-administration/image/StringSingleLineWideDataType.png "String single line wide data type")

 ![Additional comments](../../survey-administration/image/StringMultilineDataType.png "Additional comments")

</td></tr><tr><td>

Template

</td><td>

Assessment

</td><td>

On questionnaires, users select a value from a predefined series of answer options. There must be at least one template defined to use this data type. For a template, there is a template definition for each answer option, which is represented by a radio button.

</td></tr><tr><td>

Yes/No

</td><td>

Assessment

</td><td>

On questionnaires, users select **Yes** or **No** from a list.

 ![Yes/No](../images/YesNoDataType.png "Yes/No")

 Set the **Scale definition** field to **High** if selecting **Yes** equates to a better score.

</td></tr></tbody>
</table>**Parent Topic:**[Assessments reference](assessment-reference.md)

**Related topics**  


[Assessment metrics](../concept/c_AssessmentMetrics.md)

[Create an assessment metric definition](../task/t_CreateAMetricDefinition.md)

[Update a metric minimum and maximum value to match a template](../task/t_UpdAMetrMinMaxValToMatchATmplate.md)

