---
title: Operational Sustainability Management release notes
description: Version history for the Operational Sustainability Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-env-social-corporate-governance.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Operational Sustainability Management release notes

Version history for the Operational Sustainability Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Feature roles and functional domain separation — Product roles have been restructured with modified role inheritance and licensing role exclusions, enabling cleaner role management and functional domain separation in ESG.
        -   Consolidation of O365 and Document Designer add-ins — The Office 365 reporting and Document Designer add-ins have been consolidated into a single unified Document Designer plugin with updated manifest and business domain support.
    -   Changed:
        -   Restricted AI emission calculation guidelines access — Read access to the emission calculation guidelines table is now restricted to the cmd\_agent\_user role only.
        -   GRC confidentiality user access review — Assessed and updated read access of the GRC confidentiality user role on the Portfolio Management Goal Framework table.
        -   This release includes security enhancements that strengthen access controls across the application.
        -   Business domain update script — Added a script to update business domain references for uptaking teams.
        -   Demo data corrections — Corrected demo data to align with updated role and domain separation changes.
    -   Fixed:
        -   Metric picker performance — Resolved slow loading of the metric picker when adding Metric to Target relationships via related lists.
        -   Analytics dashboard drill-downs — Fixed an issue where drill-downs were not working on the ESG Workspace analytics dashboard.
        -   Metric data cleared with multibyte characters — Fixed an issue where metric data task values were set to null when accidentally edited with multibyte characters.
        -   Related list form values cleared on reload — Fixed an issue where related list UX form values sourced from the main form were cleared when reloading in the ESG workspace.
        -   Formula builder not loading for disclosure managers — Resolved an issue where the formula builder was not loading in the workspace for users with the reporting disclosure manager role.
        -   Document ID field editability — Made the Document ID field read-only as it will now be populated automatically.
        -   Accessibility improvements — Fixed accessibility issues across the application.
        -   Formula tree node visibility — Fixed an issue where node map tree nodes were not visible in the formula tree view.
        -   Create Risk button not visible — Resolved an issue where the Create Risk button was not visible in the form header on risk assessment scope records.
        -   Orchestrator execution plan — Fixed an issue where the orchestrator was skipping the last agent in the execution plan, causing workflows to close without completing all steps.
        -   List type data visualization — Fixed an issue where list type data visualization was not available for selection in Reporting configuration since the Zurich release.
        -   Record page form controller — Fixed a set value issue in the record-vertical child page when using the Form controller.
-   **Version 22.0.2 - March 2026**
    -   Changed: The ServiceNow Environmental, Social, and Governance Management application has been renamed to Operational Sustainability Management. This application manages sustainability-related data, metrics, and reporting requirements. All existing functionality, features, and user roles remain unchanged.
    -   New:
        -   Materiality assessment integration with SocialSuite
            -   Conduct CSRD-compliant double materiality assessments in SocialSuite and automatically synchronize the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following GRI and ESRS standards.
        -   Create a threshold for a metric
            -   Configure thresholds with multiple levels and ranges for granular monitoring. Duplicate and modify existing thresholds to streamline creation. When thresholds are breached, automated actions trigger immediately.
        -   Extract data from utility invoices
            -   The system now automatically extracts metric unit values from invoices and updates your metric data accordingly. This automation ensures your metric data reflects accurate unit of measure values from invoice information.
-   **Version 21.1.3 - December 2025 \(Zurich\)**
    -   New:
        -   Added default values in Calculated Metric Definition Settings to prevent calculation errors.
        -   Enabled automatic audit tracking for all emission factor tables.
        -   Removed unit restrictions between calculated metric definitions and emission factors for greater flexibility.
-   **Version 21.0.2 - August 2025**
    -   Introduction of Platform Analytics view in ESG Management for creating dashboards and reports.
    -   Updated calculated metric definition calculation logic to automatically recalculate data when emission factor values change, using the new values for dates within the validity period. This ensures that the metrics data is consistent and accurate.
-   **Version 20.2.0 - June 2025**

    Fixed: Important security fixes.

-   **Version 20.1.1 - May 2025**

    Minor bug fixes and improvements.

-   **Version 20.0.1 - February 2025**
    -   New:
        -   Import metric data by using a pre-defined import template with instructions. With this process, you can import and manage the metric data within your organization.
        -   Review the calculated metric definition data by using a formula tree so that you can access detailed information on the operands, metric definitions, metrics, and emission factors.
    -   Changed:
    -   -   If you have the ESG manager \[sn\_esg.metric\_manager\] role, you can now configure either text, choice, or HTML format options for responses to qualitative metric data tasks that are related to manual metric definitions, including both initial and overridden responses.
-   If you have the ESG data owner \[sn\_esg.data\_owner\] role, you can now apply filters by using the filter menu and reject or approve tasks from the metric data table side panel. Data owners can now multi-submit and assign approvers to multi-approve or reject tasks, with the option to use choice and HTML response formats.
-   If you have the ESG Manager \[sn\_esg.metric\_manager\] role, you can now configure the Data Owner Assignment type to be either simple or advanced for manual metric definitions. When you select the Simple option, the system assigns the specified Data Owner or Data Owner Group to the Metric Data Task. If you choose the Advanced assignment option, which is available with the GRC: Approver Configurator application, you can set custom configuration conditions, tables, or data owners to dynamically assign data owners.
    -   Fixed: Minor bug fixes and improvements.
-   **Version 19.0.1 - August 2024**
    -   New: Added provision to integrate disclosures with SharePoint sites
    -   Changed: Upgraded all the workspace pages to WCAG2.1 AA compatible
    -   Removed: Removed provision to integrate disclosures with personal OneDrive
-   **Version 18.1.1 - July 2024**

    Fixed an issue with the 'Disclosure' overview tab showing up on unwanted workspaces.

-   **Version 15.0.3 - September 2022**

    Fixed: Data owner metric data entry UI was not displaying the group filter correctly. This issue is addressed.

-   **Version 13.0.3 - November 2021**

    ServiceNow's Operational Sustainability Management Management and Reporting application help customers manage their Operational Sustainability Management programs by providing them with a common platform to track and report goals and performance across the  Operational Sustainability Management pillars.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

