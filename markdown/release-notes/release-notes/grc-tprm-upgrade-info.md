---
title: Third-party Risk Management upgrade information
description: ServiceNow Third-party Risk Management application upgrade information for the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Third-party Risk Management upgrade information

ServiceNow® Third-party Risk Management application upgrade information for the Australia release.

## Important information for upgrading Third-party Risk Management to Australia

After upgrading to Zurich, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience to ensure consistency, scalability, and innovation moving forward. While this transition isn’t reversible, it empowers customers to future-proof their assessment strategy with an engine built to evolve with emerging needs.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

## Plugin dependencies

After upgrading to Zurich and setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following applications and plugins are installed automatically:

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

**Note:** For more information on these plugins, see [Configuring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-assessment-engine-cf-config.md) and [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-assessment-config.md).

## Migrating to Smart Assessment Engine

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

For more information, see [Migrate a template to an SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-asmnt-tmplt-migrate-metrics-to.md), [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-sae-q-template.md), [Create an external assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-vendor-risk-assess-temp.md), and [Create an issue generation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-generate-issue-rule.md).

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

The following diagram shows the relationship between assessment templates and questionnaires after upgrading.

![Assessment template impact after upgrading. For a text description, see the text that preceded and follows this diagram.](../image/tprm-assess-sae-workflow.png "Assessment templates post-upgrade")

-   Before setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   Existing questionnaire templates
    -   Existing assessments
-   After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   SAE questionnaire templates \(New or migrated\).
    -   Assessments marked as Supports smart assessment.
    -   Tier-based, Provider-based, and Event-driven management rules only work with assessments marked as Supports smart assessment.

**Note:** All questionnaire templates must be reviewed and published. All assessment templates and automation rules must be reviewed to confirm they’re marked as Supports smart assessment.

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

    For more information on migration results, migration limitations, and creating TPRM SAE questionnaires, see [Results of migrating a template to a TPRM SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-migrate-asmnt-template-result.md) and [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-sae-q-template.md).

-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.

    For more information, see [Configure scoring for an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-scoring-for-assessments.md) and [Normalization in assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/normalization-in-assessment.md).

-   Event-driven management rules are the default option for scheduling assessments and replaces Repeating assessments.

## Important information for upgrading Vendor Risk Management to Australia

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

## Plugin requirements

TPRM

-   Activate the Third-party Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Third-party Risk Due Diligence application \[com.sn\_tprm\_dd\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

VRM

-   Activate the Vendor Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

For more information on licensing or metering, see [Tracking a managed activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-managed-activity.md), [Third-party Risk Management \(TPRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1431058), and [Vendor Risk Management \(VRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1362674).

## VRM to TPRM changes

-   The name of the application changed from Vendor Risk Management to Third-party Risk Management as part of the Vancouver release.
-   The internal assessment \[sn\_vdr\_asmt\_internal\_assessment\] table is introduced, extending the tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] table.
-   The Due Diligence Review \(DDR\) workflow is introduced, which uses both the internal assessment and the external \(VRA\) assessment.

    **Note:** If you have customizations on the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables, they might need modifications to work with the DDR workflow.

-   The Third-party Scores \[sn\_vdr\_risk\_asmt\_security\_score\] table has been relabeled to Risk Intelligence Scores \[sn\_vdr\_risk\_asmt\_security\_score\] to reduce confusion.
-   All instances of “vendor” are changed to “third party” in the user interface, though some global instances might remain unchanged.

    **Note:** If you don’t want to use the due diligence workflow, your original workflow \(Tiering assessment and External assessments \(VRAs\) should be the same\).


## VRM and TPRM data model

The Vendor Risk Management data model primarily uses the term “vendor” and includes the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables.

The Third-party Risk Management data model uses the term “third-party” in most user interface elements and introduces the DDR workflow, which uses both internal \[sn\_vdr\_asmt\_internal\_assessment\] and \[sn\_vdr\_risk\_asmt\_assessment\] external assessments.

The following models show VRM's and TPRM's capabilities.

![Relationship Vendor risk management main tables. For a text description, see the text that preceded and follows this data model.](../image/vrm-data-model.png "VRM data model")

The components included in the Vendor Risk Management data model are as follows:

-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Company \[core\_company\]
-   Vendor risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Vendor engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

![Relationship between due diligence, and third-party management main tables. For a text description, see the text that preceded and follows this data model.](../image/tprm-data-model-upgrade.png "TPRM data model")

The components included in the Third-party Risk Management data model are as follows:

-   Risk intelligence score \[sn\_vdr\_risk\_asmt\_security \_score\]
-   Internal assessment \[sn\_vdr\_asmt\_internal\_assessment\]
-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Event-driven management history \[sn\_tprm\_dd\_rule\_execution\_history\]
-   Third-party due diligence request \[sn\_tprm\_dd\_request\]
-   Company \[core\_company\]
-   Event-driven management rule \[sn\_tprm\_dd\_generation\_rule\]
-   Third-party risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Third-party engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Third-party risk issue \[sn\_vdr\_risk\_asmt\_issue\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

**Parent Topic:**[Third-party Risk Management release notes](grc-tprm-rn.md)

