---
title: Create or modify Smart Assessment template
description: Create or modify Smart Assessment template and associate it with Work Order Task tables to create Smart Assessment questionnaires for work order tasks using this template.
locale: en-US
release: yokohama
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-02-19"
reading_time_minutes: 3
breadcrumb: [Configuring Smart Assessment questionnaires for Now Mobile Agent, Setting up Field Service Mobile Agent, Configuring Field Service Management, Field Service Management]
---

# Create or modify Smart Assessment template

Create or modify Smart Assessment template and associate it with Work Order Task tables to create Smart Assessment questionnaires for work order tasks using this template.

## About this task

You can create Smart Assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart Assessment template allows you to create Smart Assessment questionnaires for work order tasks. Smart Assessment questionnaires helps you to evaluate various situations, aspects, or records.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Either create a template or select an existing template.

<table id="choicetable_lml_jwt_dcc"><thead><tr><th align="left" id="d130361e100">

Option

</th><th align="left" id="d130361e103">

Description

</th></tr></thead><tbody><tr><td id="d130361e109">

**Select an existing template**

</td><td>

1.  Select an existing template.
2.  In the **General** tab, select **Settings**.


</td></tr><tr><td id="d130361e133">

**Create a new template**

</td><td>

1.  Select **New template**.
2.  On the Create assessment template form, fill in the fields.

For a description of the field values, see [Smart Assessment template fields](../reference/smart-assessment-template-fields.md).

3.  Select **Create**.


</td></tr></tbody>
</table>    The Details page on the **General** tab displays the information that you provided to create the template.

3.  Select **Settings** to set the duration and role.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration

</td><td>

Default time period in days between when the assessment is sent and when responders are expected to return a completed assessment.

 This setting is used to calculate the **Due date** value for assessments that are generated from this template.

</td></tr><tr><td>

Assessment reader role

</td><td>

Role required to view an assessment generated from the template.

</td></tr></tbody>
</table>4.  On the **Questions** tab, select **Add instructions**.

    1.  Enter the information that a responder might find useful in the Instructions text box.

        This information could include the purpose of the assessment, the ways that the responses are used or analyzed, and so on.

    2.  Select **Save**.

5.  Select **Add section** to add a section that can hold questions.

    The sections organize the questions into manageable groups. For example, an assessor who is knowledgeable about a subject can answer all questions in one section and an assessor with a different area of expertise can respond to questions in another section. The sections can contain either the subsections or questions, but not both. The subsections can only contain questions but no other subsections.

    **Note:** At any time, you can select a section in the list and then select **Delete** to delete that section.

6.  Enter a name and description for the section and then select **Save**.

7.  Select a section in the list and then select **Add question**.

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
    |Create and configure text type questions.|[Create a text question](https://www.servicenow.com/docs/access?context=sae-q-text-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure drop-down list type questions.|[Create a drop-down list question](https://www.servicenow.com/docs/access?context=sae-q-drop-down-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure radio button type questions.|[Create a radio button question](https://www.servicenow.com/docs/access?context=sae-q-radio-button-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure check box type questions.|[Create a check box question](https://www.servicenow.com/docs/access?context=sae-q-check-box-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure number type questions.|[Create a number question](https://www.servicenow.com/docs/access?context=sae-q-number-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure reference type questions.|[Create a reference question](https://www.servicenow.com/docs/access?context=sae-q-reference-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure attachment type questions.|[Create an attachment question](https://www.servicenow.com/docs/access?context=sae-q-attachment-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|
    |Create and configure date type questions.|[Create a date question](https://www.servicenow.com/docs/access?context=sae-q-date-create&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|

8.  Select **Save**.

9.  Select **Publish**.

    **Note:**

    -   You can create a Smart Assessment questionnaire only from a published template.

    -   You can update a published template only if no active assessment is associated with the template.


## Result

The Smart Assessment template is created or modified.

## What to do next

[Create a Smart Assessment questionnaire](create-smart-assessment-questionnaire.md)

**Related topics**  


[Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)

[Using the template designer](https://www.servicenow.com/docs/access?context=sae-template-designer&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)

