---
title: Smart assessments with Third-party Risk Management
description: With the integration of Smart Assessment Engine \(SAE\), TPRM now supports both the Classic assessment engine and SAE. You can create questionnaire templates and add instructions, questions, and reference information by creating templates using SAE in the Vendor Management Workspace.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Smart assessments with Third-party Risk Management

With the integration of Smart Assessment Engine \(SAE\), TPRM now supports both the Classic assessment engine and SAE. You can create questionnaire templates and add instructions, questions, and reference information by creating templates using SAE in the Vendor Management Workspace.

## SAE overview

The Smart Assessment Engine in Vendor Management Workspace enables you to create both internal and external questionnaires using configurable templates, logical grouping of questions, inline guidance, and automations.

For more information about the Smart Assessment Engine application, refer to [Exploring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-explore.md).

**Note:** To use Smart Assessment Engine, you must enable the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property. After setting this property, you can't create new assessments and questionnaire templates using the Classic assessment engine.

## Benefits of using the Smart Assessment Engine experience

The new assessment experience offers the following benefits.

-   Enhanced navigation: Use the improved navigation for a better user experience.
-   Assessment support: Conduct assessments for both internal and external parties in one standard UI. TPRM SAE questionnaire templates are extended to include additional attributes such as the risk area and the option to include previous responses, which aren’t available in the base SAE templates. TPRM SAE templates must be created directly within the Vendor Management Workspace to ensure that they include the necessary attributes and can be used for TPRM assessments.
-   Organize questions: Group questions into subsections and sections for better organization.
-   Add attachments: Attach the files directly to the individual questions.
-   Add reference information: Add reference information to a questionnaire template to help ensure that assessors and respondents can access the necessary information they need while completing a questionnaire.
-   Filter questions: Quickly identify and filter unanswered questions.
-   Auto-save for questionnaires: Save your work automatically as you complete each question within a questionnaire.
-   Standardized risk rating scale definition: Override the default risk rating scales at the template level for both internal and external assessments.
-   Assessment duration: Define the duration of an assessment when creating a questionnaire template.
-   Combine assessments: Respond to questionnaires by using the same SAE template in a single, streamlined view.
-   Risk scoring and score normalization: Standardize the risk scores for a consistent evaluation using the more flexible scoring settings available in SAE.
-   Support for the GRC and third-party portals: Internal assessment responders can use the GRC portal to access and complete internal assessments and external assessment responders can use third-party portal to complete external assessments.

## Smart Assessment Engine limitations

SAE with TPRM has the following limitations.

-   All new assessments must use SAE questionnaire templates.
-   Third-party risk assessors can no longer create issues from the View responses page. Issues generation rules can be used to create issues automatically.
-   Third-party risk assessors can no longer create comments on individual questions. They can only use the comment section at the questionnaire level.
-   The signature feature isn’t supported.
-   Automatic attachment of questionnaires to external assessments based on inherent risk questionnaire \(IRQ\) responses or IRQ-calculated risk tiers is currently not supported in Smart Assessment Engine.
-   The following question types aren’t supported: Percentage, ranking, image scale, and custom metric aren’t supported. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

    **Note:** For the percentage and image scale question types, customers can use the Number type and Radio button type, respectively. Ranking and custom metric question types aren't supported.

-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.

    For more information on migration results, migration limitations, and creating TPRM SAE questionnaires, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md) and [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md).

-   Repeating assessments aren’t supported. You can use Event-driven management rules.
-   When transferring TPRM SAE questionnaire templates between instances, the update set won’t include the duration information. Users must export the duration information manually from the `sn_smart_asmt_duration` table and import it into the target instances.
-   If an assessment template isn’t updated to support SAE assessments, the related tier-based, provider-based, and event-driven management rules won’t run as expected.
-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.

**Note:** For more information on migration results and migration limitations, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md).

## What to explore next

To learn more about configuring and using SAE with Third-party Risk Management, see:

-   [Smart assessment configuration](../../grc-vendor-risk-implementation/concept/tprm-sae-assessment-config.md)
-   [Migrating from Classic Assessment Engine to Smart Assessment Engine](tprm-migrate-asmnt-sae.md)
-   [Migrate a template to an SAE template](../task/tprm-asmnt-tmplt-migrate-metrics-to.md)
-   [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md)
-   [How legacy metric types are migrated to sections in templates](../../assessment-engine/reference/sae-how-legacy-metrics-migrated.md)
-   [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md)
-   [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md)
-   [Add reference information to an assessment template](../../assessment-engine/task/sae-asmnt-add-reference.md)
-   [Scoring assessments](../../assessment-engine/concept/scoring-in-assessments.md)
-   [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md)

