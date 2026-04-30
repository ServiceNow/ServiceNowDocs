---
title: Results of migrating a template to a TPRM SAE template
description: You can view the templates that were migrated to Smart Assessment format.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Results of migrating a template to a TPRM SAE template

You can view the templates that were migrated to Smart Assessment format.

## Tracking template migration

After you have started the migration process, you can view the progress and confirm if it was completed successfully. For more information on the migration process, see [Migrate a template to an SAE template](../task/tprm-asmnt-tmplt-migrate-metrics-to.md) and [Creating an assessment template from legacy assessment metric types](../../assessment-engine/concept/sae-asmnt-template-migrating.md).

## Viewing the migration results

To view your migration results, navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Classic Template Migration**. In the Assessment template migrations list, select the migration number. Each migration record for a metric type is assigned a unique number that starts with the text ATMIG. The form displays the values that were used to generate the template. The related lists display the status and content of the migrated data.

The following table describes the fields in the Assessment template migration list.

<table id="table_rqd_1cy_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number that starts with the text ATSMIG in the migration record for the questionnaire. You can use the number to search for the record.

</td></tr><tr><td>

Source metric type

</td><td>

Classic template that migrated.

</td></tr><tr><td>

Target assessment template

</td><td>

Smart Assessment template that is migrated from the source template.

</td></tr><tr><td>

Purpose

</td><td>

Purpose for the migrated template.

**Note:** Known as Template classifications in the Classic assessment engine, TPRM has a **Purpose** for each classic template classification.

TPRM purpose options include:

-   TPRM external 3rd-party element questionnaire
-   TPRM external 4th-party questionnaire
-   TPRM external document request
-   TPRM external questionnaire
-   TPRM internal IRQ
-   TPRM internal tiering questionnaire

To view a TPRM SAE questionnaire template you must have the TPR assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\]. For more information on creating assessment template purposes, see [Create an assessment template category](../../assessment-engine/task/sae-asmnt-template-category-create.md).

**Note:** You can create an assessment only from a published assessment template. You can update a published template only if no active assessment is associated with the template.

</td></tr><tr><td>

Migration status

</td><td>

Value that updates as the template migration process proceeds.-   **In progress**: Status for after you start the migration process, the process is in progress until it finishes.
-   **Completed**: The migration is completed successfully.
-   **Partially completed**: Only some elements were successfully migrated.
-   **Errored**: An error occurred during the migration.

</td></tr><tr><td>

Error details

</td><td>

Description of an error that occurred during the unsuccessful migration.

</td></tr><tr><td>

Created

</td><td>

Date and time the migration job was created.

</td></tr></tbody>
</table>## Template migration results

The following diagram shows the questionnaire to TPRM SAE template migration workflow.

![Questionnaire to SAE template migration workflow. For a text description, see the text that preceded and follows this diagram.](../image/tprm-q-to-sae-workflow.png "SAE migration workflow")

1.  Migrate templates either one by one or in bulk. After migration, all templates are in the Draft state.
2.  Review each migrated questionnaire template individually to confirm that they’re accurate and complete.
3.  Publish TPRM SAE questionnaire templates. After publishing, the following actions occur automatically:

    -   TPRM SAE templates are associated with all related Assessment templates.
    -   TPRM SAE templates are associated with all related Issue generation rules.
    **Note:** For Issue-generation rules to work as expected when applied to an TPRM SAE assessment template, at least one question must have the option, Enable preferred response, set to true.

4.  After all questionnaire templates related to an assessment template have been migrated and published, they should be marked as Supports smart assessment and ready for use.
5.  Review each assessment template to confirm it’s marked as Supports smart assessment. If an assessment template isn’t marked as Supports smart assessment, manually adding a new TPRM SAE questionnaire template to it updates its status.
6.  After a questionnaire template has been migrated and published, its related issue generation rule is automatically marked as Supports smart assessment and is ready for use.

For more information, see [Migrate a template to an SAE template](../task/tprm-asmnt-tmplt-migrate-metrics-to.md), [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md), [Create an external assessment template](../task/create-vendor-risk-assess-temp.md), and [Create an issue generation rule](../task/tprm-generate-issue-rule.md).

The following diagram shows the relationship between assessment templates and questionnaires after upgrading.

![Assessment template impact after upgrading. For a text description, see the text that preceded and follows this diagram.](../image/tprm-assess-sae-workflow.png "Assessment templates post-upgrade")

-   Before setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   Existing questionnaire templates
    -   Existing assessments
-   After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   SAE questionnaire templates \(New or migrated\).
    -   Assessments marked as Supports smart assessment.
    -   Tier-based, Provider-based, and Event-driven management rules only work with assessments marked as Supports smart assessment.

**Note:** Templates and questions must be reviewed to confirm they’re marked as Supports smart assessment. After the assessment templates and questions are marked as Supports smart assessment, issue-generation rules can be applied.

## Template migration scoring results

The Migrate scores from classic template business rule automates the migration of scores from the Classic template to the TPRM SAE template, helping ensure consistent scoring configuration. If a new template is created, you must manually enable scoring, define the correct options, and set their scores. For more information, see [Scoring assessments](../../assessment-engine/concept/scoring-in-assessments.md), [Configure scoring for an assessment](../../assessment-engine/task/configure-scoring-for-assessments.md), and [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md).

## Migration limitations

The assessment migration process has the following limitations and requirements.

-   The following question types aren’t supported: percentage, ranking, image scale, and custom metric. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.
-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.
-   When transferring TPRM SAE questionnaire templates between instances, the update set won’t include the duration information. Users must export the duration information manually from the `sn_smart_asmt_duration` table and import it into the target instances.
-   If an assessment template isn’t updated to support SAE assessments, the related tier-based, provider-based, and event-driven management rules won’t run as expected.
-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.
-   Responses from previous assessments aren’t migrated.

**Parent Topic:**[Third-party Risk Management reference](../concept/tprm-reference.md)

**Related topics**  


[How legacy metric types are migrated to sections in templates](../../assessment-engine/reference/sae-how-legacy-metrics-migrated.md)

