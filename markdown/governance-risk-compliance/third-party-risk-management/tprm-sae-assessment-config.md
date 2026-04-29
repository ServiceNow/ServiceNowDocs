---
title: Smart assessment configuration
description: The TPR manager and TPR admin roles involve a broad variety of responsibilities. After the TPRM base system is set up, you configure Smart Assessment Engine specific settings as well as other assessment settings that enable and enhance everyday risk-assessment tasks. TPRM admins can enable SAE and work with SAE templates.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Smart assessment configuration

The TPR manager and TPR admin roles involve a broad variety of responsibilities. After the TPRM base system is set up, you configure Smart Assessment Engine specific settings as well as other assessment settings that enable and enhance everyday risk-assessment tasks. TPRM admins can enable SAE and work with SAE templates.

## Assessment setup overview

By performing the tasks in the Assessment setup checklist for TPRM, you’re setting up and configuring the TPRM application to address your unique requirements for scoring and assessing risk for third parties, engagements, and other entities using the Smart Assessment Engine for TPRM assessments.

**Note:**

For any custom messages you create, it is your responsibility to generate the corresponding `sys_ui_message` records. This step is crucial if you want the custom messages to be extracted and translated.

## Assessment setup checklist for Smart Assessment Engine integration with TPRM

<table id="table_fc1_vsx_hcc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property.

</td><td>

After setting this property, SAE becomes the default assessment engine and replaces the legacy experience.

**Warning:** After this option is enabled, this selection can’t be reversed.

 For more information, see [Configure TPRM properties](../task/tprm-properties-configure.md) and [Migrating from Classic Assessment Engine to Smart Assessment Engine](../../grc-vendor-risk/concept/tprm-migrate-asmnt-sae.md).

 Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Migrate questionnaire templates.

</td><td>

This task is optional.You can migrate existing questionnaire or document request templates to an SAE template.

**Note:** If you’re setting up assessments for TPRM for the first time, you don’t need to complete this task.

For more information, see [Migrating from Classic Assessment Engine to Smart Assessment Engine](../../grc-vendor-risk/concept/tprm-migrate-asmnt-sae.md), [Migrate a template to an SAE template](../../grc-vendor-risk/task/tprm-asmnt-tmplt-migrate-metrics-to.md), [Results of migrating a template to a TPRM SAE template](../../grc-vendor-risk/reference/tprm-migrate-asmnt-template-result.md), and [How legacy metric types are migrated to sections in templates](../../assessment-engine/reference/sae-how-legacy-metrics-migrated.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Update assessment templates and issue generation rules.

</td><td>

This task is optional.Add published SAE questionnaire templates to all related assessment templates and Issue generation rules. For more information, see [Create an external assessment template](../../grc-vendor-risk/task/create-vendor-risk-assess-temp.md) and [Create an issue generation rule](../../grc-vendor-risk/task/tprm-generate-issue-rule.md).

**Note:** If assessment templates aren’t updated to be compatible with SAE templates, tier-based, provider-based, issue generation, and event-driven management rules won’t run as expected.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Create post assessment impact automation rules.

</td><td>

This task is optional.Configure automation rules that trigger impact actions after an assessment is completed. These rules can initiate workflows such as risk mitigation, notifications, or updates to related records based on assessment outcomes.

Plugin Dependency: Smart Assessment Post-assessment Actions \(com.sn\_impact\_fwk and com.sn\_smart\_imp\_auto\).

Access vendor risk assessment configurations, including automation rule setup and impact framework integration. Rules are asynchronous and can be tailored to specific assessment types or risk thresholds.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Create response automation rules.

</td><td>

This task is optional.Enable automatic responses for assessments based on predefined conditions. For example, if a vendor scores below a certain threshold, the system can auto-generate follow-up actions or flag the record for review.

Plugin Dependency: Smart Response Automation \(com.sn\_smart\_resp\_auto\)

Configure response logic and manage automation settings within the Smart Assessment Engine. Rules can be configured using templates and conditions based on scoring, risk levels, or assessment responses.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Set up risk rating scales for scoring assessments and questionnaires.

</td><td>

This task is required for the initial setup of TPRM.You can configure the risk rating scale that is selected by default for all questionnaires.

For more information, see [Set up risk rating scales for scoring](../task/tprm-risk-rating-scales-config.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third-party risk domains or areas.

</td><td>

This task is required for the initial setup of TPRM.You can configure the scoring method and weight that is selected by default for all third parties associated with a specific risk area.

For more information, see [Define a third-party risk domain](../../grc-vendor-risk/task/tprm-risk-domain-define.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third-party risk area criteria, which are the group of risk domains or areas that apply to a type of third party.

</td><td>

This task is required for the initial setup of TPRM.You can adjust the weight and scoring method of each risk area within a criteria definition.

 For more information, see [Define third-party risk area criteria](../../grc-vendor-risk/task/tprm-risk-domain-criteria-df.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up third party and engagement component criteria.

</td><td>

This task is required for the initial setup of TPRM.Components are entities that can be assessed for risk. Component criteria are groups of components that are related to a particular type of third party or engagement.

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

This task is required for the initial setup of TPRM.Define the criteria, based on risk scores, that determine which third parties or engagements require assessments. Third-party risk scoring rules apply to subsidiaries, engagements, and third-party risk areas. Engagement risk scoring rules only apply to engagements.

For more information, see [Define third-party risk scoring rules](../../grc-vendor-risk/task/tprm-tp-risk-scoring-rules-define.md) and [Define engagement risk scoring rules](../../grc-vendor-risk/task/tprm-engagement-scoring-rules-df.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Create questionnaire or document request templates.

</td><td>

This task is required for the initial setup of TPRM.You can reuse questionnaire templates and document-request templates to streamline the creation of new questionnaires and document requests.

The following template purposes \(classifications\) are available.-   TPRM external 3rd-party element questionnaire
-   TPRM external 4th-party questionnaire
-   TPRM external document request
-   TPRM external questionnaire
-   TPRM internal IRQ
-   TPRM internal tiering questionnaire

For more information, see [Create a TPRM SAE questionnaire or document request template](../../grc-vendor-risk/task/create-sae-q-template.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Create assessment templates for external questionnaires.

</td><td>

This task is required for the initial setup of TPRM.You can create an assessment template with set duration requirements and questionnaires attached by default to help streamline the assessment process for different types of third parties and engagements.

 For more information, see [Create an external assessment template](../../grc-vendor-risk/task/create-vendor-risk-assess-temp.md).Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Create issue generation rules.

</td><td>

This task is optional.Set up rules that auto-generate issues for external assessments. Specify a Third-party risk assessment, a Questionnaire template, and the Questions to apply the rule to, as well as an Issue template and a Task template to use while generating it.

 For more information on setting up these rules, see [Create an issue generation rule](../../grc-vendor-risk/task/tprm-generate-issue-rule.md). Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Set up event-driven management rules.

</td><td>

This task is optional. Set up rules that auto-generate and send questionnaires and doc requests to engagements and third parties. For engagements and third parties that meet the criteria you define, you specify the schedule and the assessment templates. You can automate all request types except onboarding.

 For more information on setting up these rules, see [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md). **Note:** The Event-driven management rules feature is the default option for scheduling assessments and replaces Recurring assessments.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

</td></tr><tr><td>

Set up scoring for questionnaires.

</td><td>

This task is required for the initial setup of TPRM.You can configure how questionnaires and document requests are scored.

For more information, see [Configure scoring for an assessment](../../assessment-engine/task/configure-scoring-for-assessments.md), [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md), and[Configure normalization in assessment](../../assessment-engine/task/configure-normalization-in-assessment.md).Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr><tr><td>

Set up Unified Content Management

</td><td>

This task is optional. Install the Unified Content Management application. If you have the TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role you can access and update Smart Assessment Engine templates from the Unified Content Management page in the Vendor Management Workspace. The UCM application serves as a starter template library, providing ready-to-use SAE templates for TPRM assessments. You can view available templates, and activate or update template versions for use in TPRM assessments.

For more information, see [Managing TPRM SAE templates with Unified Content Management](../../grc-vendor-risk/concept/tprm-integrating-ucm.md) and [Activate or update Smart Assessment templates](../../grc-vendor-risk/task/activate_sae_ucm.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

</td></tr></tbody>
</table>