---
title: Docusign eSignature Spoke release notes
description: Version history for the Integration Hub Docusign eSignature Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-docusign.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Docusign eSignature Spoke release notes

Version history for the Integration Hub Docusign eSignature Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.4.1 - June 2026**

    Fixed: Streamline ACLs

-   **Version 4.3.0 - May 2026**
    -   Changed: Action: Add support for Certified Delivery for Send Adhoc Signature Request to Users – Inline action
    -   Fixed: Actions: Send Adhoc Signature Request to User, Send Adhoc Signature Request to Users - Inline, Subflow: Send employment offer to candidate using DocuSign template
-   **Version 4.2.2 - February 2026**
    -   Fixed:
        -   Actions:
            -   Generate Embedded Sending URL
            -   Send Adhoc Signature Request to Users - Inline
-   **Version 4.2.1 - October 2025**

    New: AI Agents.

    Fixed:

    -   Defect: Warning message in logs for some actions
    -   Defect: Handle data input for Array.Object that contains nested Array.Object
    -   Action: Send Adhoc Signature Request to User action now supports attachments larger than 12.5MB
    Removed: Surplus subflow from AI Agent.

-   **Version 4.1.0 - August 2025**
    -   New: Actions: Lock Envelope, Unlock Envelope, Resend Envelope, Upsert Envelope Recipients
    -   Changed: Actions: Look up Recipients in an Envelope, Remove Recipient from Envelope
-   **Version 4.0.3 - July 2025**

    Fixed: Event Source, Triggers status set to Published.

-   **Version 4.0.2 - March 2025**

    Fixed input to set reminder and system defaults for the "Send Adhoc Signature Request to Users - Inline" action.

-   **Version 3.3.1 - March 2025**

    Fixed input to set reminder and system defaults for the "Send Adhoc Signature Request to Users - Inline" action.

-   **Version 4.0.1 - February 2025**
    -   New: Added Triggers that will show up in the Trigger picker while authoring Flows to trigger Flows based on Docusign Events.
    -   Note: The Triggers are only available Xanadu and onward releases.
-   **Version 3.3.0 - February 2025**

    New: Action: Generate Embedded Sending URL.

-   **Version 3.2.1 - December 2024**

    Fixed: Create User action.

-   **Version 3.2.0 - November 2024**

    Fixed: Sandbox access for client.

-   **Version 3.1.3 - October 2024**

    Fixed 2 bugs.

-   **Version 3.1.2 - June 2024**
    -   Changed:
        -   Spoke name is changed from "DocuSign eSignature Spoke" to "Docusign eSignature Spoke" to align with Docusign branding changes
        -   Spoke icon is changed from an older to the new one to align with Docusign's branding changes
-   **Version 3.1.1 - May 2024**

    Provides a robust solution for easily automating DocuSign for digital signatures. Send contracts, non-disclosure agreements, tax forms, or anything your company needs. Provides automation to send ad-hoc documents uploaded as an attachment for signature. Then, the end users can choose to attach the documents to a ServiceNow Record. Additionally, provides the ability to populate an existing template in DocuSign, track the recipient's signing status, and envelope status in real-time.

-   **Version 3.0.0 - February 2024**

    New: Actions for BulkSend to manage the sending of envelopes to multiple recipients.

-   **Version 2.6.2 - August 2023**

    New: Support for absolute positioning of signature \(x,y precise\).

-   **Version 2.6.1 - June 2023**

    Fixed: Issue related to document\_id data type.

-   **Version 2.6.0 - May 2023**
    -   Changed:
        -   Action: Attach Combined Document to ServiceNow Record - You can choose whether to include the certificate in the combined document or not.
        -   Handles envelop cancelled incoming event.
-   **Version 2.4.2 - September 2022**

    Fixed: Patch version of DocuSign Spoke for Integration Hub. This version includes fixes to improve the installation performance, pre-processing error at embedded Signing without signing recipient, and changes to canceling or voiding the envelope sent for DocuSign eSignature.

-   **Version 2.4.1 - March 2022**

    New: This version adds functionality to upload the transient document and Anchor Tabs support for parallel document signing.

-   **Version 2.2.1 - December 2021**
    -   Fixed: Patch release of DocuSign Spoke for IntegrationHub. This version includes security-related changes and fixes the below issues:
        -   Character limitation at email subject.
        -   Method 'Look up Fields' not returning tabLabel and pageNumber for radio button.
        -   Duplicate recipients created when same person is repeated twice in Serial Signing.
-   **Version 2.2.0 - October 2021**
    -   New:
        -   Actions now support multiple recipients and carbon copy recipients in one call.
        -   Now support REST 2.1 inbound webhook event notification from DocuSign.
        -   Added authentication configuration template for easier setup.
        -   Added a sample inbound subflow to showcase how to build a workflow from DocuSign to ServiceNow.
-   **Version 2.1.0 - August 2021**
    -   New action:
        -   Look up Fields action to get list of all fields in 1 action call.
        -   Set field Values action to set all fields in 1 action call.
        -   Reflect the latest actions above in Get and Set Values for Docusign PDF Template subflow to improve integration efficiency
-   **Version 2.0.3 - June 2021**

    This is a patch release of DocuSign Spoke for IntegrationHub. This release includes a fix for cross-scope privilege to variables.

-   **Version 2.0.1 - April 2021**

    This is a patch release with a couple of fixes for the Docusign Spoke

-   **Version 2.0.0 - November 2020**
    -   New: Actions and subflows
    -   Changed: Updates to existing actions and subflows
-   **Version 1.2.2 - June 2020**

    Patch release of DocuSign spoke for IntegrationHub.

-   **Version 1.2.1 - February 2020**
    -   New actions:
        -   Get Documents In An Envelope
        -   Get Recipients In An Envelope
        -   Get List of Documents
    -   New features:
        -   Real time update recipient signing status and the envelope status in the DocuSign spoke
        -   Dynamic inputs to discover documents
        -   Restrict access to accounts based on user roles and attributes
-   **Version 1.2.0 - November 2019**

    Added new actions and features to the DocuSign Spoke New Actions: Get Documents In An Envelope Get Recipients In An Envelope Get List of Documents New Features Real time update recipient signing status and the envelope status in the DocuSign Spoke Dynamic inputs to discover documents Restrict access to accounts based on user roles and attributes

-   **Version 1.1.6 - August 2019**

    Licensing patch for the DocuSign spoke on Integration Hub

-   **Version 1.1.4 - March 2019**
    -   Provides a robust solution for easily automating DocuSign for digital signatures
    -   Send contracts, non-disclosure agreements, tax forms, or anything your company needs
    -   Provides automation to send adhoc documents uploaded as an attachment for signature
    -   Provides the ability to populate an existing template in DocuSign.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

