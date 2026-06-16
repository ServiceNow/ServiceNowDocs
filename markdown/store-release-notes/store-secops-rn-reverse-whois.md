---
title: Reverse Whois integration release notes
description: Version history for the Security Operations Reverse Whois integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-reverse-whois.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Reverse Whois integration release notes

Version history for the Security Operations Reverse Whois integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to improve security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.4.0 - August 2024**

    Changed: Migrated enrichment workflows to flow designer.

-   **Version 10.3.6 - November 2023**

    Fixed: Optional tag was missing in the capability filter XML file.

-   **Version 10.3.4 - May 2023**

    Fixed: Implemented Table Cleaner rules for high impact/churn ServiceNow-owned tables from Security Incident Response for the Reverse WHOIS integration.

-   **Version 10.3.2 - February 2023**

    New: Updated to support Security Incident Response workspace.

-   **Version 10.3.1 - November 2022**

    Fixed: Error when Run Observable Enrichment is triggered from the Observable form view.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support Integration capability framework v2.0

-   **Version 8.0.3 - June 2019**

    Update to the WhoisXML API key and configuration steps for the integration. Obtain a new API key from the WhoisXML API website and refer to the updated configuration steps in the store documentation for the Reverse Whois integration.

-   **Version 5.0.11 - October 2018**
    -   Updated release of the Reverse Whois integration fixes situations where duplicate results are being reported.
    -   Supports the latest London release.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

