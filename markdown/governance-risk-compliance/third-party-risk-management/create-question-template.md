---
title: Create a questionnaire or document request template using the Designer
description: Use the Questionnaire Template Designer to create and edit questionnaire or document request templates that you can use as the basis for other templates.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a questionnaire or document request template using the Designer

Use the Questionnaire Template Designer to create and edit questionnaire or document request templates that you can use as the basis for other templates.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

<table id="id_g5g_vwv_szb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric or Assessment metric

</td><td>

A single question within a questionnaire template.

</td></tr><tr><td>

Metric type or Assessment metric type

</td><td>

A questionnaire template.

</td></tr><tr><td>

Category or Assessment category

</td><td>

A set of related questions within a questionnaire template.**Note:** There can be multiple categories within a metric type.

</td></tr></tbody>
</table>**Note:** A questionnaire template must have at least one category. Each category must contain at least one question.

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Third-party Risk Management** &gt; **Assessment setup** &gt; **Questionnaire Templates** or **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Document Request Templates**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Assessment setup** &gt; **Questionnaire Templates**.
2.  Select **New \(Designer\)**.

    |Tab|Description|
    |---|-----------|
    |Controls|Supported question data types are available in the Controls palette. Drag a control onto the designer canvas to create a question of that type.|
    |Questions|A library of questions for various categories, so you don’t have to build each questionnaire from scratch.|
    |Categories|Assessment open in the **Design** view. The questionnaire **Name** field appears above the first category in the canvas. An empty question field appears in the category container.|

3.  Enter a name and then drag a control onto the designer canvas to create a question of that type.

    **Note:** Selecting the scored option \(**Scored** check box\) is optional. All question responses unless otherwise stated are scored. The scored option changes the scoring behavior. If selected, the score is based on a binary system \(0 or 100\) reflecting whether the answer is correct or incorrect. If not selected, the score is calculated using a scale definition, involving the questionRating, questionPercentContribution, and questionNormalizedValue formulae, and the MaximumNormalizationInput field can influence the normalized value. For more information, see [Scoring calculations using the classic assessment engine](../concept/vendor-ratings-scoring.md) and [Normalize the scores for metrics](../../grc-vendor-risk-implementation/concept/set-max-norm-input.md).

    |Data type|Description|Scored|
    |---------|-----------|------|
    |Attachment|Question with a manage attachments icon for users to attach one or more files.|Y|
    |Boolean|Question with a check box or a **Yes/No** list for user responses.|N|
    |Choice|List of predefined options. For more information, select the definition for **Choices**.|Y|
    |Date|Date field.|N|
    |Date/Time|Date and time field.|N|
    |Number|Number field with predefined minimum and maximum values. The default is 1–10.|N|
    |Percentage|Percentage field with a prescribed range.|N|
    |Scale|Predefined Likert scale. Answer options appear as radio buttons.|Y|
    |Numeric Scale|Selectable number scale. The default is 1–5. Answer options appear as radio buttons.|Y|
    |String|Single or multi-line text field.|N|
    |Template|Choice list of templates that provide a predefined scale of options.|Y|
    |Reference|Choice list of fields from a specified reference table. This data type doesn’t support reference qualifiers.|N|
    |Image Scale|Choice list of images you can use for scales.|N|
    |Multiple Selection|List of selectable choices. Multiple choices are allowed.|N|
    |Ranking|Selectable scale for ranking choices.|N|

4.  Select the form context menu to select one of the following options.

<table id="choicetable_mvf_45v_lz"><tbody><tr><td id="d87802e528">

**Save**

</td><td>

Save the current questionnaire or document request.

</td></tr><tr><td id="d87802e537">

**Preview**

</td><td>

Display a preview of the questionnaire or document request with its current settings.

</td></tr><tr><td id="d87802e546">

**New Assessment**

</td><td>

Open a fresh canvas for a new questionnaire or document request.

</td></tr><tr><td id="d87802e555">

**Load Assessment**

</td><td>

Open the list of existing questionnaires or document requests that are available for use.

</td></tr><tr><td id="d87802e564">

**Copy Assessment**

</td><td>

Create a copy of the questionnaire or document request that you can edit.

</td></tr></tbody>
</table>
