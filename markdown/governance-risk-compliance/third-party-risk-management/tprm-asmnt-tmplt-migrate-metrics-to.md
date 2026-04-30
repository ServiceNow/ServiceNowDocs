---
title: Migrate a template to an SAE template
description: Migrate an existing questionnaire or document request template to a TPRM SAE questionnaire template. You must migrate all classic templates to TPRM SAE templates or create new ones before you can use SAE in TPRM.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Migrate a template to an SAE template

Migrate an existing questionnaire or document request template to a TPRM SAE questionnaire template. You must migrate all classic templates to TPRM SAE templates or create new ones before you can use SAE in TPRM.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

Before beginning the migration process, take note of the following and plan accordingly.

-   You must set the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience.

    **Warning:** After this option is enabled, this selection can’t be reversed.

    For more information, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md) and [Migrating from Classic Assessment Engine to Smart Assessment Engine](../concept/tprm-migrate-asmnt-sae.md).

-   The following question types aren’t supported: percentage, ranking, image scale, and custom metric. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.
-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.
-   When transferring TPRM SAE questionnaire templates between instances, the update set won’t include the duration information. Users must export the duration information manually from the `sn_smart_asmt_duration` table and import it into the target instances.
-   If an assessment template isn’t updated to support SAE assessments, the related tier-based, provider-based, and event-driven management rules won’t run as expected.
-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.
-   Responses from previous assessments aren’t migrated.
-   Event-driven management rules are the default option for scheduling assessments and replace Recurring assessments.

**Note:**

For more information on migration results and migration limitations, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md).

For more information on creating SAE questionnaires, see [Create a TPRM SAE questionnaire or document request template](create-sae-q-template.md).

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Questionnaire Templates** or **Document Request Templates**.

    You must set the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property before migrating templates.

2.  To migrate one questionnaire, select the questionnaire template you want and then select **Migrate**.

    You can migrate multiple questionnaires in bulk, by selecting the check box next to each questionnaire you want and then select **Migrate**.

3.  View the generated Assessment template migration record by selecting the link in the info message.

    You can view all Assessment template migration records by navigating to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Classic Template Migration**. For more information about the Classic Template Migration table and migration results, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md).

    The **Migration Status** field will update with one of the following after the migration job runs:

    -   **Completed**: The migration is completed successfully.
    -   **Partially completed**: Only some elements were successfully migrated.
    -   **Errored**: An error occurred during the migration.
4.  Navigate to the **Migration Status** of the Classic Template Migration Table to view templates that were migrated successfully or resulted in errors and correct any errors in the questionnaire template that you want to migrate.

5.  Repeat the steps until all errors are resolved and the questionnaire migrated successfully.

6.  Navigate to **Workspaces** &gt; **Vendor Management Workspace** and review the migrated questionnaire.

7.  Review and confirm all questions, sections, and scoring appear as expected by completing the following.

    1.  Identify unsupported question types.

        -   Percentage
        -   Ranking
        -   Image scale
        -   Custom metric
    2.  Convert unsupported question types.

        -   For percentage questions, use the Number type.
        -   For image scale questions, use the Radio button type.
        -   Ranking and custom metric question types aren’t supported.
    3.  Remove empty sections.

        If a section in the classic template contains only unsupported questions, an empty section is created in the new template. Templates with empty sections can’t be published.

    4.  Navigate to the **Scoring** tab and confirm that all settings appear as expected.

        For more information, see [Configure scoring for an assessment](../../assessment-engine/task/configure-scoring-for-assessments.md) and [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md).

8.  Select **Publish**.

    TPR admins can edit the questionnaire and publish it with changes.


## Result

The SAE Questionnaire Templates and SAE Document Templates related list of the original questionnaire template record is updated to include the migrated templates. For more information, see [Results of migrating a template to a TPRM SAE template](../reference/tprm-migrate-asmnt-template-result.md).

## What to do next

If you have Assessment templates, add the published SAE questionnaire template to all related assessment templates. If you have Issue generation rules, add the published SAE questionnaire template and its related questions to each related generation rule. For more information, see [Create an external assessment template](create-vendor-risk-assess-temp.md) and [Create an issue generation rule](tprm-generate-issue-rule.md).

