---
title: Assessment Metric form for a category
description: Description of the field values for the Assessment Metric form. Use the fields when you create an assessment metric for a category.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Assessments reference, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment Metric form for a category

Description of the field values for the Assessment Metric form. Use the fields when you create an assessment metric for a category.

<table id="table_v2j_rgr_z4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the metric.

</td></tr><tr><td>

Category

</td><td>

Metric category that the metric belongs to. The system automatically populates this category if you create a new metric from the Metric Category form. **Note:** You cannot change the category if the **Depends on** field is set or if another metric depends on this metric

</td></tr><tr><td>

Method

</td><td>

Determines how to use the metric.

-   **Assessment** : Non-scripted metric. Make the metric available as a question on an assessment questionnaire. The **Assessment** method is compatible with all data types except **Duration**.
-   **Script**: Scripted metric. Obtain values by writing a custom script. The **Script** method is compatible with the **Duration**, **Number**, and **Percentage** data types.
-   **Default answer from field**: This option appears only if you have selected an **Assessment Metric Type** that contains a table. The **General** tab adds two fields:
    -   **Default answer**: Select the default answer for the question. The list comes from the selected table.
    -   **Ask question**: Specifies when to ask the question: always or only if the default answer is empty.
-   **Default answer from script**: The **General** tab adds a field:

**Ask question**: Specifies when to ask the question: always or only if the script does not contain a default answer. The script is defined on the **Field Type** tab.


 **Note:** If you select a **Data type** that is incompatible with the selected **Method**, the system automatically changes the **Method** to the correct value.

</td></tr><tr><td>

Weight

</td><td>

Numeric value that represents the importance of this metric relative to other metrics in the same category. By default, the weight is 10. For weighting suggestions, see [Weight Metrics and Metric Categories](../concept/c_AssessmentMetrics.md).

 This field is visible and required unless the **Data type** is **Date**, **Date/Time**, or **String**. These data types are not included in results calculations.

</td></tr><tr><td>

Order

</td><td>

Numeric value that determines the order of the metric question on assessment questionnaires, relative to other metric questions in the same category. The metric with the smallest order value appears as the first question in the category section. By default, the order is 100. For more information about questionnaire layout, see [Complete Assessment Questionnaires](../concept/c_AssessmentQuestionnaires.md). **Note:** It does not matter which order value you use for metrics with the Script method, as they do not appear on questionnaires.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this metric is used to gather assessment results. If a non-scripted metric \(Assessment method\) is inactive, the question does not appear on assessment questionnaires generated after the metric becomes inactive. If a scripted metric \(Script method\) is inactive, the script does not run.

</td></tr><tr><td>

Mandatory

</td><td>

Check box that makes the metric question mandatory \(selected\) or optional \(cleared\) on assessment questionnaires. Users cannot submit questionnaires until they provide valid responses to all mandatory questions, which display a red [field status indicator](../concept/c_AssessmentQuestionnaires.md).

 This field is visible only if the **Method** is **Assessment**, the **Depends on** field is empty, and the data type is not **Checkbox**.

</td></tr><tr><td>

Allow not applicable

</td><td>

Check box that determines whether to include a **Not Applicable** answer option for this metric question on assessment questionnaires. Users can select **Not Applicable** if they do not have sufficient information to respond to a question or if a question does not apply to a particular assessable record. User responses of **Not Applicable** are excluded from results calculations.

 This field is visible only if the **Method** is **Assessment** and certain data types are selected.![Assessments not applicable option](../images/AssessmentNotApplicableOption.png)

</td></tr><tr><td class="sub-head" colspan="2">

Additional fields you can add by customizing the form

</td></tr><tr><td>

Details

</td><td>

Text field containing an HTML editor. Use this field to present important details about this metric to assessment recipients. Details can include formatted lists, images, videos, or links to external websites. ![Assessment metric details](../images/AssessmentMetricDetails.png)

</td></tr><tr><td class="sub-head" colspan="2">

General Section

</td></tr><tr><td>

Question

</td><td>

Text to use as the question on assessment questionnaires. Enter a clear, straightforward question that is easy to answer, such as **How likely are you to recommend this vendor for the purchase of office supplies?** ![Assessment question field](../images/AssessmentQuestionField.png)

</td></tr><tr><td>

Description

</td><td>

Information about the metric and what it evaluates. If the **Method** is **Assessment**, include details that help users understand how to answer the question. This text appears as a hint when a user points to the question text on the questionnaire.![Assessment description field tooltip](../images/AssessmentDescriptionFieldTooltip.png)

</td></tr><tr><td>

Depends on

</td><td>

Setting used to make this metric a conditional question. Select an existing metric question from the list, which displays **Checkbox**, **Choice**, **Likert Scale**, **Template**, and **Yes/No** metrics of the same category as this metric. Then, use the **Displayed when** field to set the conditions that display this metric question on questionnaires. The system prevents the creation of recursive dependencies between metrics. For example, if Metric A depends on Metric B, Metric B cannot depend on Metric A.

 This field is visible only if the Method is Assessment.

</td></tr><tr><td>

Displayed when

</td><td>

Answer options for the selected **Depends on** metric question that, when chosen on questionnaires, display this metric question.

 This field is visible and required only if the **Depends on** field is set.

</td></tr><tr><td class="sub-head" colspan="2">

Field Type Section

</td></tr><tr><td>

Data type

</td><td>

\[Required\] Format of the expected response data. The function of the data type depends on the selected **Method**. If the method is **Assessment**, the data type determines how users answer the corresponding question on questionnaires. If the method is **Script**, the data type determines how the system calculates assessment results.**Note:** If another metric depends on this metric, you cannot change the data type.

</td></tr><tr><td>

Randomize answers

</td><td>

Check box that determines whether to present the answer options for this metric question in a random order. The order of answer options can influence users, which creates biased results. Randomizing answer options can help prevent this bias.

 This field is visible only if a data type that requires metric definitions is selected.

 **Note:** Randomizing answer options for certain questions can make those questions confusing for the person answering. In general, only randomize answer options that do not follow a logical order. For example, the following question is confusing when randomization is enabled:

 ![Assessment question random order](../images/AssessmentQuestionRandomOrder.png)

</td></tr><tr><td>

Template

</td><td>

Metric template to use for the metric question. A metric template is a set of predefined answer options.

 This field is visible and required only if the **Data type** is **Template**.

**Note:** If another metric depends on this metric, you cannot change the template.

</td></tr><tr><td>

Dependent plugin

</td><td>

Plugin that contains the tables queried in the script. The system executes the metric script only if the plugin is active. The default available values are **Asset Management**, **CMDB**, **Core**, **Cost Management**, **Procurement**, and **Software Asset Management**. If the **Method** is **Script**, select a plugin.

 This field is visible only if the **Method** is **Script**.

 **Note:** An administrator may need to add more [Define an option for a choice list](https://www.servicenow.com/docs/access?context=t_ViewChoiceListDefinitions&version=yokohama&pubname=yokohama-platform-administration&section=t_DefineAnOptionForAChoiceList&ft:locale=en-US) of plugins to the field.

</td></tr><tr><td>

Scale definition

</td><td>

Setting that determines whether lesser or greater numerical values equate to a good score in assessment result calculations. Select **Low** if lesser numerical values are better, such as for a metric that measures the number of incidents for a vendor. Select **High** if greater numerical values are better, such as for a metric that measures user satisfaction on a scale of one to five. The default value is **High**.

 This field is visible and required unless the **Data type** is **Date**, **Date/Time**, or **String**. The results for these data types are not included in results calculations.

 **Note:** For information about how to set the scale definition for data types that do not require you to set a numerical value, see [Data Types](r_DataTypes.md).

</td></tr><tr><td>

Min

</td><td>

Lowest numerical value to be used as an answer option on assessments or as a scaled value in a scripted metric.

 This field is visible and required only if certain data types are selected. If the data type is **Choice** or **Likert Scale**, this field is read-only and is set automatically based on the smallest metric definition **Value**.

</td></tr><tr><td>

Max

</td><td>

Highest numerical value to be used as an answer option or scaled value.

 This field is visible and required only if certain data types are selected. If the data type is **Choice** or **Likert Scale**, this field is read-only and is set automatically based on the largest metric definition **Value**.

</td></tr><tr><td>

Script

</td><td>

Script that obtains the desired system information. This field is visible and required only if the **Method** is **Script**.

**Note:** Script can now only be edited by Assessment Admins. Survey Creators no longer have the ability to edit the script.

</td></tr><tr><td class="sub-head" colspan="2">

Related List

</td></tr><tr><td>

Assessment Metric Definitions

</td><td>

Lists all metric definitions, which appear as answer options for questions on assessment questionnaires. Click **New** to create a new metric definition.

 This related list is available only if the Data type is **Choice** or **Likert Scale**.

</td></tr></tbody>
</table>**Parent Topic:**[Assessments reference](assessment-reference.md)

**Related topics**  


[Create an assessment metric for a category](../task/t_CreateAMetric.md)

