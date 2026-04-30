---
title: Metric Result form
description: Description of the field values for the Metric Result form.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Metric Result form

Description of the field values for the Metric Result form.

<table id="table_jdq_n5r_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment group

</td><td>

Assessment group to which the metric result belongs. An assessment group is a container for survey instances and results generated in a single occurrence. The system generates an assessment group every time at least one survey instance is created. If multiple survey instances are created at once, such as when a survey administrator sends invitations to a list of survey users, they are all stored in the same assessment group.

</td></tr><tr><td>

Metric

</td><td>

Question that the user answered.

</td></tr><tr><td>

Data type

</td><td>

Data type of the question the user answered.

</td></tr><tr><td>

Method

</td><td>

Assessment method. Always **Assessment** for surveys.

</td></tr><tr><td>

Updated

</td><td>

Date and time the metric result was last updated.

</td></tr><tr><td>

Source

</td><td>

Survey definition from which the associated survey instance was generated.

</td></tr><tr><td>

Assigned to

</td><td>

User who completed the survey questionnaire.

</td></tr><tr><td>

Instance

</td><td>

Survey instance completed by the **Assigned to** user.

</td></tr><tr><td>

Actual value

</td><td>

Value obtained from the user response to the question. The actual value is determined by the question data type:

 -   **Checkbox:** The actual value is 0 if the check box is cleared and 1 if it is selected.
-   **Choice** or **Likert Scale:** The actual value is equal to the **Value** of the metric definition associated with the chosen answer option.
-   **Date**, **Date/Time**, or **String:** The actual value is -1 to indicate that these data types do not contribute to category result calculations.
-   **Template:** The actual value is equal to the **Value** of the template definition associated with the chosen answer option.
-   **Yes/No:** The actual value is 0 if the response is **No** and 1 if it is **Yes**.

</td></tr><tr><td>

Normalized value

</td><td>

Adjusted value that accounts for the **Scale definition** setting, minimum and maximum values, and other factors. The equation that generates the value and an example calculation appear in [Normalized value for an assessment](../../orchestration-activity-designer/reference/example-normalized-value-calc.md).

</td></tr><tr><td>

String value

</td><td>

Value that displays the response as it appears on a questionnaire. In some cases this is the same as the **Actual value**, such as when the question data type is **Percentage**. The string value is `N/A` for unanswered questions of certain data types.

</td></tr></tbody>
</table>-   **[Normalized value for an assessment](../../orchestration-activity-designer/reference/example-normalized-value-calc.md)**  
The normalized value is calculated based on a linear equation and the scale definition of the metric. This value can be used for risk assessment.

**Parent Topic:**[Surveys reference](survey-reference.md)

