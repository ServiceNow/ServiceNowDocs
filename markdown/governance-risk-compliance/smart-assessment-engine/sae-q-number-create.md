---
title: Create a number question
description: Enable the assessors to respond to a number question with a numerical value. Specify any of several attributes to qualify the question, for example, whether a response is required or an attachment is requested as part of your assessment template by using the Smart Assessment Engine application.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Add instructions and questions to an assessment template, Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create a number question

Enable the assessors to respond to a number question with a numerical value. Specify any of several attributes to qualify the question, for example, whether a response is required or an attachment is requested as part of your assessment template by using the Smart Assessment Engine application.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## Procedure

1.  You can update an assessment template by either opening an existing template from the landing page or by creating a new template and saving it.

    |Option|Description|
    |------|-----------|
    |**Existing template**|On the Assessment Workspace landing page, select an existing template.|
    |**New template**|Create a template as described in [Add instructions and questions to an assessment template](sae-asmnt-template-populate.md).|

2.  On the **Questions** tab for the template, select the section that you want to add the question to and then select **Add question**.

3.  In the Type section, select **Number** and then enter the question in the text box.

    The Preview section displays an example of the text box that the assessor uses for the response.

4.  Specify any number of attributes for the question and select **Save** after every change.

<table id="choicetable_afm_5mq_mbc"><thead><tr><th align="left" id="d260256e142">

Attribute

</th><th align="left" id="d260256e145">

Description

</th></tr></thead><tbody><tr><td id="d260256e151">

**Required**

</td><td>

If the assessor must answer the question to submit the assessment, select **Required**. The assessor sees the \* \(asterisk\) character to indicate that a response is required.

</td></tr><tr><td id="d260256e168">

**Conditionally visible**

</td><td>

A setting on any question type that lets template builders control when a question is shown or hidden to respondents, based on conditions tied to other questions' answers. This Option is in the configuration options menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

 Select this attribute if the question appears to the assessor only if the response to a different question meets the conditions that you specify.

 Use the condition builder to specify the conditions that are required to present this question to the assessor.

 You specify the section, subsection \(if available\), question, and, optionally, the response. Together, the values that you specify define the conditions that must be met for the question to appear in the assessment.

</td></tr><tr><td id="d260256e197">

**Justification**

</td><td>

A setting that lets template builders request additional text comments \(justification\) from respondents for a given question, either always or based on conditions. This Option is in the configuration options menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

 Enable the assessor to supply the additional text information that justifies a response. This option is useful when you expect that some responses will be nonstandard.

 In the assessment, the \* \(asterisk\) character appears on the field for a required justification.

</td></tr><tr><td id="d260256e223">

**Attachments**

</td><td>

A setting that lets template builders request file attachments \(evidence\) from respondents for a given question, either always or based on conditions. This Option is in the configuration options menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

Request the attachments for the specific responses. You can specify that the attachments are: -   Required
-   Optional
-   The request for the attachments appears only if the response meets the conditions that you specify.

Use the condition builder to specify the conditions. The values that you specify define the conditions that must be met to enable the assessor to add the attachments.

</td></tr><tr><td id="d260256e260">

**Set number range**

</td><td>

Option for number question type.

 Specify the range of values that is allowed in the response.

 The Preview section displays an example of the text box that the assessor uses for the response.

 The default number range is a minimum value of 0 and a maximum value of 1000.

</td></tr><tr><td id="d260256e282">

**Specify preferred answers**

</td><td>

A setting on choice-type questions that lets template builders define which answers are considered "preferred". This Option is in the configuration options menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

 Use the "Mark preferred answers" modal to define conditions for preferred answers.

</td></tr></tbody>
</table>5.  If you want to add content that helps the assessor answer this question, select **Add additional content**.

<table id="choicetable_up4_xqd_mbc"><tbody><tr><td id="d260256e321">

**Question description**

</td><td>

Enter the descriptive text that follows the question when the assessor accesses the question.

 A confirmation box displays the text as an assessor sees it. Update the text by selecting **Edit**.

 ![Confirmation of the description text. You can update the text.](../image/sae-q-description-confirmation.png)

</td></tr><tr><td id="d260256e346">

**Guidance**

</td><td>

Enter the content that explains how best to answer the question. Add the formatted text, table, images, links, and attachments. The **Attach image** option enables you to attach descriptive images in the guidance section of the assessment questions. This means that template managers can include helpful visuals to assist respondents, making the instructions clearer and easier to understand. You can include one image per question, with mandatory alt text. The content appears in a pop-up window when the assessor accesses the question.A confirmation box displays the list of items that are provided to an assessor. Update the content by selecting **Edit**.

![Confirmation of the guidance content. You can update the content.](../image/sae-q-guidance-confirmation.png)

</td></tr></tbody>
</table>6.  Select **Save**.


