---
title: RISKIQ integration release notes
description: Version history for the Security Operations RISKIQ integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-riskiq.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# RISKIQ integration release notes

Version history for the Security Operations RISKIQ integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.4.1 - August 2024**

    Changed: Migrated Enrichment workflows to flow designer.

-   **Version 10.3.5 - May 2023**

    Fixed: Optional tag was missing in the capability filter XML file.

-   **Version 10.3.4 - February 2023**

    New: Added changes to support the Security Incident Response workspace.

-   **Version 10.3.2 - March 2022**

    Changed: Upgraded to the new V2 API.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support Integration capability framework v2.0

-   **Version 8.0.0 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Bug fixes
-   **Version 5.0.10 - June 2018**
    -   Automatic enrichment lookups for SSL certificate and the domain registration information are run on selected observables upon the incident creation.
    -   After the application is configured, the workflow launches automatically for RISKIQ lookups and the completion status is recorded in work notes.
    -   Observables can be looked up manually by adding them to the Security Incident form or the Observable Entry table and launching an enrichment lookup.
    -   Results are displayed in the SSL Certificates and Observable Enrichment tabs under Related Links.

