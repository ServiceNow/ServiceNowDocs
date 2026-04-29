---
title: Review responses to external questionnaires
description: Third-party contacts use the Third-party portal to complete assessments and collaborate with the TPR manager in the comments section for each question. When assessments reveal gaps, the TPR manager or the TPR assessor can generate an issue or task. In addition, the Vendor Management Workspace application can auto-generate issues.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Review responses to external questionnaires

Third-party contacts use the Third-party portal to complete assessments and collaborate with the TPR manager in the comments section for each question. When assessments reveal gaps, the TPR manager or the TPR assessor can generate an issue or task. In addition, the Vendor Management Workspace application can auto-generate issues.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

If the TPR manager or TPR assessor decides that an assessment response is unsatisfactory, they can return some of the questions or document requests in the assessment. Incorrect answers to questions can automatically generate issues, or issues can be generated manually from the question. The comments identify the issues to the third-party contact.

To enable TPR assessors to modify responses, configure the **Allow TPR assessors to modify responses in third-party questionnaires** \[`sn_svdp.allow_assessor_edit`\] system property. You can set the following options:

-   Enable TPR assessors to answer questions or modify responses \(default\)
-   Enable TPR assessors to modify responses
-   Do not enable TPR assessors to answer questions or modify responses

See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Third-party risk management** &gt; **External risk assessments** &gt; **All open**.

2.  Select the External assessment \(VRA\) number of an assessment that is in the **Responses received** state.

3.  On the Risk overview tab, in the Questionnaires and document requests section select the templates related list, select the **Name** or **Questionnaire instance** to open the questionnaire that you want.

4.  If you’re using the Classic assessment engine, you can fill in the following fields.

<table id="table_eyj_cn3_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reviewer comment

</td><td>

Text that provides internal information about the state of responses.

</td></tr><tr><td>

Show follow-up only

</td><td>

Select the check box to display only questions that were flagged as needing a follow-up \(the **Follow up** check box was selected when the assessment was returned to the third-party for updates\).

</td></tr><tr><td>

Show incorrect or un-scored responses only

</td><td>

Select the check box to display only questions with an incorrect answer or for which no response was given.

</td></tr><tr><td>

Show unanswered questions only

</td><td>

Select the check box to display only questions for which no response was given.

</td></tr><tr><td>

Hide comments

</td><td>

Select the check box to hide all **Comment** text boxes.

</td></tr><tr><td>

Include this question when creating an issue

</td><td>

Select the check box to indicate that you want to create an issue dealing with this question. You can add an **Internal comment**.**Note:** If you have already created an issue for a question, the field is inactive to help prevent you from creating an additional issue for the question.

</td></tr><tr><td>

Follow up

</td><td>

Select the check box to make the external comment visible to the third party.

</td></tr><tr><td>

Comment for third party

</td><td>

Select the check box to add an **External comment** for the third party.

</td></tr></tbody>
</table>5.  After you review the assessment and add comments, perform one of the following steps.

<table id="choicetable_yxv_pmr_5mb"><thead><tr><th align="left" id="d137409e267">

Choice

</th><th align="left" id="d137409e270">

Description

</th></tr></thead><tbody><tr><td id="d137409e276">

**To generate issues associated with each question in the classic assessment engine**

</td><td>

Select **Create Issue**. A message with the issue number appears, and each question with an issue shows an icon to indicate that you can’t create a new issue for the question. The indicator is removed when the issue is closed or canceled.![Question with an issue.](../image/ws-issue-icon.png)

 **Note:** This is available when you’re using the Classic assessment engine.

</td></tr><tr><td id="d137409e299">

**To resubmit the assessment to the third party or engagement**

</td><td>

Select **Return to third party**.If the assessment schedule might be affected, you can extend the term by adjusting the number of days in the **Return questionnaire** window.

**Note:** After the assessment has been submitted, the third party or engagement can’t make edits to the assessment. You can return the assessment to the third party or engagement if changes are required.

</td></tr><tr><td id="d137409e318">

**To export a spreadsheet with responses, comments, and issues in the classic assessment engine**

</td><td>

Select **Export responses**.A Microsoft Excel spreadsheet is generated containing the latest responses, comments, issues, and assessment details.

**Note:** This is available when you’re using the Classic assessment engine.

</td></tr><tr><td id="d137409e337">

**To add notes or comments and review questionnaire activity**

</td><td>

Select the **Notes and Comments** tab.**Note:** This is available when you’re using the Classic assessment engine.

</td></tr></tbody>
</table>
