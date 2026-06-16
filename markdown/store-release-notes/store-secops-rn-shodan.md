---
title: Shodan integration release notes
description: Version history for the Security Operations Shodan integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-shodan.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Shodan integration release notes

Version history for the Security Operations Shodan integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.4.1 - August 2024**

    Changed: Migrated Enrichment workflow to subflow.

-   **Version 10.3.4 - May 2023**

    Fixed: Optional tag is missing in the capability filter xml file, which is now fixed.

-   **Version 10.3.2 - February 2023**

    New: Added changes to support the Security Incident Response workspace.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support the new capability framework \(v2.0\)

-   **Version 1.0.0 - February 2018**
    -   Automatic enrichment lookups are run on selected observables upon incident creation.
    -   After the application is configured, the workflow launches automatically, and Shodan lookup execution and completion status is recorded in work notes.
    -   Observables can be looked up manually by adding them to the Security Incident form and launching workflows.
    -   Results are displayed in the Network Banners and Observable Enrichment tabs under Related Links.

