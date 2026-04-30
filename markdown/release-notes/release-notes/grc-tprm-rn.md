---
title: Third-party Risk Management release notes
description: The ServiceNow Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 13
---

# Third-party Risk Management release notes

The ServiceNow® Third-party Risk Management \(TPRM\) application provides a centralized process for managing your portfolio of third parties and their engagements, assessing and scoring risk, and performing remediation. TPRM was enhanced and updated in the Zurich release.

## Third-party Risk Management highlights for the Zurich release

-   Use the Document Management system in TPRM to centralize third-party documentation in a searchable repository with metadata, and versioning, access controls.
-   Use vertical navigation in the Vendor Management Workspace through a customizable panel grouped by related lists for improved access to third-party records, assessments, and performance pages.
-   Configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace.
-   Use the latest Smart Assessment Engine questionnaire templates to perform internal and external assessments.
-   Use the enhanced Digital Resilience Third-party Information Register features in the Vendor Management Workspace.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Third-party Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Third-party Risk Management to Zurich

If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings.

## New in the Zurich release

-   **[Now Assist for Third-party Risk Management \(TPRM\) release notes](now-assist-for-tprm-rn.md)**

    Review the Now Assist for Third-party Risk Management \(TPRM\) \(TPRM\) release notes for full descriptions of the features.

-   **[Document Management system in Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-dms&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

    For information on Now Assist skills for TPRM and Document Management, see [Now Assist for Third-party Risk Management \(TPRM\) release notes](now-assist-for-tprm-rn.md) and [Now Assist in Document Intelligence release notes](../analytics-intelligence-reporting/now-assist-document-intelligence-rn.md).

-   **[Register of information regulatory packages](https://www.servicenow.com/docs/access?context=tprm-dora-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can now generate regulator-ready Register of Information packages using the Plain-CSV Report Package option on the download page. The ZIP file includes metadata and report folders structured to regulator specifications, with file names containing LEI, entity ID, and release version. This format helps ensure EU DORA compliance and supports automated validation workflows. You can follow the user guide on the Download/Upload request page for suggested steps and permissions.

-   **[Validation framework for Register of Information](https://www.servicenow.com/docs/access?context=tprm-validation-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can now validate downloaded Register of Information packages using the Plain-CSV Report Package option on the download page against requirements. File format, structure, encoding, naming conventions, and field-level data are validated across multiple tables. If any validation warnings are detected, a validation report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. Validation reports include real-world field labels, rule expressions, and record identifiers. You can cross-reference validation errors using a downloadable Excel master template that mirrors the CSV structure, making it easier to locate and address issues. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data.

-   **[New sn\_vdr\_risk\_asmt.sae\_enabled property](https://www.servicenow.com/docs/access?context=tprm-properties-configure&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the new and improved Smart Assessment experience after you upgrade to version 21.0.x and set the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Smart assessments with Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-sae-using&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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

## UI changes

-   **[Vertical navigation in the Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-monitoring-tpr&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, the legacy horizontal tab-based layout in the Vendor Management Workspace has been replaced with a structured vertical navigation panel with groups of related lists, organizing access to third-party records, assessments, and performance pages in a way that supports clearer workflows and is consistently available to all internal users.

-   **[Third-party information register download option renamed to Excel master template](https://www.servicenow.com/docs/access?context=tprm-excel-upload-download-request&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, the option to download the Third-party Information Register is renamed to Excel Master Template. This change improves clarity and aligns with regulator terminology.

-   **[DPM business validation rules and properties](https://www.servicenow.com/docs/access?context=tprm-validation-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, the DPM business validation rules and report.json, reportPackage.json, FrameworkCodeModuleVersion properties are now included. These modules enable Third-party risk admins \[sn\_vdr\_risk\_asmt.vendor\_admin\] to view and maintain validation logic and configuration settings for CSV reporting and automated validation.

-   **[Choice field for ICT third-party service provider identification](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, the field **Type of code to identify the ICT third-party service provider** is now updated to be a choice field in the Digital Resilience Third-party Information Register in the contract record. This update aligns the field with regulator-defined options for selecting identification systems when creating new providers. In the Specific Information section of the contract record, the field is read-only and auto-populated based on upstream selections, such as the third-party or engagement record.

-   **Global TPRM changes**
    -   Assessments and Third-party assessments are now renamed as External assessments.
    -   Tiering assessments are now renamed as Internal assessments.
    -   The Tier-level column is now renamed as Risk rating.
    -   The Tiering assessors column is now renamed as Respondents.
    -   The **Owner** field is now renamed as **Assigned to** on the internal assessment, external assessment, tiering assessment, and due diligence request forms.
-   **[Changes made to the list view in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-ws-list-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**
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
-   **[Smart Assessment integration changes](https://www.servicenow.com/docs/access?context=tprm-sae-using&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**
    -   The Assessment engine column has been added to the Internal and External assessment list views in Vendor Management Workspace. You can track the assessment type as you transition to using the Smart Assessment Engine for all active questionnaires.
    -   The **Assessment engine** field has been added to related forms for internal risk assessments, external risk assessments, and assessment templates.
    -   The Support smart assessment column has been added to the Assessment templates and Issue generation rules list views.
    -   The original TPRM **Classification** field has been replaced with the **Purpose** field on all assessment templates.
-   **[Changes made to Digital Resilience Third-party Information Register contract records in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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


## Changed in this release

-   **[Risk areas extended to internal assessments](https://www.servicenow.com/docs/access?context=create-sae-q-template&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, if you have the third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_admin\] role, you can now configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace. Risk scores can be aggregated at the engagement level using customizable methods such as max, min, or average, and mapped to risk ratings based on business rules. Risk managers can override system-generated ratings with required justification, enabling expert judgment and helping ensure transparency in risk decisions.

-   **[Smart Assessment Engine advanced plugins](https://www.servicenow.com/docs/access?context=tprm-migrate-asmnt-sae&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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
-   **[Fourth-party assessment support in SAE](https://www.servicenow.com/docs/access?context=tprm-monitor-fourth-parties&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with version 21.1.x, Fourth-party assessments are now supported after you enable the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Enhanced contract records for Digital Resilience Third-party Information Register in Vendor Management Workspace](https://www.servicenow.com/docs/access?context=tprm-drtp-reg-contract&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\], you can now associate multiple entities with a single contract record. This association indicates that all entities have signed the contract and are providing services that are associated with the contract. You can also configure contracts that are based on the supply chain and assessment, upload contract records, and generate reports in Microsoft Excel. To better track these entities and help ensure compliance with Digital Operational Resilience Management \(DORA\) regulations, related lists have been added to the existing contract records, and existing fields have been reorganized for better usability.


## Activation information

Install Third-party Risk Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for the Vendor Management Workspace and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Operational Resilience helps organizations respond to adverse operational events by anticipating, preventing, recovering from, and adapting to such events.

-   **[Operational Resilience Workspace](https://www.servicenow.com/docs/access?context=working-in-opres-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use Operational Resilience Workspace to manage your resilience tasks and monitor resilience metrics from a single dashboard.

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce your reaction time from days to minutes.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Risk Workspace in the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for risk-related activities.

-   **[Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The ServiceNow® Smart Assessment Engine \(SAE\) application helps you to reduce the manual burden and costs of your assessment processes through automation.


-   **[Third-party Risk Management upgrade information](grc-tprm-upgrade-info.md)**  
ServiceNow® Third-party Risk Management application upgrade information for the Zurich release.

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

