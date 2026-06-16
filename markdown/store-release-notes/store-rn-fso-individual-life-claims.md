---
title: Individual Life Claims release notes
description: Version history for the Individual Life Claims application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-individual-life-claims.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Individual Life Claims release notes

Version history for the Individual Life Claims application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.6.0 - June 2026**

    New: Added child tables for indexing for Financial Case indexed source

-   **Version 1.5.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 1.4.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 1.1.1 - February 2025**

    Fixed: Performance improvements.

-   **Version 1.1.0 - November 2024**
    -   New: Added "sn\_ins\_claim\_indl.flow\_executor" \(Flow Executor role\) which is going to be used to run all flows/sub-flows. It contains the "sn\_bom.flow\_executor" and "sn\_ins\_claim\_indl.manager" roles.
    -   Changed:
        -   Flows and sub-flows have been updated to run as Flow executor instead of System user:
            -   Individual death claim triage decision.
            -   Create participant role for related claims.
            -   Update participant role for related claims.
            -   Create related death claim.
            -   Create related death policy claim.
            -   Individual life claim policy case - PB activity.
            -   Related claim closed complete.
            -   Claim Participant - PB activity.
            -   Individual Claim Document Decision.
            -   Create or update claim participant for related claims.
            -   Create related death policy claims.
        -   BeneficiaryRoleAjax, IndivDeathClaimAjax have been made as Sandbox enabled as false.
    -   Removed: Removed contributor viewer role from adjuster.
-   **Version 1.0.3 - September 2024**

    Fixed: The app was released as a dependency plugin. A fix was applied to install it as an independent plugin.

-   **Version 1.0.0 - August 2024**

    Individual Life Claims empowers carriers to digitize any individual life benefits claims process end-to-end. Eliminate paper files and update claims in real time, with the ability to work from anywhere. Automate the transfer of documents, data, payment, and approval requests with seamless work orchestration. Increase efficiencies and improve customer satisfaction with frictionless experiences.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

