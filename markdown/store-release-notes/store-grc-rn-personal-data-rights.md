---
title: GRC: Personal Data Rights release notes
description: Version history for the GRC: Personal Data Rights application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-personal-data-rights.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Personal Data Rights release notes

Version history for the GRC: Personal Data Rights application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.4 - June 2026 \(Australia\)**
    -   New:
        -   Configure the Personal Data Rights \(PDR\) external-facing form to map jurisdictions to data subject types and request types, and control whether an authorized agent can submit a request on behalf of a data subject.
        -   Privacy administrators can navigate to External form configuration to tailor the public-facing PDR form for their organization.
    -   Changed:
        -   Query range access controls have been added for PDR plugin tables.
        -   Access to data is now managed with updated query range ACLs for improved governance.
-   **Version 22.0.2 - March 2026**
    -   Changed: Fixed demo data changes for control objective workflow.
    -   Fixed: Fixed security issues.
-   **Version 21.1.3 - December 2025**
    -   New: Added the ability to create personal data rights requests using a public form. This feature includes:
        -   The capability for users to submit requests without logging into the ServiceNow instance.
        -   The option for users to provide details such as country, email, phone, and type of request.
        -   Email OTP-based validation to ensure the security of the requests.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   Fixed:
        -   Fixed issues related to access permissions.
        -   Corrected spelling issues across the product.
-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.1 - May 2025**

    Fixed the accessibility and security issues on PDR application.

-   **Version 20.0.1 - February 2025**

    Fixed: Refactored code to improve code quality and fixed other certification errors.

-   **Version 19.1.1 - November 2024**

    Fixed: Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.

-   **Version 19.0.1 - August 2024**

    The Personal Data Rights application enables individuals associated with an organization in exercising their personal data rights, while assisting the privacy team in monitoring, overseeing, and promptly resolving incoming data rights requests within the SLAs specified by global privacy laws. Additionally, the privacy team has the capability to delegate tasks to different data administrators for the timely fulfillment of individual requests within the defined SLAs.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

