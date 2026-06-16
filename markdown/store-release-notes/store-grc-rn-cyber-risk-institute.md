---
title: GRC: Cyber Risk Institute release notes
description: Version history for the GRC: Cyber Risk Institute application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-cyber-risk-institute.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Cyber Risk Institute release notes

Version history for the GRC: Cyber Risk Institute application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Enabled versioning support for CRI tiering and assessments.
        -   Enhancements to query range ACLs:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
    -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**
    -   Changed:
        -   Updated the control objective content records with record nature field as Current version and state as published
        -   Updated the control objectives module to prevent the display of working drafts.
    -   Fixed: CRI Profile and Tiering Questionnaires assessment are not being created
-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed: Added a read-only attribute to the read-only field 'CRI Tier' in Control objective table to enhance security.

-   **Version 21.0.1 - August 2025**

    Changed: Smart assessment updates for CRI and Tiering assessments to support the introduction of a new reference field called "purpose."

-   **Version 19.1.0 - November 2024**
    -   Changed:
        -   Security fixes
        -   Labels
-   **Version 19.0.3 - August 2024**
    -   The Cyber Risk Institute \(CRI\) framework profile and CRI assessments assist customers in implementing the CRI framework to enhance cyber compliance management. This framework includes detailed diagnostic statements \(control objectives aligned with NIST CSF 2.0\) that map to financial services regulatory references \(such as FS citations from FFIEC CAT and others\).
    -   As part of the Cyber Risk Institute's \(CRI\) Accelerator, customers can:
        -   Import a CRI profile containing relevant authority documents, citations, and control objectives based on NIST CSF.
        -   Streamline the risk management process with automated tiering and selection of CRI assessments, conducted using the smart assessment engine.
    -   Automatically create controls based on tier and generate a compliance score from the CRI assessment responses, which roll up to the entity level.

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

