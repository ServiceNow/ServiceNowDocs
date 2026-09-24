---
title: Set up and maintain a question bank
description: After you add a question to a question bank, you can reuse it in any assessment by dropping it into the assessment. You can create custom questions, add existing questions, or add and customize the sample questions that are included with the base system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-question-bank-create.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up and maintain a question bank

After you add a question to a question bank, you can reuse it in any assessment by dropping it into the assessment. You can create custom questions, add existing questions, or add and customize the sample questions that are included with the base system.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

The steps below describe the question bank feature for the classic assessment engine. If your organization uses the Smart Assessment Engine \(SAE\), question banks work differently. For more information, see the note at the end of this topic.

## Procedure

1.  Define an assessment category by navigating to **All** &gt; **Third-party Risk Management** &gt; **Administration** &gt; **Question Bank**, and then select **New**.

2.  Enter a descriptive name and description for the assessment category and then select **Save**.

3.  Open the record by selecting the name of the new assessment category.

4.  Add an assessment metric \(a question\) to the category using one of the following methods.

<table id="choicetable_rkc_13z_hcc"><thead><tr><th align="left" id="d60626e114">

Option

</th><th align="left" id="d60626e117">

Description

</th></tr></thead><tbody><tr><td id="d60626e123">

**Create a question**

</td><td>

Select **New** and fill out the form. For more information, see [Define a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-questions-create.md).

</td></tr><tr><td id="d60626e146">

**Add a question**

</td><td>

Add a question from an existing questionnaire template.1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Questionnaire Templates** and select the questionnaire template you want.
2.  Select the question from the metric categories related list and then select **Add to Question Bank**.
3.  Select the question bank where you would like the question added.
The question has been added to the question bank.

</td></tr></tbody>
</table>5.  Select **Update** to save the questions to the question bank in the current assessment category.


## What to do next

SAE question banks

For SAE templates, a **Type** field on the template determines whether it functions as a standard assessment template or as a question bank:

-   **Template**: the template is used to create assessments, as described elsewhere in this docset. Out-of-box SAE templates are set to this type.
-   **Question bank**: the template functions as a shareable pool of questions rather than a standalone assessment template.

A **Purposes** field on the template lets you share a question bank across multiple template categories, rather than restricting it to a single category.

A **Question bank category roles** field on the template category record lets you restrict which users can reference question bank questions from that category. Users can reference questions only from categories they're authorized for.

