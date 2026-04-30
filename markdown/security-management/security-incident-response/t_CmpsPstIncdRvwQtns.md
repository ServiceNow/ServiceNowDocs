---
title: Compose post incident review questions
description: You can use the questions that come with the base system or create your own questions.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Perform a questionnaire-based post incident review, Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Compose post incident review questions

You can use the questions that come with the base system or create your own questions.

## Before you begin

Role required: sn\_si.admin

## About this task

The methods for gathering post incident review information can be in the form of questions or as data automatically collected using scripts.

Questions can depend on the answers to other questions. For example, you might ask if all necessary logs were available. If the answer is No, you ask a follow-up question to ascertain which of the needed logs were not enabled.

Scripted data collection, also called script metrics, gather data related to the security incident via scripts you write. This action can go well beyond the data in the security incident record itself. For example, a script metric could gather the recent outage time for a server affected by this security incident.

Finally, you can mix the two types. Questions can have default values taken from a script, or simply from a field in the security incident record. When you use a `Default Answer from…` type of question, you can choose if you want the user to always answer the question – with the default value providing them an initial value – or if you want the user to only be asked the question if the script or field comes up empty.

To create a new question:

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Post Incident Review**.

2.  Click the category for which you want to create a new question.

3.  Click the **Assessment Metrics** tab.

4.  Click **New**.

    You can also click an existing question to modify it.

5.  Fill in the fields on the form, as appropriate.

<table id="table_qvm_fbd_3t"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the metric \(question or script\). If the metric is a scripted data collection, this name appears on the post incident report.

</td></tr><tr><td>

Category

</td><td>

The category that the metric belongs to. The system automatically populates this category if you create a new metric from the Metric Category form. **Note:** You cannot change the category if the **Depends on** field is set or if another metric depends on this metric

</td></tr><tr><td>

Method

</td><td>

Indicates the type of metric, as follows:

-   **Assessment**: A question that has no default value. There are several data types that can be defined in the **Data Type** field on the **Field Type** tab, such as check boxes, choice lists, text input.
-   **Script**: Scripted metric. Obtain values by writing a custom script. The **Script** method is compatible with the **Duration**, **Number**, and **Percentage** data types.
-   **Default answer from field**: A question where the default response comes from a selected field in the security incident. Selecting this option adds two fields to the **General** tab:
    -   **Default answer**: Select the field in the security incident that contains the default answer for the question. For example, for the question: "Who initially reported this incident?", the **Requested by** field would be a likely choice.
    -   **Ask question**: Specifies when to ask the question: always or only if the **Default answer** field is empty. Using the example above, the question would be asked if the **Requested by** field is empty.
-   **Default answer from script**: A question where the default answer comes from a script. The answer may be a number, string, or percentage. The **General** tab adds a field:

**Ask question**: as the Specifies when to ask the question: always or only if the script does not provide a default answer. The script is defined on the **Field Type** tab.

 **Note:** If you select a **Data type** that is incompatible with the selected **Method**, the system automatically changes the **Method** to a compatible value.

</td></tr><tr><td>

Weight

</td><td>

\[Required\] Numeric value that represents the importance of this metric relative to other metrics in the same category. By default, the weight is 10.

 This field is visible and required unless the **Data type** is **Date**, **Date/Time**, or **String**. These data types are not included in results calculations.

</td></tr><tr><td>

Order

</td><td>

\[Required\] Numeric value that determines the order of the metric question on assessment questionnaires, relative to other metric questions in the same category. The metric with the smallest order value appears as the first question in the category section. By default, the order is 100.

**Note:** It does not matter which order value you use for metrics with the Script method, as they do not appear on questionnaires.

</td></tr><tr><td>

Active

</td><td>

Check box that determines whether this metric is used. If the check box is not selected, it is as if the metric record does not exist.

</td></tr><tr><td>

Mandatory

</td><td>

Check box that makes the metric question mandatory \(selected\) or optional \(cleared\) on assessment questionnaires. Users cannot submit questionnaires until they provide valid responses to all mandatory questions, which are denoted by a red field status indicator.

 This field is visible only if the **Depends on** field is empty, and the data type is not **Checkbox**.

</td></tr></tbody>
</table>6.  Click the **General** tab and fill in the fields, as appropriate.

<table id="table_swb_mcd_3t"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Text to use as the question on security incident review questionnaires. Enter a clear, straightforward question that is easy to answer, such as **How did we contain the incident**

</td></tr><tr><td>

Description

</td><td>

Information about the metric and what it evaluates. If the **Method** is **Assessment**, include details that help users understand how to answer the question. This text appears as a hint when a user points to the question text on the questionnaire.

</td></tr><tr><td>

Depends on and Displayed when

</td><td>

Select a question in the **Depends on** field that the current question depends on. For example, the question, "What additional logs were needed?" depends on the question "Were all needed logs available?"

 Next, use the **Displayed when** field to identify when you want the dependent question to appear in questionnaires. For example, if you want the dependent question to be asked only when the user answers **No** to the "Were all needed logs available?" question, select **No** in the **Displayed when** field.

 **Note:** The system prevents the creation of recursive dependencies between metrics. For example, if Metric A depends on Metric B, Metric B cannot depend on Metric A.

</td></tr></tbody>
</table>7.  Click the **Field Type** tab and fill in the fields, as appropriate.

<table id="table_ybl_pdd_3t"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data type

</td><td>

The data type of the expected response the list of types available depends on for the selected method. If the method is **Assessment**, the data type determines how users answer the corresponding question on questionnaires. If the method is **Script**, the data type determines how the system calculates assessment results.**Note:** If another metric depends on this metric, you cannot change the data type.

</td></tr><tr><td>

Randomize answers

</td><td>

Check box that determines whether to present the answer options for this metric question in a random order each time a user opens an assessment questionnaire that contains the question. Answer preference can be influenced by the order in which answer options appear. This can result in biased results. Randomizing answer options can help prevent this bias.

 This field is visible only if you select **Likert scale** or **Choice** in the **Data type** field.

</td></tr><tr><td>

Dependent plugin

</td><td>

\[Required if the **Method** is **Script**.\]Plugin that contains the tables queried in the script. The system executes the metric script only if the plugin is active. The default available values are **Asset Management**, **CMDB**, **Core**, **Cost Management**, **Procurement**, and **Software Asset Management**.

 This field is visible only if the **Method** is **Script**.

 **Note:**

-   If the Core default value is used, the script is always run.
-   If you are an administrator, you can add more choices of plugins to the field.


</td></tr><tr><td>

Scale definition

</td><td>

Setting that determines whether lesser or greater numerical values equate to a good score in assessment result calculations. Select **Low** if lesser numerical values are better, such as for a metric that measures the number of defects for a vendor. Select **High** if greater numerical values are better, such as for a metric that measures user satisfaction on a scale of one to five. The default value is **High**.

 This field is visible and required unless the **Data type** is **Date**, **Date/Time**, or **String**. The results for these data types are not included in results calculations.

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

Script that obtains the desired system information. The script has one input variable, set with the ID of the security incident \(primary\), and three possible output variables set by the script, string\_result, scaled\_result, and actual\_result. When the data type is String, only the string\_result is required.

 This field is visible and required when the **Method** is **Script**, or the default value comes from a script.

</td></tr><tr><td>

Template

</td><td>

A predefined set of common answers to use for the question. For example, a frequency template would likely start with a value of "Never," and go up to the top value of "Always."

 This field is visible and required only if the **Data type** is **Template**.

**Note:** If another metric depends on this metric, you cannot change the template.

</td></tr></tbody>
</table>8.  When you have completed your entries, click **Update**.


