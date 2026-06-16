---
title: Digital Resilience Third-party Information Register release notes
description: Version history for the Digital Resilience Third-party Information Register application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-digital-resilience-third-party-info-register.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Digital Resilience Third-party Information Register release notes

Version history for the Digital Resilience Third-party Information Register application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Added LEI code validation against GLEIF API for legal entities, branches, and third-party providers.
        -   Added legal entity provider reporting to B.05\_01 sheet.
    -   Changed:
        -   Optimized LEI validation using batch GLEIF API calls \(200 records per batch\) for improved performance.
        -   Enhanced LEI validation to use headquarters address country for third parties and branches.
        -   Updated duplicate row detection to warn users during CSV package download for B.02\_02 and B.05\_02 sheets.
    -   Fixed:
        -   Corrected decimal monetary value handling in CSV reports \(PRB2022444\).
        -   Resolved parent legal entity inclusion in tab 01.02 CSV report \(PRB2006352\).
        -   Fixed CSV column ordering to display in natural order \(PRB2000322\).
        -   Corrected boolean value formatting from 'true' to 'TRUE' in B.03\_01 sheet \(PRB2000321\).
        -   Resolved translation issue for "Not Applicable" in downloaded CSV packages \(PRB1996947\).
-   **Version 22.0.3 - March 2026**

    New: Updates have been made to support the currency conversion during download of ROI report.

-   **Version 21.1.7 - December 2025 \(Zurich\)**
    -   New:
        -   Field-level validations outlined by regulators have been added to be compliant.
        -   Updates have been made to support the CSV download package, including structured ZIP files with metadata and report folders aligned to regulator specifications, file naming conventions with LEI and entity ID, and enhancements for validation workflows.
-   **Version 21.0.1 - August 2025**

    Changed: The download template has been updated to align with the regulator template.

-   **Version 20.1.2 - May 2025**
    -   New: Include the choice/reference dropdown options in the downloaded MS Excel files.
    -   Fixed: i18n translation issues have been addressed.
-   **Version 20.0.0 - March 2025**
    -   New: Added the following new fields for Third parties and Third-party engagements "Type of additional identification code to identify the ICT third-party service", "Additional identification code of ICT third-party service provider", "Legal name of the ICT third-party service provider". Added "EUID" as a choice for "Type of code to identify the ICT third-party service provider's ultimate parent" and "Type of additional identification code to identify the ICT third-party service" for third parties and third-party engagements. If supply chain records, assessment records, or contract records are associated with a third party or third-party engagement that uses "EUID" code type all relevant code type fields are auto-filled.
    -   Fixed: Function's column codes have been modified and templates have been updated to reflect latest regulatory changes.
-   **Version 19.0.0 - November 2024**

    Application provides default template aligned with DORA \(Digital Operation Resilience Act\) regulatory requirements for contractual arrangements for the services provided by third parties.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

