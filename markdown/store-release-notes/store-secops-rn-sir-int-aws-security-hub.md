---
title: Security Incident Response integration with AWS SecurityHub release notes
description: Version history for the Security Incident Response integration with AWS SecurityHub application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-int-aws-security-hub.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response integration with AWS SecurityHub release notes

Version history for the Security Incident Response integration with AWS SecurityHub application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.2 - June 2026**

    Fixed: Added OOB field translations for Priority, Category and Configuration Item fields.

-   **Version 1.1.1 - May 2026**
    -   Fixed:
        -   SIRs are not created from SIEM ingestion due to "Secure Notes" access issue to Crypto module since Yokohama upgrade is fixed.
        -   Access issues for Security Analyst on querying tables.
-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.0.3 - August 2025**

    Fixed: Blank SIR's getting created due to gr.update in Process Raw Data.

-   **Version 1.0.2 - March 2025**

    Fixed: Version 1.0.2 of "Security Incident Response integration with AWS SecurityHub" includes a bug fix.

-   **Version 1.0.1 - November 2024**

    AWS Security Hub integration with Security Incident Response is a new SIEM integration. The AWS Security Hub integration enables SIR to ingest Security Hub findings and create corresponding security incidents.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

