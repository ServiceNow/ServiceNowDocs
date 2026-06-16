---
title: Security Incident Response integration with Proofpoint release notes
description: Version history for the Security Incident Response integration with Proofpoint application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-int-proofpoint.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response integration with Proofpoint release notes

Version history for the Security Incident Response integration with Proofpoint application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.2 - June 2026**

    Fixed: Read only column access on all the tables for read only fields.

-   **Version 1.1.1 - May 2026**

    Fixed: Security Incident Response \(SIR\) records were not created during Proofpoint event ingestion when the secure\_notes field was explicitly mapped in the profile's field mapping configuration.

-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.0.5 - August 2025**

    Fixed: Populate Integration source for aggregated incidents.

-   **Version 1.0.4 - July 2025**

    Fixed: ACL issues reported from ARC0016874.

-   **Version 1.0.3 - May 2025**

    Fixed: Access permissions for the sn\_si.analyst role to ensure read-only access to Event Profiles.

-   **Version 1.0.2 - March 2025**
    -   Fixed:
        -   Refresh Forensic Details Tab Occurring Under All Tabs and Under All Sections.
        -   Configuration tile throwing insufficient data for end user.
-   **Version 1.0.1 - February 2025**

    Security Incident Response integration with Proofpoint allows security operations center \(SOC\) analysts to generate ServiceNow AI Platform Security Incident Response \(SIR\) incidents automatically when certain configured ProofPoint Events are captured.Analysts respond to the security incidents that are created with workflows in the ServiceNow AI Platform that automate incident response activities and remediation.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

