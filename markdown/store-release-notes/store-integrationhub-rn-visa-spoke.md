---
title: Visa Spoke release notes
description: Version history for the Visa Spoke application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-visa-spoke.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Visa Spoke release notes

Version history for the Visa Spoke application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.5.2 - May 2026**

    Fixed: Fixed dispute questionnaire spoke regression issue

-   **Version 2.5.1 - April 2026**
    -   Changed:
        -   Updated dispute lookup responses to include JSON formatted data and raw response from Visa for better data accessibility and troubleshooting.
        -   Enhanced transaction detail lookups to include raw response data from Visa alongside structured transaction information.
        -   Updated dispute questionnaire submission to support additional fields and validation requirements per Visa revision 26.1.
        -   Updated exception request submission to align with latest Visa API specifications.
        -   Updated fraud bundle dispute questionnaire to support new data fields required by Visa.
        -   Enhanced dispute pre-arbitration detail lookups to support new request parameters and response fields.
        -   Updated dispute detail responses to include merchant acceptance indicator field for better dispute tracking.
        -   Fixed attachment object naming in arbitration and compliance workflows for proper file handling.
        -   Added translations for multiple languages to support global users.
-   **Version 2.4.0 - March 2026**
    -   New:
        -   Added a copy of the \*\*Look up Image\*\* action as a Builder and Parser action; marked the existing action as Deprecated.
        -   Added a copy of the \*\*Look up Report Output\*\* action as a Builder and Parser action; marked the existing action as Deprecated.
        -   Added a copy of the \*\*Download and Attach Image\*\* action as a Builder and Parser action; marked the existing action as Deprecated.
        -   Added a copy of the \*\*Look up Associated Transaction List\*\* action as a Builder and Parser action; marked the existing action as Deprecated.
-   **Version 2.2.2 - December 2025**

    Fixed: Look up Dispute Pre Arbitration Details Response Parser: Resolved an issue with the output object structure in the action type definition by removing unnecessary metadata fields. This ensures proper action status handling and improves reliability of workflow executions.

-   **Version 2.2.1 - October 2025**
    -   New:
        -   Visa 25.2 Integration: Added new fields for Visa spoke integration, enhancing the dispute management capabilities. Supports fetching the Visa Dispute Intelligence \(VDI\) score, which provides essential metrics for informed decision-making throughout the dispute process.
        -   Hypersearch Functionality: Implemented new hypersearch features as part of Visa 25.2 revision, providing improved search capabilities for dispute resolution.
    -   Changed:
        -   Label Improvements: Updated label from "Info" to "Information" across multiple action definitions, enhancing clarity and consistency in the user interface.
        -   Field Name Standardization: Changed "Probability Of Success" to "Probability of Success" for better readability and consistency.
        -   Field Label Enhancement: Expanded abbreviated label "Include Prediction Details Ind" to the more descriptive "Include Prediction Details Indicator" for improved user understanding.
    -   Fixed:
        -   Resolved issue with inconsistent field labeling by changing "Include Prediction Details Ind" to "Include Prediction Details Indicator".
        -   Field Naming Consistency: Fixed inconsistencies in field naming conventions across the Visa integration components.
-   **Version 2.0.0 - May 2025**
    -   New: Added spoke actions to support the Visa Stop Payment Service in Integration Hub.
    -   Fixed: Resolved an issue with missing API Endpoint and Resource path in spokes.
-   **Version 1.3.0 - April 2025**

    Changed

    -   Modifies VISA actions with respect to visa 25.1 revision
-   **Version 1.2.3 - March 2025**

    Fixed the issue with improper empty inputs that are being passed when subflows are called through scripts.

-   **Version 1.2.2 - February 2025**
    -   Added:
        -   New spoke to download and attach an image from a Visa document ID.
        -   New spoke to accept a dispute.
    -   Improvement:
        -   Added more fields in output of the spoke action
    -   Fixes:
        -   Updated the internal name of the case filing amount in the spoke action.
        -   Corrected the Dispute Category from string type to object.
        -   Corrected the Dispute amount from string to object.
        -   Fixed issues by cleaning up invalid input values of the spoke action.
        -   Modified the input structure for a spoke.
-   **Version 1.1.1 - October 2024**

    Changed: Updated all actions with Visa Resolve Online \(VROL\) Release 24.2 revision changes as released by Visa.

-   **Version 1.0.1 - May 2024**

    Fixed category mismatches in Actions.

-   **Version 1.0.0 - February 2024**

    The Visa spoke allows ServiceNow to connect with Visa's REST APIs, providing customers quick access to payment, and security data. Customers can use the spoke to search for transactions, collaborate with merchants, manage disputes, and perform other functions with updated security. It also enables them to resolve disputes, access data, and utilize other features. By integrating with the ServiceNow platform and other spokes, customers can create more complex workflows to fit their needs.


