---
title: Vulnerability Response Patch Orchestration with Microsoft SCCM release notes
description: Version history for the Vulnerability Response Patch Orchestration with Microsoft SCCM integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-po-microsoft-sccm.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Vulnerability Response Patch Orchestration with Microsoft SCCM release notes

Version history for the Vulnerability Response Patch Orchestration with Microsoft SCCM integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.0.6 - September 2026**

    New: Deploy more than one patch to more than one collection in a single deployment, instead of one patch to one collection at a time. When you select more than one patch for a deployment, the integration automatically creates a Software Update Group in Microsoft SCCM to bundle the patches.

-   **Version 2.3.9 - August 2026**
    -   Changed: Query-Based \(JDBC\) SCCM Integration Migration
    -   Migrated all Microsoft SCCM integrations — Software/Device Collection, Patch Update, Device Patch Update, and Deployment from API-based to direct SQL query-based \(JDBC\) data collection. This change improves reliability and reduces dependency on SCCM's web service API, along with added configuration validation, ECC queue stuck-record detection, and pagination support for large result sets.
    -   Strengthened Query-Based Integration ACLsAdded out-of-the-box ACLs restricting direct SCCM query access.Fixed:
    -   Resolved several functional and review-driven fixes across the new query-based integrations, including corrections to the delta-days business rule, status transform map logic, and ECC queue response handling for delayed replies.
-   **Version 2.3.1 - May 2025**

    New: The patch orchestration data model is extended to integrate with ITSM systems seamlessly.

-   **Version 2.2.1 - November 2024**

    Fixed: Minor fixes for this release.

-   **Version 2.1.6 - May 2024**

    Fixed: Localization issues have been fixed.

-   **Version 2.1.2 - February 2024**

    Fixed: Provided error handling support while validating credentials in SCCM configuration page.

-   **Version 2.1.1 - August 2023 \(Vancouver\)**

    Fixed: Earlier, the SCCM integration credentials validation was failing with the flow designer timeout. This issue has been fixed. The SCCM integration credentials validation now honors the integration instance timeout property.

-   **Version 2.0.1 - March 2022**

    This patch orchestration integration with the Vulnerability Response application uses scheduled Patch imports from the Microsoft System Center Configuration Manager \(SCCM\) product to help your security and IT teams identify your critical vulnerabilities and then apply the updates that can fix them.


**Parent Topic:**[ServiceNow Store - Vulnerability Response version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

