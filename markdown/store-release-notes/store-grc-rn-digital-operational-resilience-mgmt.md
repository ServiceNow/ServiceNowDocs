---
title: Digital Operational Resilience Management release notes
description: Version history for the Digital Operational Resilience Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-digital-operational-resilience-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Digital Operational Resilience Management release notes

Version history for the Digital Operational Resilience Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   New: Added LEI validation against GLEIF API for legal entities, branches, and third-party providers- Introduced duplicate DORA contract detection during manual entry and upload- Added system properties for GLEIF API configuration \(timeout, batch size, validation behavior\)
    -   Changed: Improved upload error messages with internationalization support- Enhanced LEI code handling to be case-insensitive- Updated monetary decimal precision configuration
    -   Fixed: Resolved intra-group contractual arrangement deletion issues- Corrected supply chain cascading updates and deletions- Fixed date validation on specific information records- Addressed third-party engagement dictionary issues
-   **Version 22.0.1 - March 2026**
    -   New: Currency conversion for the contract value and Total expenses aggregation for third-party providers has been added.
    -   Changed: The combination of License Activity, LEI of Entity, and Function Name must be unique per Regulator's doc and this check has been incorporated.
    -   Fixed: Records with missing function numbers no longer cause Register of Information \(ROI\) download errors.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New:
        -   Digital Operation Resilience Management export package functionality has been updated to support the CSV format along with Level 1 and Level 2 validation requirements.
        -   As part of export package, level 3 validations have been introduced to validate the generated package and provide the output of the validations along with the downloaded export package.
    -   Changed: Any fields that need to be strict read-only have been updated appropriately in the dictionaries to prevent client side updates.
    -   Fixed: Missing field level validations or failing validations have been addressed to confirm with regulator suggested field validations.
-   **Version 21.0.1 - August 2025**
    -   New: Field level validations have been added to meet regulator requirements.
    -   Changed: This application data model has been updated to align with regulators data model.
    -   Fixed: Translation issues have been addressed.
-   **Version 20.1.1 - May 2025**

    New:

    -   New:
        -   Allow multiple legal entities using the service when creating DORA contract.
        -   Include the choice/reference dropdown options in the downloaded MS Excel files.
        -   Button to download templates on Upload request page.
    -   Updated: Updated reporting template to reflect latest regulator changes.
    -   Fixed:
        -   Prevent duplicate record creation for Legal Entity, Branch and DORA contract records.
        -   Translation issues have been handled.
        -   Allow multi-selection on Business Capability/Business Service/Business Process/Service Offering in the Function record
-   **Version 20.0.10 - March 2025**
    -   New:
        -   'Business Capability' has been added as a Function type that can be selected from a drop-down list on a Function record. The Business Capability records being referenced are from the cmdb\_ci\_business\_capability table.
        -   The 'Business Capability' field is now available as a Function type option for a Function record on the Vendor Risk Management Workspace.
        -   Added the following new fields for Third parties and Third-party engagements "Type of additional identification code to identify the ICT third-party service", "Additional identification code of ICT third-party service provider", "Legal name of the ICT third-party service provider". Added "EUID" as a choice for "Type of code to identify the ICT third-party service provider's ultimate parent" and "Type of additional identification code to identify the ICT third-party service" for third parties and third-party engagements. If supply chain records, assessment records, or contract records are associated with a third party or third-party engagement that uses "EUID" code type, all relevant code type fields are auto-filled.
    -   Fixed:
        -   Addressed the issue where the system was selecting incorrect choices when downloading a template and creating duplicate choices when uploading functions. Both the label and the category are used to find the correct choice to avoid duplicate choice options.
        -   The column code numbers have been updated to align with the updated regulatory requirements. Additionally, the template has been updated to include new fields, such as 'Type of additional identification code to identify the ICT third-party service', 'Additional identification code of ICT third-party service provider', and 'Legal name of the ICT third-party service provider'. 'EUID' has been included as a choice for 'Type of code to identify the ICT third-party service provider's ultimate parent' and 'Type of additional identification code to identify the ICT third-party service'.
-   **Version 20.0.9 - February 2025**
    -   New: Added drop-down options to eight DORA excel templates
    -   Fixed:
        -   Functions identifier does not increment beyond F10
        -   Functions form always throws error that "Date of the last assessment of criticality or importance cannot be a future date." when the date format in system properties is set to 'MMM-dd-yyyy', even though the date is in the past
        -   When importing new Assessment from Excel, user does not enter "Is the ICT third party audited?" column, because the default value is "Yes", it complains that the "Date of the last audit on the ICT third-party service provider" is empty.
-   **Version 19.0.1 - November 2024**

    Digital Operational Resilience Management is a common application used to store legal entities, branches, functions, third-parties, third-party engagements, and contracts for reporting.


