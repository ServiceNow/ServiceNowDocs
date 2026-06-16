---
title: Now Assist Readiness Evaluation release notes
description: Version history for the Now Assist Readiness Evaluation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-now-assist-readiness-eval.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Now Assist Readiness Evaluation release notes

Version history for the Now Assist Readiness Evaluation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.0 - June 2026**
    -   Changed: The Ready/Action Required readiness percentage calculation has been updated across all module cards on both the Agentic AI Assessment and Now Assist Assessment tabs. The percentage now reflects the ratio of passed assessment questions to total questions of interest for the current run, replacing the previous effort-based calculation. This change ensures readiness scores accurately reflect the current state of your instance across all assessed modules: Agentic AI ITSM, CSM, and HRSD; and Now Assist ITSM, CSM, HRSD, AI Search, and Virtual Agent.
    -   Fixed:
        -   Resolved an issue where customized field counts displayed in Agentic AI and Now Assist assessment findings were inaccurate due to overly broad table scoping in the underlying query. Field counts now correctly reflect only the target table for each assessment module across ITSM, CSM, and HRSD.
        -   Resolved an issue where click-through links in assessment findings failed to load on instances with large datasets. Links now use a query-based URL rather than enumerating sys\_ids, ensuring consistent navigation to affected records regardless of instance size.
        -   Resolved an issue where the HRSD Agentic AI assessment hyperlink displayed all business rules on the HR Case table instead of the intended filtered set of custom business rules.
        -   Resolved an issue where the Now Assist ITSM assessment reported incorrect percentages for Resolution Notes and Work Notes fields. The calculation now correctly filters to resolved incidents only, consistent with the assessment question definition.
-   **Version 1.3.0 - April 2026**
    -   New:
        -   Agentic AI assessment for HR Service Delivery \(HRSD\), covering four out-of-the-box agentic workflows: Predict Service &amp; Transfer HR Cases, Resolve Non-Critical HR Cases, Resolve Critical HR Cases, and Generate Onboarding Ramp-Up Plan
        -   Dedicated Agentic AI HRSD assessment page with status icons, legends, and download functionality
        -   HRSD agentic findings now reflected in the Agentic AI home page readiness card, assessment summary, dashboard visualizations, and remediation tab
        -   HRSD agentic assessment data included in the exportable PDF readiness report
    -   Changed: Updated Agentic AI summary page, Homepage cards, Dashboard, and Remediation properties tab to include Agentic AI HRSD assessment data
    -   Fixed:
        -   Resolved a script include error that prevented AI Search, ITSM, CSM, and HRSD scheduled assessment jobs from completing when percentage variables were uninitialized or contained null values
        -   Resolved an issue where the Now Assist Readiness Evaluation application's list view configuration overrode AI Agent Studio's default Agentic Workflows list layout, causing jumbled fields when this app was installed via Now Assist Suite.
-   **Version 1.2.1 - March 2026**
    -   Changed:
        -   Updated assessment terminology across the workspace to use clearer, implementation-focused language:
            -   Severity labels now display as Required, Recommended, and Informational
            -   Readiness status now displays as Ready or Action Required
            -   Finding categories now display as Data Readiness, Configuration Needed, and Now Support Recommended
            -   Dashboard widget labels updated to Assessment Findings, Findings by Category, Finding Trends, and Remediation Effort by Category
        -   Corrected inconsistent widget display order between the Agentic AI and Now Assist assessment dashboard tabs so both tabs now present Findings widgets first and Effort widgets second
-   **Version 1.2.0 - February 2026**

    Fixed: Performance and minor display improvements.

-   **Version 1.1.0 - January 2026**
    -   New: Editable estimated remediation effort: Users can now view effort assumptions on a separate tab \(via system property\) and modify default assumptions to fit their business.
    -   Changed:
        -   Improved dashboard usability with drill‑downs from the Now Assist and Agentic AI summary tabs.
        -   Expanded remediation effort legend across all pages, from “None” to “XXL.”
        -   Enhanced Agentic AI summary navigation with links to ITSM and CSM tabs.
    -   Fixed:
        -   Resolved inflated estimated effort caused by irrelevant metrics.
        -   Reworded select questions for clarity.
        -   Refined customization logic to show only items affecting Now Assist BU skills implementation; “warnings” show no remediation effort.
        -   Optimized scheduled job performance by prioritizing the latest 10,000 records \(via system property\).
        -   Set optimal record count \(50\) to limit hallucinations.
    -   Removed: Removed the Agentic workflow grouping/selector from the ITSM assessment to match CSM, as the assessment applies to all workflows.
-   **Version 1.0.5 - December 2025**
    -   Fixed:
        -   Unable to load guided setup in Zurich release \(PRB1952120\).
        -   AI Search scheduled job fails and logs script errors if AI Search for Next Experience is not installed \(PRB1955805\).
        -   Virtual Agent assessment doesn't complete when the answer record for the question "is there an opportunity to convert any of the top 10 catalog items for conversational?" contain a carriage return \(\\r\) in the Name field \(PRB1955831\).
        -   The query "How many past incidents are there with no resolution details?" incorrectly filters for incidents in the On Hold state with empty Resolution notes. It should only check Resolved and Closed incidents where Resolution notes are empty \(PRB1956511\).
        -   Custom script links generated incorrectly \(PRB1959327\).
        -   Incorrect Contact Support information in Application Navigator under Now Assist Readiness Evaluation \(PRB1962501\).
        -   System Properties: Not showing up properties in Guided Setup step 3 \(PRB1962505\).
        -   Resolution notes should not be in HRSD Module \(PRB1962507\).
        -   All questions and answers are now displayed correctly on the HRSD tab \(PRB1962508\)
        -   Validation of questions and answers are now displayed correctly on the Agentic AI - ITSM TAB \(PRB1962512\)
        -   Question showing wrong icon for "Are there any group restrictions?" \(PRB1962514\).
    -   Removed:
        -   Removed privacy policy from Application navigator \(PRB1962502\).
        -   Removed "Four" in Restricted Caller Access Privilege Step 2 in Guided Setup \(PRB1962504\).
-   **Version 1.0.3 - October 2025**

    New: This is the initial version of the Now Assist Readiness Evaluation. The assessment is a solution designed to simplify and automate the assessment process as part of Now Assist \(ITSM, CSM, HRSD\) &amp; agentic AI \(ITSM, CSM\) capabilities and implementation.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

