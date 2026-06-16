---
title: GRC: Model Risk Management release notes
description: Version history for the ServiceNow GRC: Model Risk Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-model-risk-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Model Risk Management release notes

Version history for the ServiceNow® GRC: Model Risk Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Standardized Query Range ACLs: All tables now include standardized query range ACLs, ensuring authenticated users with read permissions can reliably query records. New ACL rules install automatically during upgrade. Automated scripts handle detection and processing of any previously customized ACLs. Review customized query range ACLs after upgrade to confirm alignment with your access policy.
        -   Smart Assessment Template Versioning: Model risk management now supports template versioning — modify existing templates by creating new versions instead of building from scratch. The latest published version is always used when creating assessments.
    -   Changed: Workspace redirection for Model Risk Management notifications: Email notification links for Model Risk Management records now redirect users to the Model Risk workspace or the GRC Tasks portal, based on their access permissions.
    -   Fixed:
        -   The "Create Assessment" button now functions correctly when creating assessments in the initiation state.
        -   Resolved translation gaps in the Model Risk Management workspace.
-   **Version 22.0.4 - March 2026**
    -   Fixed:
        -   Model Owner updates now reflect correctly in the model header.
            -   Resolved an issue where updating the Model Owner through stakeholder changes did not reflect in the model header.
        -   Corrected access control for model risk data.
            -   Fixed an authorization issue by removing unintended role inheritance, ensuring users have access only to the model risk content.
        -   Resolved list view Edit action failure.
            -   Fixed an issue where the Edit action in the Model Risk workspace list view was failing. The unsupported Edit option has been removed to prevent errors.
-   **Version 21.1.3 - December 2025**

    Model Risk Management \(MRM\) application focuses on identifying, assessing, and mitigating the risks associated with using quantitative models in decision-making processes. These models, commonly used in financial services for tasks such as pricing, value-at-risk calculations, and cashflow projections, can carry significant risk if they produce flawed or misleading results.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

