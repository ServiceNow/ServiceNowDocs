---
title: Migrating from Classic Assessment Engine to Smart Assessment Engine
description: Learn what changes when you migrate from the Classic Assessment Engine to the Smart Assessment Engine, including feature differences, limitations, and setup requirements. This overview can help you and your team evaluate the impact before enabling the new engine.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-10-10"
reading_time_minutes: 8
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Migrating from Classic Assessment Engine to Smart Assessment Engine

Learn what changes when you migrate from the Classic Assessment Engine to the Smart Assessment Engine, including feature differences, limitations, and setup requirements. This overview can help you and your team evaluate the impact before enabling the new engine.

## Enabling SAE in TPRM

Starting with version 21.0.x of the Third-party Risk Management application, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

## Smart Assessment Engine limitations

The TPRM SAE questionnaire template has the following limitations.

-   All new assessments must use SAE questionnaire templates.
-   Third-party risk assessors can no longer create issues from the View responses page. Issues generation rules can be used to create issues automatically.
-   Third-party risk assessors can no longer create comments on individual questions. They can only use the comment section at the questionnaire level.
-   The signature feature isn’t supported.
-   Automatic attachment of questionnaires to external assessments based on inherent risk questionnaire \(IRQ\) responses or IRQ-calculated risk tiers is currently not supported in Smart Assessment Engine.
-   The following question types aren’t supported: percentage, ranking, image scale, and custom metric. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

    **Note:** For the percentage and image scale question types, customers can use the Number type and Radio button type, respectively. Ranking and custom metric question types aren't supported. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.

    For more information on migration results, migration limitations, and creating TPRM SAE questionnaires, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md) and [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md).

-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.

    For more information, see [Configure scoring for an assessment](../../assessment-engine/task/configure-scoring-for-assessments.md) and [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md).

-   Event-driven management rules are the default option for scheduling assessments and replaces Repeating assessments.

## Plugin dependencies

After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following applications and plugins are installed automatically:

-   The Vendor Risk Management Workspace application \[sn\_vrm\_ws\] is automatically installed so you can use the Vendor Risk Management workspace where you can access SAE questionnaires and features.
-   The Smart Assessment Engine application and plugins are automatically installed enabling you to use the features of the Smart Assessment Engine for your assessments.

    Smart Assessment Engine application package that includes the following:

    -   Smart Assessment Core plugin \[com.sn\_smart\_asmt\]
    -   Smart Assessment Designer plugin \[com.sn\_smart\_asmt\_desg\]
    -   Smart Assessment Connected plugin \[com.sn\_smart\_asmt\_conn\]
    -   Smart Assessment Migration Tools plugin \[com.sn\_smart\_asmt\_mig\]
    -   Smart Assessment Dependencies plugin \[com.sn\_smart\_asmt\_dep\]
    -   Smart Assessment Post-assessment Actions plugin \[com.sn\_impact\_fwk\] and \[com.sn\_smart\_imp\_auto\]
    -   Smart Assessment Response Automation plugin \[com.sn\_smart\_resp\_auto\]
    -   Smart Assessment Scoring plugin \[com.sn\_smart\_scoring\]

**Note:** For more information on these plugins, see [Configuring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-config.md) and [Smart assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-sae-assessment-config.md).

## Migration Overview

After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, all TPRM assessments will automatically use SAE templates and automation rules \(tier-based rules, provider-based rules, event-driven rules and issue generation rules\) that support SAE only. You will be able to continue any in-flight assessment until they are completed. You will not be able to create any new assessments with classic questionnaire templates.

The following diagram shows the questionnaire to TPRM SAE template migration workflow.

![Questionnaire to TPRM SAE template migration workflow. For a text description, see the text that preceded and follows this diagram.](../image/tprm-q-to-sae-workflow.png "SAE migration workflow")

1.  Migrate templates either one by one or in bulk. After migration, all templates are in the Draft state by default.
2.  Review each migrated questionnaire template individually to confirm that they’re accurate and complete.
3.  Publish TPRM SAE questionnaire templates. After publishing, the following actions occur automatically:

    -   All the related assessment templates are updated to use the migrated questionnaire template. If all the questionnaire templates in an assessment template are published, the assessment template is automatically marked as Support smart assessment.
    -   All issue generation rules are automatically marked as Support smart assessment if their related questionnaire template is published.
    -   All automation rules \(tier-based rules, provider-based rules, event-driven rules and issue generation rules\) are automatically marked as Support smart assessment after their related assessment template is marked as Support smart assessment.
    **Note:** For Issue-generation rules to work as expected when applied to an TPRM SAE questionnaire template, at least one question must have the option, Enable preferred response, set to true.

4.  Review each assessment template to confirm it’s marked as Supports smart assessment. If an assessment template isn’t marked as Supports smart assessment, manually adding a new TPRM SAE questionnaire template to it updates its status.

For more information, see [Migrate a template to an SAE template](../task/tprm-asmnt-tmplt-migrate-metrics-to.md), [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md), [Create an external assessment template](../task/create-vendor-risk-assess-temp.md), and [Create an issue generation rule](../task/tprm-generate-issue-rule.md).

## Classic assessment engine to Smart Assessment Engine comparison

The following table shows the comparable features between the Classic assessment engine and Smart Assessment Engine.

|Classic assessment engine features|Smart assessment engine features|
|----------------------------------|--------------------------------|
|Metric Type​|Template|
|Metric Category|Section|
|Metrics|Questions|
|Additional Information​|Justification|
|Assessable Record|Scope|
|Multiple Assessable Records in one Assessment|Combined Assessments|
|Schedule and Trigger Assessments|Trigger Assessment Flow Action|
|Domain Separation|Domain Separation|
|Question Dependency|Conditional Visibility|
|Correct Answer|Preferred Answer|
|Scoring|Scoring|
|Automated response|Response Automation|

The following diagram shows the relationship between assessment templates and questionnaires after enabling SAE.

![Assessment template impact after enabling SAE. For a text description, see the text that preceded and follows this diagram.](../image/tprm-assess-sae-workflow.png "Assessment templates post-upgrade")

-   Before setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   Existing questionnaire templates
    -   Existing assessments
-   After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   SAE questionnaire templates \(New or migrated\).
    -   Assessments marked as Supports smart assessment.
    -   Tier-based, Provider-based, and Event-driven management rules only work with assessments marked as Supports smart assessment.

**Note:** All questionnaire templates must be reviewed and published. All assessment templates and automation rules must be reviewed to confirm they’re marked as Supports smart assessment.

**Related topics**  


[Smart assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-sae-assessment-config.md)

[Migrate a template to an SAE template](../task/tprm-asmnt-tmplt-migrate-metrics-to.md)

[Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md)

[How legacy metric types are migrated to sections in templates](../../assessment-engine/reference/sae-how-legacy-metrics-migrated.md)

[Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md)

[Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md)

[Add reference information to an assessment template](../../assessment-engine/task/sae-asmnt-add-reference.md)

[Scoring assessments](../../assessment-engine/concept/scoring-in-assessments.md)

[Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md)

