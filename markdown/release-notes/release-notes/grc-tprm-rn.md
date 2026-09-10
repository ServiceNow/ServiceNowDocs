---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.ServiceNow Third-party Risk Management application upgrade information for the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-05-22"
reading_time_minutes: 21
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

## About Third-party Risk Management

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

Starting with Australia Patch 5, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   Reduce manual data entry by using AI to pre‑fill questionnaires for third-party contacts and business owners.
-   Use updated Standardized Information Gathering \(SIG\) questionnaire content for 2026.
-   Automate Software Bill of Materials \(SBOM\) collection, integration, and vulnerability correlation with Unified Security Exposure Management \(USEM\) integration.
-   Manage SAE assessment template versions to prevent changes from affecting in‑flight assessments.
-   Add question-level comments and follow-up capabilities during SAE reviews.
-   Maintain DORA Register of Information accuracy with automatic supply chain cascading updates and duplicate record detection for contractual arrangement and supply chain tables.
-   Validate Legal Entity Identifier \(LEI\) codes against the GLEIF database during Register of Information reporting to identify format errors, checksum failures, and inactive or unissued entities.

-   Enhance DORA Register of Information reporting with optional currency conversion and third‑party expense aggregation to generate consistent, regulator‑ready reports.
-   Review the simplified third‑party elements process in the due diligence workflow.
-   Access the unified content management module in the Vendor Management Workspace to view a centralized library of smart assessment templates.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

Review the updated AI experience with three licensing tiers.

See [Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md) for more information.

[Early availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-all-other-fixes.md)

Use generative AI to recommend TPRM issues for reviewer validation.

## Activation and other requirements

**Note:** Third-party Risk Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don't run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

    After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) is set to the default assessment engine and replaces the legacy experience. The transition is irreversible.

    **Warning:** Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so can result in unexpected issues.

    For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-tprm-rn.md).

    For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content. Update any customizations that reference the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

    After upgrading to version 22.3.3, the `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles. During upgrade, most users are automatically migrated to new feature‑specific roles. Users with custom role combinations may not be migrated automatically and require manual review before the grace period ends.


## Accessibility and localization

-   **Accessibility information**

    The Vendor Management Workspace and the third-party portal include accessibility improvements in this release, including improved color contrast, enhanced focus indicators, skip navigation links, and full keyboard navigation.

-   **Localization information**

    Third-party portal strings are externalized and translated for supported languages. Newly introduced features may have incomplete translations.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

## Third-party Risk Management upgrade information

ServiceNow® Third-party Risk Management application upgrade information for the Australia release.

### Important information for upgrading Third-party Risk Management to Australia

After upgrading to Zurich, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience to ensure consistency, scalability, and innovation moving forward. While this transition isn’t reversible, it empowers customers to future-proof their assessment strategy with an engine built to evolve with emerging needs.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

### Plugin dependencies

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

**Note:** For more information on these plugins, see [Configuring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine-cf-config.md) and [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sae-assessment-config.md).

### Migrating to Smart Assessment Engine

After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, all TPRM assessments will automatically use SAE templates and automation rules \(tier-based rules, provider-based rules, event-driven rules and issue generation rules\) that support SAE only. You will be able to continue any in-flight assessment until they are completed. You will not be able to create any new assessments with classic questionnaire templates.

The following diagram shows the questionnaire to TPRM SAE template migration workflow.

\[Omitted image "tprm-q-to-sae-workflow.png"\] Alt text: Questionnaire to TPRM SAE template migration workflow. For a text description, see the text that preceded and follows this diagram.

1.  Migrate templates either one by one or in bulk. After migration, all templates are in the Draft state by default.
2.  Review each migrated questionnaire template individually to confirm that they’re accurate and complete.
3.  Publish TPRM SAE questionnaire templates. After publishing, the following actions occur automatically:

    -   All the related assessment templates are updated to use the migrated questionnaire template. If all the questionnaire templates in an assessment template are published, the assessment template is automatically marked as Support smart assessment.
    -   All issue generation rules are automatically marked as Support smart assessment if their related questionnaire template is published.
    -   All automation rules \(tier-based rules, provider-based rules, event-driven rules and issue generation rules\) are automatically marked as Support smart assessment after their related assessment template is marked as Support smart assessment.
    **Note:** For Issue-generation rules to work as expected when applied to an TPRM SAE questionnaire template, at least one question must have the option, Enable preferred response, set to true.

4.  Review each assessment template to confirm it’s marked as Supports smart assessment. If an assessment template isn’t marked as Supports smart assessment, manually adding a new TPRM SAE questionnaire template to it updates its status.

For more information, see [Migrate a template to an SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-asmnt-tmplt-migrate-metrics-to.md), [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sae-q-template.md), [Create an external assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-vendor-risk-assess-temp.md), and [Create an issue generation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-generate-issue-rule.md).

### Classic assessment engine to Smart Assessment Engine comparison

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

\[Omitted image "tprm-assess-sae-workflow.png"\] Alt text: Assessment template impact after upgrading. For a text description, see the text that preceded and follows this diagram.

-   Before setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   Existing questionnaire templates
    -   Existing assessments
-   After setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property, the following are used by default.
    -   SAE questionnaire templates \(New or migrated\).
    -   Assessments marked as Supports smart assessment.
    -   Tier-based, Provider-based, and Event-driven management rules only work with assessments marked as Supports smart assessment.

**Note:** All questionnaire templates must be reviewed and published. All assessment templates and automation rules must be reviewed to confirm they’re marked as Supports smart assessment.

### Smart Assessment Engine limitations

The TPRM SAE questionnaire template has the following limitations.

-   All new assessments must use SAE questionnaire templates.
-   Third-party risk assessors can no longer create issues from the View responses page. Issues generation rules can be used to create issues automatically.
-   The signature feature isn’t supported.
-   Automatic attachment of questionnaires to external assessments based on inherent risk questionnaire \(IRQ\) responses or IRQ-calculated risk tiers is currently not supported in Smart Assessment Engine.
-   The following question types aren’t supported: percentage, ranking, image scale, and custom metric. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

    **Note:** For the percentage and image scale question types, customers can use the Number type and Radio button type, respectively. Ranking and custom metric question types aren't supported. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.

    For more information on migration results, migration limitations, and creating TPRM SAE questionnaires, see [Results of migrating a template to a TPRM SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-migrate-asmnt-template-result.md) and [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-sae-q-template.md).

-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.

    For more information, see [Configure scoring for an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-scoring-for-assessments.md) and [Normalization in assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/normalization-in-assessment.md).

-   Event-driven management rules are the default option for scheduling assessments and replaces Repeating assessments.

### External assessment status changes when enabling SAE

When you enable the Smart Assessment Engine \(SAE\) after upgrading to Zurich, external assessment statuses change to reflect the SAE lifecycle. The following table shows how Classic engine assessment statuses map to SAE assessment statuses.

|Classic engine status|SAE status \(Zurich and later\)|
|---------------------|-------------------------------|
|**Responses received**|**Submitted to third party**|
|**Returned**|**In progress**|

These status changes apply only when SAE is enabled. Assessments that continue to use the Classic engine retain the original states. For more information about the SAE assessment and questionnaire lifecycle, see [External assessment lifecycle states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-external-assessment-lifecycle.md).

### Important information for upgrading Vendor Risk Management to Australia

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

### Plugin requirements

TPRM

-   Activate the Third-party Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Third-party Risk Due Diligence application \[com.sn\_tprm\_dd\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

VRM

-   Activate the Vendor Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

For more information on licensing or metering, see [Tracking a managed activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-managed-activity.md), [Third-party Risk Management \(TPRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1431058), and [Vendor Risk Management \(VRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1362674).

### VRM to TPRM changes

-   The name of the application changed from Vendor Risk Management to Third-party Risk Management as part of the Vancouver release.
-   The internal assessment \[sn\_vdr\_asmt\_internal\_assessment\] table is introduced, extending the tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] table.
-   The Due Diligence Review \(DDR\) workflow is introduced, which uses both the internal assessment and the external \(VRA\) assessment.

    **Note:** If you have customizations on the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables, they might need modifications to work with the DDR workflow.

-   The Third-party Scores \[sn\_vdr\_risk\_asmt\_security\_score\] table has been relabeled to Risk Intelligence Scores \[sn\_vdr\_risk\_asmt\_security\_score\] to reduce confusion.
-   All instances of “vendor” are changed to “third party” in the user interface, though some global instances might remain unchanged.

    **Note:** If you don’t want to use the due diligence workflow, your original workflow \(Tiering assessment and External assessments \(VRAs\) should be the same\).


### VRM and TPRM data model

The Vendor Risk Management data model primarily uses the term “vendor” and includes the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables.

The Third-party Risk Management data model uses the term “third-party” in most user interface elements and introduces the DDR workflow, which uses both internal \[sn\_vdr\_asmt\_internal\_assessment\] and \[sn\_vdr\_risk\_asmt\_assessment\] external assessments.

The following models show VRM's and TPRM's capabilities.

\[Omitted image "vrm-data-model.png"\] Alt text: Relationship Vendor risk management main tables. For a text description, see the text that preceded and follows this data model.

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

\[Omitted image "tprm-data-model-upgrade.png"\] Alt text: Relationship between due diligence, and third-party management main tables. For a text description, see the text that preceded and follows this data model.

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

## September 2026

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's deprecated or removed

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## August 2026

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's changed

-   **[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)**

    Starting with Australia Patch 5, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


## July 2026

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's new

-   **[Extended AI model support for Now Assist for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/supporting-information-now-assist-tprm.md)**

    After upgrading to version 22.3.4, ServiceNow Otto for Third-party Risk Management \(TPRM\) supports Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models in addition to previously supported models. Model availability depends on your ServiceNow Otto for Third-party Risk Management \(TPRM\) subscription, providing greater flexibility when selecting the AI model that meets your requirements.


### What's changed

-   **[Default AI model for issue recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/supporting-information-now-assist-tprm.md)**

    After upgrading to version 22.3.4, the issue recommendation skill in ServiceNow Otto for Third-party Risk Management \(TPRM\) uses Azure OpenAI gpt-4-5-mini as the default model. This update changes the default model for issue recommendations. You can select alternative models, including the newly supported Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini, based on your requirements.

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## June 2026

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's new

-   **[AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-dms-sae.md)**

    After upgrading to version 22.3.3 and activating the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use uploaded documents and responses from previous assessments to generate suggested questionnaire responses with source citations. For internal assessments, the snc\_internal role is required. For external assessments, primary contacts can complete all assessment response actions; secondary contacts must be assigned read and write access.

-   **[Software Bill of Materials \(SBOM\) support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sbom-exploring.md)**

    After upgrading to version 22.3.2 and installing the required SBOM applications, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or third-party risk assessor role \[sn\_vdr\_risk\_asmt.vendor\_risk\_assessor\], you can collect and manage SBOM data to support regulatory disclosure requirements.

-   **[Standardized Information Gathering \(SIG\) 2026 questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sig-use-and-support.md)**

    After upgrading to version 22.3.0, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can use updated SIG Full, SIG Core, and SIG Lite templates for 2026 with expanded coverage across major security and privacy frameworks. Existing SIG questionnaire versions remain available. In‑flight assessments aren't affected.

-   **[Smart Assessment template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sae-using.md)**

    After upgrading to version 22.3.3, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can manage SAE template lifecycles using explicit versioning so that in-flight assessments use the version that was active when they were created.

-   **[Legal Entity Identifier \(LEI\) validation for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-valid-lei.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, if you have the third-party risk manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\], you can validate Legal Entity Identifier codes against the GLEIF database to support regulatory accuracy in Register of Information reporting. For descriptions of validation results and report columns, see [Level 4 LEI Validation Report columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-lei-validation-report.md).


### What's changed

-   **[Improved handling of skipped conditional questions in SAE assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-sae-using.md)**

    After upgrading to version 22.3.3, Smart Assessment Engine assessments hide conditional questions that are skipped based on response logic. Sections that contain skipped questions are visually de‑emphasized, and assessments render in a continuous scroll layout.This change affects the assessment review experience only and does not change assessment logic, scoring, or response data.

-   **[Comments field in the third‑party portal saves when you leave the field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.2, the comments field in the third‑party portal saves when you leave the field rather than on every keystroke.

-   **[Issue indicators in the third-party portal shown only after submission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.2, issue indicators appear in the third‑party portal only after an issue is submitted to the third party and the **Visible in third‑party portal** field is selected. Previously, indicators were visible before submission when the field was selected.


-   **[Consolidated assessment email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set_sys_props_for_email.md)**

    After upgrading to version 22.3.3, external assessment‑related email notifications are sent as a single consolidated summary instead of individual per‑event messages. Users can configure notification frequency, detail level, and delivery channel in their notification preferences. Multi‑language templates are available.

-   **[Assessment count mechanism updated in the third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/vendor-portal.md)**

    After upgrading to version 22.3.3, engagement assessment counts in the third-party portal include only active, pending, and in‑progress assessments. Previously, counts included inactive and canceled assessments.

-   **[Inactive metrics excluded when copying assessment responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-assessing-tpr.md)**

    After upgrading to version 22.3.3, inactive and retired metrics are excluded when copying responses between assessments. Previously, copying responses could include inactive metrics, causing scoring errors.

-   **[Type of ICT services changes cascade to supply chain in DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, when the Type of ICT services value is updated on a Contractual Arrangements – Specific Information \(B.02.02\) record, the ICT service supply chain \(B.05.02\) is now updated automatically. If a Type of ICT services value is removed from a Specific Information record, the corresponding supply chain records for Rank 1 and higher ranks are also deleted automatically. Previously, Rank 1 supply chain records were generated when the Specific Information record was first created, but subsequent changes or removals did not propagate to the supply chain, requiring manual correction.

-   **[Duplicate contractual arrangements detected and warned in DORA Register of Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, duplicate records in the Contractual Arrangements – Specific Information \(B.02.02\) table are now detected and handled across three scenarios. When saving a contractual arrangement from the UI, a business rule checks eight composite key fields and blocks the save if a duplicate is found. During Excel upload, duplicate rows are rejected and logged to the upload error report. During CSV package download, duplicate rows in B.02.02 are flagged in the DORA request record's error log; duplicates are warned but not removed from the generated CSV.

-   **[Duplicate supply chain rows warned during DORA CSV package download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-drtp-roi-packages.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.3.1, during CSV package download, duplicate rows in the ICT service supply chains \(B.05.02\) table are now detected and a warning is added to the request record. This applies to both Rank 1 supply chain records, which are auto-generated from Specific Information records, and higher-ranked records. Additionally, when the Storage of data field is set to No on a contractual arrangement, associated location field values are now cleared automatically.


### What's deprecated or removed

-   The `grc_business_user` and `grc_reader` roles are no longer directly inherited by TPRM roles.
-   The `scoring_rule` and `scoring_rule_ref` fields are removed from assessment forms and UI sections. Custom scripts or integrations that reference these fields must be updated.

## April 2026

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's new

-   **[Generate issue recommendations for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-recommendation-tprm-issue.md)**

    After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the ServiceNow Otto for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


### What's changed

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Australia

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk and performing remediation. TPRM was enhanced and updated in the Australia release.

### What's new

-   **[Generate aggregate regulatory reports in local currencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-dora-currency-aggregation.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-integrating-ucm.md)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


### What's changed

-   **[Fields added to Create New Excel download/upload request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-create-report-aggregate-expenses.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, the **Enable currency conversion** and **Enable third‑party total expense aggregation** fields are available on the Excel download/upload request page. When creating Excel Master Template or Plain‑CSV Reporting Package requests, you can configure these options directly on the form.

-   **[TPRM Unified content management page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-ws-ucm-page.md)**

    After upgrading to version 22.0.2 and installing the Unified Content Management application, the unified content management module is available in the Vendor Management Workspace.


-   **[Simplified third-party element process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tprm-workflow-in-workspace.md)**

    After upgrading to version 22.0.1, third‑party elements are now linked to a single third party and can no longer be shared across third parties. Scoring rollups calculate results from element‑level assessments rather than entity records.


### What's deprecated or removed

-   Assessments using entities are no longer supported.

