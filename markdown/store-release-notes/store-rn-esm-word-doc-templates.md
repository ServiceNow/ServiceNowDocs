---
title: Word Document Templates release notes
description: Version history for the Word Document Templates application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-word-doc-templates.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Word Document Templates release notes

Version history for the Word Document Templates application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**

    New: Word document templates now support the initials tag for the signatory in addition to existing e-signature tags.

-   **Version 1.9.7 - January 2026**

    Fixed: Resolved date format to be displayed correctly for signature date in Word templates when using AdobeSign.

-   **Version 1.9.5 - December 2025**
    -   Fixed:
        -   Resolved preview of contract template.
        -   Optimized the performance by keeping the latest contract document template and deleting its older attachments.
-   **Version 1.9.0 - August 2025**
    -   New:
        -   When template is setup on the Contract Request table, the Table mappings tab displays an additional field, called the Parent request table field, that you can use to select the source parent request table
        -   Additionally, the Table field has been renamed to Lookup table where you can select the table from the data that is populated into the contract document. If the template isn't based on the Contract Request table, only the Lookup table field is shown.
-   **Version 1.7.0 - February 2025**

    Fixed: Security issues.

-   **Version 1.6.2 - November 2024**

    Security fixes.

-   **Version 1.5.1 - August 2024**

    Fixed: A contract document could not be sent for signature if the participants field was empty under Template Mappings of the contract template.

-   **Version 1.4.0 - May 2024**

    Fixed: Signature date field is displayed as signature instead of signature date in Docusign doc task.

-   **Version 1.2.1 - March 2024**

    The Word Document Templates application leverages industry standard Microsoft Word to generate document templates to quickly create contract templates or standard letters in alignment with the submitted request. The application is automatically installed with Contracts Core.


