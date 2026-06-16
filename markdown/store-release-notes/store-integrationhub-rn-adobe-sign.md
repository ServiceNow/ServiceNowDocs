---
title: Adobe Acrobat Sign spoke release notes
description: Version history for the Integration Hub Adobe Acrobat Sign spoke on the ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-adobe-sign.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Adobe Acrobat Sign spoke release notes

Version history for the Integration Hub Adobe Acrobat Sign spoke on the ServiceNow.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.10.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 2.9.0 - May 2026**

    Changed: Added support for ACCEPTORS role while adding participants to the agreement in Add Participant to Agreement, Add Participant to Agreement with Email OTP Authentication, Add Participant to Agreement with Password Authentication, and Add Participant to Agreement with Phone Authentication actions.

-   **Version 2.8.0 - March 2026**
    -   New:
        -   Action: Generate Embedded Sending URL
        -   Webhook event: AGREEMENT\_EMAIL\_BOUNCED
-   **Version 2.7.2 - October 2025**

    Fixed: Dot-walking in actions for alias.

-   **Version 2.7.1 - July 2025**
    -   New: Action: Add Participant Reminders to Agreement action to set up reminders for agreement.
    -   Changed: Action: Cancel Agreement - To also now take in cancellation reason.
    -   Fixed:
        -   Action: Add Participant to Agreement Action
        -   Adobe sign webhook authentication KMF policy
-   **Version 2.6.0 - May 2025**

    Changed: Participant Name input added to Add Participant to Agreement, Add Participant to Agreement with Phone, Add Participant to Agreement with Email OTP, Add Participant to Agreement with Password, and Send Agreement

-   **Version 2.5.2 - December 2024**

    Fixed: Security defects.

-   **Version 2.5.1 - November 2024**
    -   New:
        -   Actions have been added to support some methods of Advanced Electronic Signature \(AES\), and to retrieve Agreement Documents and add to ServiceNow records.
            -   Document Management: Look up Agreement Documents, Attach Agreement Document to ServiceNow Record, Attach Agreement Audit Trail to ServiceNow Record
            -   Signature Management: Add Participant to Agreement with Email OTP Authentication, Add Participant to Agreement with Password Authentication, Add Participant to Agreement with Phone Authentication
    -   Changed:
        -   Action has been upgraded to support Agreement level password
            -   Signature Management: Create Draft Agreement
    -   Fixed:
        -   Upload Attachment as Transient Document - File name was not being honoured
        -   ACL configurations
-   **Version 2.4.1 - July 2024**

    Fixed: Actions that were processing ETag.

-   **Version 2.4.0 - May 2024**

    Changed: Updated handling of incoming events related to document delegation and capturing that information in participants module.

-   **Version 2.3.4 - January 2024**
    -   New: Add Report View ACL for participant table.
    -   Fixed: Authentication-related error.
-   **Version 2.3.3 - October 2023**

    Fixed: Send Agreement action for authoring state.

-   **Version 2.3.2 - September 2023**

    Fixed: This release version fixes the license requirements.

-   **Version 2.3.1 - August 2023**

    New: Support absolute positioning of signature \(x,y precise\).

-   **Version 2.3.0 - May 2023**

    Changed: Action: Send Agreement - Allows you to send multiple documents.

-   **Version 2.2.0 - February 2023**
    -   New: Look up Agreement Events action
    -   Changed: Finalize Draft and Send Agreement action
-   **Version 2.1.2 - September 2022**

    Fixed: Patch version of Adobe Sign Spoke for Integration Hub. This version includes a fix to improve installation performance of spoke.

-   **Version 2.1.1 - February 2022**

    Fixed: This version adds fixes for values not being set within Create Webhook action, and an issue with Agreement - Send NDA outbound flow.

-   **Version 2.1.0 - October 2021**
    -   New: Added a column to support expiration date in the agreement table.
    -   Changed: Updated the error message when hybrid routing is not enabled in Adobe instance.
-   **Version 2.0.0 - July 2021**
    -   Added MegaSigns related actions
    -   Added sample MegaSigns flow
    -   Action label naming convention cleanup
-   **Version 1.1.2 - February 2021**

    Patch release of Adobe Sign spoke for IntegrationHub.

-   **Version 1.1.1 - June 2020**

    Patch release of Adobe Sign spoke for IntegrationHub.

-   **Version 1.0.2 - January 2020**
    -   Fixed:
        -   Fixed a security bug
        -   Label name is no longer missing for Credential and Connection Alias on crating group, document, or agreement records
        -   Fixed issue with attaching signed agreements to ServiceNow records
        -   Outputs are now ordered correctly
-   **Version 1.0.0 - August 2019**

    Automate document, signature, and user management of your Adobe Sign instance from the ServiceNow instance.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

