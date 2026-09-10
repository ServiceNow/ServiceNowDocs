---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.ServiceNow Third-party Risk Management application upgrade information for the Zurich release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 22
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.

## About Third-party Risk Management

-   Use the Document Management system in TPRM to centralize third-party documentation in a searchable repository with metadata, and versioning, access controls.
-   Use vertical navigation in the Vendor Management Workspace through a customizable panel grouped by related lists for improved access to third-party records, assessments, and performance pages.
-   Configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace.
-   Use the latest Smart Assessment Engine questionnaire templates to perform internal and external assessments.
-   Use the enhanced Digital Resilience Third-party Information Register features in the Vendor Management Workspace.

See [Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md) for more information.

## Activation and other requirements

**Important:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

    After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

    **Warning:**

    Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

    For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/grc-tprm-rn.md).

    For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

    The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings.


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for the Vendor Management Workspace and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/grc-rn-landing.md)

## Third-party Risk Management upgrade information

ServiceNow® Third-party Risk Management application upgrade information for the Zurich release.

### Important information for upgrading Third-party Risk Management to Zurich

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

**Note:** For more information on these plugins, see [Configuring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/smart-assessment-engine-cf-config.md) and [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-sae-assessment-config.md).

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

For more information, see [Migrate a template to an SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-asmnt-tmplt-migrate-metrics-to.md), [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-sae-q-template.md), [Create an external assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-vendor-risk-assess-temp.md), and [Create an issue generation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-generate-issue-rule.md).

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
-   Third-party risk assessors can no longer create comments on individual questions. They can only use the comment section at the questionnaire level.
-   The signature feature isn’t supported.
-   Automatic attachment of questionnaires to external assessments based on inherent risk questionnaire \(IRQ\) responses or IRQ-calculated risk tiers is currently not supported in Smart Assessment Engine.
-   The following question types aren’t supported: percentage, ranking, image scale, and custom metric. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

    **Note:** For the percentage and image scale question types, customers can use the Number type and Radio button type, respectively. Ranking and custom metric question types aren't supported. You must either convert these question types to supported formats before migration or create new questions in the template designer after migration.

-   If a section in the classic template contains only unsupported questions, an empty section is created in the TPRM SAE template. TPRM SAE templates with empty sections can’t be published; therefore, you must either add replacement questions to these sections or delete the empty sections before publishing.

    For more information on migration results, migration limitations, and creating TPRM SAE questionnaires, see [Results of migrating a template to a TPRM SAE template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-migrate-asmnt-template-result.md) and [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-sae-q-template.md).

-   The TPRM scoring migration proceeds only if there were no errors during the template migration. If there were errors, the TPRM scoring migration doesn’t occur.

    For more information, see [Configure scoring for an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configure-scoring-for-assessments.md) and [Normalization in assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/normalization-in-assessment.md).

-   Event-driven management rules are the default option for scheduling assessments and replaces Repeating assessments.

### External assessment status changes when enabling SAE

When you enable the Smart Assessment Engine \(SAE\) after upgrading to Zurich, external assessment statuses change to reflect the SAE lifecycle. The following table shows how Classic engine assessment statuses map to SAE assessment statuses.

|Classic engine status|SAE status \(Zurich and later\)|
|---------------------|-------------------------------|
|**Responses received**|**Submitted to third party**|
|**Returned**|**In progress**|

These status changes apply only when SAE is enabled. Assessments that continue to use the Classic engine retain the original states. For more information about the SAE assessment and questionnaire lifecycle, see [External assessment lifecycle states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-external-assessment-lifecycle.md).

### Important information for upgrading Vendor Risk Management to Zurich

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

### Plugin requirements

TPRM

-   Activate the Third-party Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Third-party Risk Due Diligence application \[com.sn\_tprm\_dd\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

VRM

-   Activate the Vendor Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

For more information on licensing or metering, see [Tracking a managed activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-managed-activity.md), [Third-party Risk Management \(TPRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1431058), and [Vendor Risk Management \(VRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1362674).

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

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.

### What's deprecated or removed

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## December 2025

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.

### What's new

-   **[ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes]()**

    Review the ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes for full descriptions of the features.

-   **[Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-dms.md)**

    Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

    For information on Now Assist skills for TPRM and Document Management, see [ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes]() and [Now Assist in Document Intelligence release notes]().

-   **[Register of information regulatory packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-dora-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can now generate regulator-ready Register of Information packages using the Plain-CSV Report Package option on the download page. The ZIP file includes metadata and report folders structured to regulator specifications, with file names containing LEI, entity ID, and release version. This format helps ensure EU DORA compliance and supports automated validation workflows. You can follow the user guide on the Download/Upload request page for suggested steps and permissions.

-   **[Validation framework for Register of Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-validation-roi.md)**

    After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can now validate downloaded Register of Information packages using the Plain-CSV Report Package option on the download page against requirements. File format, structure, encoding, naming conventions, and field-level data are validated across multiple tables. If any validation warnings are detected, a validation report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. Validation reports include real-world field labels, rule expressions, and record identifiers. You can cross-reference validation errors using a downloadable Excel master template that mirrors the CSV structure, making it easier to locate and address issues. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data.


### What's changed

-   **[Vertical navigation in the Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-monitoring-tpr.md)**

    Starting with version 21.1.x, the legacy horizontal tab-based layout in the Vendor Management Workspace has been replaced with a structured vertical navigation panel with groups of related lists, organizing access to third-party records, assessments, and performance pages in a way that supports clearer workflows and is consistently available to all internal users.

-   **[Third-party information register download option renamed to Excel master template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-excel-upload-download-request.md)**

    Starting with version 21.1.x, the option to download the Third-party Information Register is renamed to Excel Master Template. This change improves clarity and aligns with regulator terminology.

-   **[DPM business validation rules and properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-validation-roi.md)**

    Starting with version 21.1.x, the DPM business validation rules and report.json, reportPackage.json, FrameworkCodeModuleVersion properties are now included. These modules enable Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] to view and maintain validation logic and configuration settings for CSV reporting and automated validation.

-   **[Choice field for ICT third-party service provider identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    Starting with version 21.1.x, the field **Type of code to identify the ICT third-party service provider** is now updated to be a choice field in the Digital Resilience Third-party Information Register in the contract record. This update aligns the field with regulator-defined options for selecting identification systems when creating new providers. In the Specific Information section of the contract record, the field is read-only and auto-populated based on upstream selections, such as the third-party or engagement record.


-   **[Risk areas extended to internal assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-sae-q-template.md)**

    Starting with version 21.1.x, if you have the third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_admin\] role, you can now configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace. Risk scores can be aggregated at the engagement level using customizable methods such as max, min, or average, and mapped to risk ratings based on business rules. Risk managers can override system-generated ratings with required justification, enabling expert judgment and helping ensure transparency in risk decisions.

-   **[Smart Assessment Engine advanced plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-migrate-asmnt-sae.md)**

    Starting with version 21.1.x, the following Smart Assessment Engine advanced plugins are automatically installed: Post Assessment Actions for Smart Assessments \[com.sn\_smart\_imp\_auto and com.sn\_impact\_fwk\] and Advanced Response Automation for Smart assessments \[sn\_smart\_resp\_auto\]. The Post Assessment Actions for Smart Assessments plugin lets Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] automate follow-up tasks, like notifications or workflow launches, after an assessment is completed. The Advanced Response Automation for Smart Assessments plugin automatically fills in assessment responses based on prior data or logic, streamlining and standardizing the assessment process.

-   **Feature-specific administrator role enhancements**

    Starting with version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

    -   Assign sn\_vdr\_risk\_asmt.vendor\_risk\_admin to users who need to configure and manage vendor risk features.
    -   Assign sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer to users who perform assessments, manage dashboards, and require operational access.
    -   Assign sn\_vdr\_risk\_asmt.external\_assessment\_responder to users who need access to the third-party portal and to complete assessments.

        **Note:** Administrator privileges no longer grant access to TPRM features. Users must be assigned an appropriate feature-specific role to access relevant functionality.

-   **Read-only field enhancements**

    Starting with version 21.1.x, the following Third-party Risk Management plugins have security enhancements for read-only fields in this release:

    -   Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\]
    -   Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\]
    -   GRC: Vendor Portal \[com.sn\_grc\_vendor\_portal\]
    -   GRC: Profiles \[com.sn\_grc\]
    -   GRC: Compliance Assessment \[com.sn\_comp\_asmt\]
    -   GRC: SIG Questionnaire Integration \[com.sn\_sig\_asmt\]
    -   GRC: Performance Analytics Premium Integration \[com.sn\_grc\_pa\]
    -   Vendor Risk Management integration with EcoVadis \[com.sn\_app\_grc\_ecovadis\]
    -   ITAM applications \[com.snc.vendor\_core\]
-   **[Fourth-party assessment support in SAE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-monitor-fourth-parties.md)**

    Starting with version 21.1.x, Fourth-party assessments are now supported after you enable the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.


## Zurich

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.

### What's new

-   **[New sn\_vdr\_risk\_asmt.sae\_enabled property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-properties-configure.md)**

    Use the new and improved Smart Assessment experience after you upgrade to version 21.0.x and set the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Smart assessments with Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-sae-using.md)**

    Create Smart Assessment Engine assessments for your organization:

    -   Enhanced navigation: Use the improved navigation for a better user experience.
    -   Assessment support: Conduct assessments for both internal and external parties. TPRM questionnaire templates include additional attributes such as the risk area and the option to include previous responses, which aren’t available in SAE. TPRM templates must be created directly within the Vendor Management Workspace to ensure that they include the necessary attributes.
    -   Organize questions: Group questions into subsections for better organization.
    -   Add attachments: Attach the files directly to the individual questions.
    -   Add reference information: Add reference information to a questionnaire template to help ensure that assessors can access the information they need while responding.
    -   Filter questions: Quickly identify and filter unanswered questions.
    -   Auto-save for questionnaires: Auto-save each question automatically after changes are made to them.
    -   Standardized risk rating scale definition: Define the risk rating scales at the template level for both internal and external assessments.
    -   Assessment duration: Define the duration of an assessment when creating a questionnaire template.
    -   Combine assessments: Respond to questionnaires by using the same SAE template in a single, streamlined view.
    -   Bulk template migration: Migrate classic templates in bulk to the Smart Assessment format. To ensure the templates work correctly in TPRM, you must migrate them by using the Third-party Risk Management application.
    -   Risk score normalization: Standardize the risk scores for a consistent evaluation.
    -   Support for the GRC and third-party portals: Use the GRC portal to access and complete internal assessments and the third-party portal to complete external assessments.

### What's changed

-   **Global TPRM changes**
    -   Assessments and Third-party assessments are now renamed as External assessments.
    -   Tiering assessments are now renamed as Internal assessments.
    -   The Tier-level column is now renamed as Risk rating.
    -   The Tiering assessors column is now renamed as Respondents.
    -   The **Owner** field is now renamed as **Assigned to** on the internal assessment, external assessment, tiering assessment, and due diligence request forms.
-   **[Changes made to the list view in Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-ws-list-page.md)**
    -   The Assessment setup section has been added. From this section, you can create assessment templates, Smart Assessment questionnaire templates, and issue generation rules.
    -   The Questionnaire requests section has been added.
    -   The Tiering assessments and Inherent risk questionnaires \(IRQ\) are combined in the Internal assessments section.
-   **Changes made to internal assessment pages**
    -   Tier-level scales are renamed as Scales.
    -   Tiering assessment schedule and Schedules are combined and renamed as Assessment schedule.
-   **Changes made to assessment related lists**
    -   Assessment instances is renamed as Questionnaire requests.
    -   Questionnaires is renamed as Questionnaire templates.
    -   Document requests is renamed as Document templates.
    -   Fourth-party questionnaires is renamed as Fourth-party templates.
    -   Repeating assessments is renamed as Assessment scheduling.
-   **[Smart Assessment integration changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-sae-using.md)**
    -   The Assessment engine column has been added to the Internal and External assessment list views in Vendor Management Workspace. You can track the assessment type as you transition to using the Smart Assessment Engine for all active questionnaires.
    -   The **Assessment engine** field has been added to related forms for internal risk assessments, external risk assessments, and assessment templates.
    -   The Support smart assessment column has been added to the Assessment templates and Issue generation rules list views.
    -   The original TPRM **Classification** field has been replaced with the **Purpose** field on all assessment templates.
    -   The external assessment status **Responses received** is now **Submitted to third party** when SAE is enabled.
    -   The external assessment status **Returned** is now **In progress** when SAE is enabled.
-   **[Changes made to Digital Resilience Third-party Information Register contract records in Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    The General info related list has now been renamed as Details and the following related lists have been added:

    -   Entities signing contract to use service
    -   Entities making use of services
    -   Entities providing services
    -   Third parties signing contract to provide services
    -   Third-party engagements signing contract
    -   ICT service supply chains
    -   Assessments of the ICT services
-   **Coral theme**

    Coral is now the default theme for Vendor Management Workspace, portal, and mobile experiences. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

    **Note:** When you're upgrading from Xanadu or Yokohama to Zurich with version 20.1.x of the GRC: Vendor Portal, the application UI themes might not match. The Vendor Management Workspace uses the Polaris theme by default, and the Third-party portal uses the Coral theme by default. Upgrading to Xanadu or Yokohama with version 20.1.x of the GRC: Vendor Portal results in both the Vendor Management Workspace and Third-party portal using the Polaris theme. Upgrading to version 21.x or higher results in both the Vendor Management Workspace and Third-party portal using the Coral UI theme.


-   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/tprm-drtp-reg-contract.md)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


