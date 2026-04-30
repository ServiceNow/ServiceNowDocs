---
title: Create an attachment question
description: Enable the assessors to respond to an attachment question by adding one or more files as a response. Specify any of several attributes to qualify the question, for example, whether a response is required or an attachment is requested as part of your assessment template by using the Smart Assessment Engine application.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Add instructions and questions to an assessment template, Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create an attachment question

Enable the assessors to respond to an attachment question by adding one or more files as a response. Specify any of several attributes to qualify the question, for example, whether a response is required or an attachment is requested as part of your assessment template by using the Smart Assessment Engine application.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## Procedure

1.  Open the assessment template to add questions on the landing page or create a template to add questions.

    |Option|Description|
    |------|-----------|
    |**Existing template**|On the Assessment Workspace landing page, select an existing template.|
    |**New template**|Create a template as described in [Add instructions and questions to an assessment template](sae-asmnt-template-populate.md).|

2.  On the **Questions** tab for the template, select the section that you want to add the question to and then select **Add question**.

3.  In the Type section, select **Attachment** and then enter the question in the text box.

    The Preview section displays an example of how the attached file appears to the assessor.

4.  Specify any number of attributes for the question and select **Save** after every change.

<table id="choicetable_afm_5mq_mbc"><thead><tr><th align="left" id="d108248e141">

Attribute

</th><th align="left" id="d108248e144">

Description

</th></tr></thead><tbody><tr><td id="d108248e150">

**Required**

</td><td>

If the assessor must answer the question in order to submit the assessment, select **Required**. The assessor sees the \* \(asterisk\) character to indicate that a response is required.

</td></tr><tr><td id="d108248e167">

**Conditionally visible**

</td><td>

Option in the additional attributes menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

 Select this attribute if the question appears to the assessor only if the response to a different question meets the conditions that you specify.

 Use the condition builder to specify the conditions that are required to present this question to the assessor.

 You specify the section, subsection \(if available\), question, and, optionally, the response. Together, the values that you specify define the conditions that must be met for the question to appear in the assessment.

</td></tr><tr><td id="d108248e196">

**Justification**

</td><td>

Option in the additional attributes menu \(![Additional attributes menu icon.](../../grc-business-continuity-management/image/AlertMenuIcon.png)\).

 Enable the assessor to supply the additional text information that justifies a response. This option is useful when you expect that some responses will be nonstandard.

 In the assessment, the \* \(asterisk\) character appears on the field for a required justification.

</td></tr></tbody>
</table>5.  If you want to add content that helps the assessor answer this question, select **Add additional content**.

<table id="choicetable_up4_xqd_mbc"><tbody><tr><td id="d108248e238">

**Question description**

</td><td>

Enter the descriptive text that follows the question when the assessor accesses the question.

 A confirmation box displays the text as an assessor sees it. Update the text by selecting **Edit**.

 ![Confirmation of the description text. You can update the text.](../image/sae-q-description-confirmation.png)

</td></tr><tr><td id="d108248e263">

**Guidance**

</td><td>

Enter the content that explains how best to answer the question. Add the formatted text, table, images, links, and attachments. The content appears in a pop-up window when the assessor accesses the question.

 A confirmation box displays the list of items that are provided to an assessor. Update the content by selecting **Edit**.

 ![Confirmation of the guidance content. You can update the content.](../image/sae-q-guidance-confirmation.png)

</td></tr></tbody>
</table>6.  Select **Save**.


