---
title: Create a privacy assessment
description: Create various types of assessments and send those assessments to the business process or business application owners to collect their responses. The responses help you to understand how personal information \(PI\) is being used or stored in a processing activity.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Create a privacy assessment

Create various types of assessments and send those assessments to the business process or business application owners to collect their responses. The responses help you to understand how personal information \(PI\) is being used or stored in a processing activity.

## Before you begin

Role required: sn\_privacy.admin and sn\_privacy.manager

## About this task

Using the privacy assessment capability, you can create various types of assessments such as privacy screening initial assessments, privacy impact assessments \(PIA\), and privacy readiness assessments.

The following capabilities are provided to configure the assessments:

-   Mapping control objectives to the responses of the question.
-   Mapping information objects to the responses of the question.
-   Mapping the processing activity fields to the responses of the questions.

While configuring the assessments, consider the following terminology:

-   Metric type refers to the assessment template.
-   Metric category refers to the section label in the assessment.
-   Metric refers to a question.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **New Assessment Template**.

2.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assessment template.

</td></tr><tr><td>

Assessment duration

</td><td>

Length of time allowed for completing the assessment from the time the assessment is generated.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records.

</td></tr><tr><td>

Auto approve privacy assessment tasks

</td><td>

Option to indicate that the privacy assessment tasks must be automatically approved without a review. When this option is selected, after the assessment task is submitted, automatically the assessment task is approved and controls, risks and the information objects are created on the processing activity, and the task is closed.

</td></tr><tr><td>

State

</td><td>

State of the assessment. This field is automatically set to **Draft**.

</td></tr><tr><td>

Roles

</td><td>

Roles that have read access to the template.

</td></tr><tr><td>

Classification

</td><td>

Classification of assessment metric type. The choices are the following:-   **None**
-   **Initial Assessment**
-   **PIA Assessment**


</td></tr><tr><td>

Description

</td><td>

Purpose of the assessment template and the reason for its creation.

</td></tr><tr><td>

Introduction

</td><td>

Guidance text for business users who respond to the assessment.

</td></tr></tbody>
</table>3.  Click **Save and Open Designer**.

    The designer contains the following elements.

    |Element|Description|
    |-------|-----------|
    |Controls|Supported question data types that are available in the Controls palette.|
    |Questions|Library of questions for various categories.|
    |Categories|New assessment opens in the Design view. The questionnaire **Name** field appears above the first category in the canvas. An empty question field appears in the category container.|

4.  Drag a control on the designer canvas to create a question of that type.

    The canvas contains the following types of questions controls.

<table id="table_dgb_pvh_br"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment

</td><td>

Questions that enable users to attach one or more files as a response.

</td></tr><tr><td>

Boolean

</td><td>

Questions with the following value types:-   A check box to select or clear.
-   A Yes or No answer.


</td></tr><tr><td>

Choice

</td><td>

Questions with a list of predefined options.

</td></tr><tr><td>

Date

</td><td>

Date field. Enables you to collect the date information filled in by a respondent.

</td></tr><tr><td>

Date/Time

</td><td>

Date and time field. Enables you to collect the date and time information filled in by a respondent.

</td></tr><tr><td>

Number

</td><td>

Number field with predefined minimum and maximum values. The default range is 1–10.

</td></tr><tr><td>

Percentage

</td><td>

Percentage field with a prescribed range.

</td></tr><tr><td>

Scale

</td><td>

Predefined Likert scale. Answer options appear as radio buttons.

</td></tr><tr><td>

Numeric Scale

</td><td>

Numeric or numerical scale. Requires the respondent to provide the response in terms of numerical values.

</td></tr><tr><td>

String

</td><td>

Single or multi-line text field.

</td></tr><tr><td>

Template

</td><td>

List of templates that provide a predefined scale of options.

</td></tr><tr><td>

Reference

</td><td>

List of fields from a specified reference table.

</td></tr><tr><td>

Image Scale

</td><td>

Image question. Enables you to click images as your answer to a question.

</td></tr><tr><td>

Multiple Selection

</td><td>

Multiple options. You can select multiple options as responses.

</td></tr><tr><td>

Ranking

</td><td>

Question type with options as answers. The options must be ranked.

</td></tr></tbody>
</table>5.  Point to **Save** and then select **Save and Publish**.

    The state of the template changes to Published.


## Result

The assessment template with the questions is ready to be sent to the entity owner.

## What to do next

After the template is published, send it to the entity or processing activity owners to collect responses. For more information, see [Send a privacy assessment to an entity](send-privacy-assessmt-entity.md) and [Respond to a privacy screening assessment](respond-to-privacy-assmnt.md).

After responses are submitted, review and approve the assessment. For more information, see [Review a privacy assessment](review-a-privacy-assessment.md).

To map assessment responses to a processing activity, see [Map the processing activity fields to a question response](copy-responses-to-ropa.md).

-   **[Write a processing activity script](configure-a-processing-activity-script.md)**  
Write custom scripts on the assessment templates to update the processing activity fields using a script. The script runs when the assessment response is completed. You can write multiple scripts for both screening assessments and impact assessments.
-   **[Map a control objective to a question response](relate-control-objectives-to-ropa.md)**  
Map the control objectives to the responses of the assessment questions to automatically create and apply the respective controls on the processing activity.
-   **[Map an information object to a question response](relate-io-to-ropa.md)**  
Map the \[PI\] Information objects to the responses of the assessment questions that must be associated to the processing activity. This association helps the privacy teams to understand what personal information is being processed by the processing activity.
-   **[Map a risk statement to a question response](map-risk-statements-to-pa.md)**  
Map the risk statements to the responses of the assessment questions to automatically create and apply the respective risks on the processing activity.
-   **[Map the processing activity fields to a question response](copy-responses-to-ropa.md)**  
Map some of the processing activity fields with the responses of the assessment questions to update the processing activity details based on the assessment response.

**Parent Topic:**[Configuring Privacy Management](../concept/configure-privacy-mgmt.md)

**Related topics**  


[Smart assessments in Privacy Management](../concept/smart-assessments-in-privacy-management.md)

