---
title: Add instructions and questions to an assessment template
description: Add instructions and questions to an assessment template by using the Smart Assessment Engine application. You can use instructions and questions to help gather precise and relevant information from designated responders.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Add instructions and questions to an assessment template

Add instructions and questions to an assessment template by using the Smart Assessment Engine application. You can use instructions and questions to help gather precise and relevant information from designated responders.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

Add instructions and questions to an assessment template 

## Procedure

1.  Open an assessment template for updates by either going to the landing page or when you create a template and save it.

    |Option|Description|
    |------|-----------|
    |**Existing template**|On the Assessment Workspace landing page, select an existing template.|
    |**New template**|When you have created a template and select **Save**, the template opens on the **General** tab.|

    The Details page on the **General** tab displays the information that you provided to create the template.

2.  Select the Settings page and then fill in the values.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration

</td><td>

Default time period in days between when the assessment is sent and when the responders are expected to return a completed assessment.

 This setting is used to calculate the **Due date** value for assessments that are generated from this template.

</td></tr><tr><td>

Assessment reader role

</td><td>

Role that is required to view an assessment that is generated from this template.

</td></tr></tbody>
</table>3.  Add instructions to the assessment.

    1.  On the **Questions** tab, select **Add instructions**.

    2.  Enter the information that a responder might find useful in the Instructions text box.

        This information could include the purpose of the assessment, the ways that the responses are used or analyzed, and so on.

    3.  Select **Save**.

4.  Add a section that can hold questions by selecting **Add section**.

    The sections organize the questions into manageable groups. For example, an assessor who is knowledgeable about a subject can answer all questions in one section and an assessor with a different area of expertise can respond to questions in another section. The sections can contain either the subsections or questions, but not both. The subsections can only contain questions but no other subsections.

    **Note:** At any time, you can select a section in the list and then select **Delete** to delete that section.

5.  Enter a name and description for the section and then select **Save**.

6.  Select a section in the list and then select **Add question**.

    ![Configuring a question. Descriptions for the sections of the form appear in the following list.](../image/sae-create-question-form-annotated.png)

    For each question type, you configure the following settings:

    -   **A: Enter the text of the question**

        Enter the question text that the assessor reads.

    -   **B: Add additional content \(optional\)**

        Add a plain text description that appears after the question and Guidance text that could contain HTML or images by selecting **Question description**. You can provide descriptive text that appears in addition to the question text and provide guidance on how best to answer the question.

    -   **C: Specify the question type and set the attributes for the type**

        Configure any one of several question types \(check box, text, date, and so on\).

        You can customize each type of question with attributes like whether a response is required or visible only when specified conditions are met, whether particular responses are correct or preferred, whether a justification is required, and so on.

        **Note:** The option to have one or multiple records selected as answers to one question is available only for the drop-down list, check box, and reference question types.

    -   **D: Specify possible responses**

        Configure a specified set of possible responses to some question types.

    For more information on configuring a question, see one of the following topics.

    |Description|Location|
    |-----------|--------|
    |Create and configure text type questions.|[Create a text question](sae-q-text-create.md)|
    |Create and configure drop-down list type questions.|[Create a drop-down list question](sae-q-drop-down-create.md)|
    |Create and configure radio button type questions.|[Create a radio button question](sae-q-radio-button-create.md)|
    |Create and configure check box type questions.|[Create a check box question](sae-q-check-box-create.md)|
    |Create and configure number type questions.|[Create a number question](sae-q-number-create.md)|
    |Create and configure reference type questions.|[Create a reference question](sae-q-reference-create.md)|
    |Create and configure attachment type questions.|[Create an attachment question](sae-q-attachment-create.md)|
    |Create and configure date type questions.|[Create a date question](sae-q-date-create.md)|
    |Create and configure code type questions.|[Create a code question](sae-q-code-create.md)|


