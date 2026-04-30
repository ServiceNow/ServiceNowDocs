---
title: Classic assessment configuration
description: The TPR manager and TPR admin roles involve a broad variety of responsibilities. After the TPRM base system is set up, you configure additional settings that enable and enhance everyday risk-assessment tasks.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Classic assessment configuration

The TPR manager and TPR admin roles involve a broad variety of responsibilities. After the TPRM base system is set up, you configure additional settings that enable and enhance everyday risk-assessment tasks.

## Assessment setup overview

By performing the tasks in the Assessment setup checklist for TPRM, you’re setting up and configuring the TPRM application to address your unique requirements for scoring and assessing risk for third parties, engagements, and other entities using the classic assessment engine.

**Note:**

For any custom messages you create, it is your responsibility to generate the corresponding `sys_ui_message` records. This step is crucial if you want the custom messages to be extracted and translated.

## Assessment setup checklist for TPRM

<table id="table_fc1_vsx_hcc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set up risk rating scales for scoring assessments and questionnaires.

</td><td>

You can configure the risk rating scale that is selected by default for all questionnaires.

For more information, see [Set up risk rating scales for scoring](../task/tprm-risk-rating-scales-config.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third-party risk domains or areas.

</td><td>

You can configure the scoring method and weight that is selected by default for all third parties associated with a specific risk area.

For more information, see [Define a third-party risk domain](../../grc-vendor-risk/task/tprm-risk-domain-define.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third-party risk area criteria, which are the group of risk domains or areas that apply to a type of third party.

</td><td>

You can adjust the weight and scoring method of each risk area within a criteria definition.

 For more information, see [Define third-party risk area criteria](../../grc-vendor-risk/task/tprm-risk-domain-criteria-df.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third party and engagement component criteria.

</td><td>

Components are entities that can be assessed for risk. Component criteria are groups of components that are related to a particular type of third party or engagement.

 You can’t add new components or modify existing ones. You can, however, define the criteria \(in terms of scoring method and weight\) to be used to assess the components. You can update the **Default scoring method** to specify how multiple scores for each risk area are calculated. You can use the **Default weight** to adjust the weight of third-party provider scores in the third party's overall risk rating.

 The following component classifications are available.

-   Third-party components
    -   Third-party risk assessments \(External risk assessments\)
    -   Subsidiaries
    -   Engagements
    -   Risk intelligence rating
-   Engagement components
    -   Engagement risk assessments
    -   Product
    -   Principal
    -   Facility
    -   Other

 For more information on setting up component criteria, see [Define component criteria](../../grc-vendor-risk/task/tprm-component-criteria-define.md).

 For more information on how engagement components impact third-party elements, see [Monitoring third-party elements](../../grc-vendor-risk/concept/tprm-monitor-tp-elements.md).

 Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third-party and engagement risk scoring rules.

</td><td>

Define the criteria, based on risk scores, that determine which third parties or engagements require assessments. Third-party risk scoring rules apply to subsidiaries, engagements, and third-party risk areas. Engagement risk scoring rules only apply to engagements.

For more information, see [Define third-party risk scoring rules](../../grc-vendor-risk/task/tprm-tp-risk-scoring-rules-define.md) and [Define engagement risk scoring rules](../../grc-vendor-risk/task/tprm-engagement-scoring-rules-df.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Create questionnaire or document request templates.

</td><td>

You can reuse questionnaire templates and document-request templates to streamline the creation of new questionnaires and document requests.

The following template classifications are available.-   Questionnaire template
-   Document request template
-   Tiering questionnaire template
-   Fourth-party template
-   IRQ template
-   Collection template

For more information, see [Create a questionnaire or document request template](../../grc-vendor-risk/task/create-questionnaire-template.md) and [Create a questionnaire or document request template using the Designer](../../grc-vendor-risk/task/create-question-template.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Import questionnaires using an excel spreadsheet.

</td><td>

This task is optional.After preparing your excel spreadsheet, you can import your data and then create questionnaires automatically from templates.

For more information, see [Import a questionnaire from a spreadsheet](../../grc-vendor-risk/task/import-questions-from-excel.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up a metric category \(question bank\), which is a group of questions related to a type of an assessment.

</td><td>

Add questions to a question bank so that you can reuse sets of questions in a questionnaire template. You can add new questions and questions from existing questionnaires.

For more information, see [Set up and maintain a question bank](../task/tprm-question-bank-create.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Create questions to meet your assessment requirements.

</td><td>

You can create custom questions, add existing questions, or add and customize the sample questions that are included with the base system.

For more information, see [Define a question](../task/tprm-questions-create.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up option to use normalized values for scoring.

</td><td>

You can use the **Maximum normalization input** setting to use normalized values to calculate assessment scores for Choice or Multiple Selection questions with the scored check box not selected. Normalization of values can help ensure consistent comparisons across different entities.

For more information on how this setting impacts scoring, see [Normalize the scores for metrics](set-max-norm-input.md).**Note:** This option is available under the question type tab of an assessment metric \(question\) record. For more information on setting up questions, see [Define a question](../task/tprm-questions-create.md).

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Create assessment templates for external questionnaires.

</td><td>

You can create an assessment template with set duration requirements and questionnaires attached by default to help streamline the assessment process for different types of third parties and engagements.

 For more information, see [Create an external assessment template](../../grc-vendor-risk/task/create-vendor-risk-assess-temp.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Create issue generation rules.

</td><td>

This task is optional.Set up rules that auto-generate issues for external assessments. Specify a Third-party risk assessment, a Questionnaire template, and the Questions to apply the rule to, as well as an Issue template and a Task template to use while generating it.

 For more information on setting up these rules, see [Create an issue generation rule](../../grc-vendor-risk/task/tprm-generate-issue-rule.md). Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Schedule recurring assessments.

</td><td>

This task is optional.Recurring assessments can be scheduled for third parties or engagements. You can use an assessment template you created or manually attach questionnaire and document requests as needed.

For more information, see [Configure a risk assessment to recur on a schedule](../../grc-vendor-risk/task/define-repeating-vend-assess.md).Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

</td></tr><tr><td>

Set up an internal questionnaire's responses to automatically attach questionnaires to external assessments that are based on the responses, the calculated risk tier, or both.

</td><td>

This task is optional. For more information, see [Set up internal questionnaire responses to automatically attach external questionnaires to assessments](../../grc-workspace-vrm/task/tprm-setup-eq-irq.md).

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Set up event-driven management rules.

</td><td>

This task is optional. Set up rules that auto-generate and send questionnaires and doc requests to engagements and third parties. For engagements and third parties that meet the criteria you define, you specify the schedule and the assessment templates. You can automate all request types except onboarding.

 For more information on setting up these rules, see [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md). Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Verify risk ratings and scoring calculations.

</td><td>

This task is optional. Review scores and risk ratings in your questionnaires and help ensure the accuracy and consistency of risk scoring by verifying the correct application of weights, normalized values, scoring methods, and risk rating scales.

For more information, see [Verifying scoring calculations using the classic assessment engine](../../grc-vendor-risk/concept/tprm-verif-q.md).

</td></tr></tbody>
</table>For more information on calculations for risk ratings and scoring, see [Scoring calculations using the classic assessment engine](../../grc-vendor-risk/concept/vendor-ratings-scoring.md).

For more information on assessment and score-related automation, see [Set up internal questionnaire responses to automatically attach external questionnaires to assessments](../../grc-workspace-vrm/task/tprm-setup-eq-irq.md), [Assessing your third-party risk](../../grc-vendor-risk/concept/tprm-assessing-tpr.md), [Create a VRM automated risk assessment when the assigned risk tier changes](../../grc-vendor-risk/task/create-tier-based-risk-submission.md), [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md), and [Automate actions upon risk intelligence updates](../../grc-vendor-risk/task/tprm-riskintelprvdr-submissrule.md).

