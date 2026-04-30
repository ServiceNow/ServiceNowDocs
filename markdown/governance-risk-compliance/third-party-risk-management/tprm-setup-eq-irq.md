---
title: Set up internal questionnaire responses to automatically attach external questionnaires to assessments
description: Set up an internal questionnaire's responses to automatically attach questionnaires to external assessments that are based on the responses, the calculated risk tier, or both by using Third-party Risk Management. By setting up this configuration, you can help to improve your ability to respond to risk tier changes and internal questionnaire responses.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up internal questionnaire responses to automatically attach external questionnaires to assessments

Set up an internal questionnaire's responses to automatically attach questionnaires to external assessments that are based on the responses, the calculated risk tier, or both by using Third-party Risk Management. By setting up this configuration, you can help to improve your ability to respond to risk tier changes and internal questionnaire responses.

## Before you begin

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

**Note:** Automatic attachment of questionnaires to external assessments based on inherent risk questionnaire \(IRQ\) responses or IRQ-calculated risk tiers is currently not supported in Smart Assessment Engine.

## About this task

You can set up questionnaires to be automatically added to external assessments based on responses to an internal questionnaire, calculated risk tiers, or both. Risk tiers are determined based on the responses collected after an internal assessment is completed. You can configure whether the risk tier that is used to automatically attach a questionnaire is calculated after the IRQ is completed or for the engagement as part of its internal assessment. For more information on risk tiers, see [VRM third-party risk tiering assessments](../reference/manage-risk-tiering-assessments.md).

## Procedure

1.  Navigate to **All** &gt; **Third Party Risk Management** &gt; **Assessment Setup** &gt; **Questionnaire Templates**.

2.  Select the internal questionnaire template that you want to use.

    **Note:** The questionnaire must have the IRQ template classification.

3.  Select the Metric Categories related list, the category name, and then select the question from the Assessments Metrics related list that you want to configure.

    For more information on the different types of questions and how to define them, see [Define a question](../../grc-vendor-risk-implementation/task/tprm-questions-create.md).

4.  Add a configuration to the Questionnaires templates related list by selecting **New**.

5.  On the form, fill in the fields.

<table id="table_oyj_52z_hrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Type of question in the questionnaire that you’re configuring. For example, it could be a choice or string question.

</td></tr><tr><td>

Answer

</td><td>

Answer that results in the questionnaire to be attached to the external assessment.

</td></tr><tr><td>

Tier

</td><td>

Risk tier that results in the questionnaire to be attached to the external assessment.

</td></tr><tr><td>

Tier from level

</td><td>

Level at which the referenced risk tier is calculated: IRQ assessment or Engagement.

For example, if the risk tier that is calculated during the inherent risk questionnaire assessment matches what you selected for the **Tier** field, the questionnaire is attached to the external assessment.

</td></tr><tr><td>

Questionnaire

</td><td>

Questionnaire that is attached if the requirements that are defined by this form are met.

</td></tr><tr><td>

Applies to

</td><td>

Type of external assessment that the questionnaire is attached to.

</td></tr></tbody>
</table>6.  Select **Submit**.


