---
title: Security Incident Response integration with Microsoft Defender for Endpoint release notes
description: Version history for the Security Incident Response integration with Microsoft Defender for Endpoint on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-ms-defender.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response integration with Microsoft Defender for Endpoint release notes

Version history for the Security Incident Response integration with Microsoft Defender for Endpoint on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.5 - June 2026**
    -   Fixed:
        -   The Isolate Host action failing with the error "No Machine id found for given CI".
        -   Implemented fixes related to Cobalt Raven Non-Glide Query ACL directives, ensuring proper ACL enforcement for non-Glide query operations.
-   **Version 1.3.4 - April 2026**

    New: Capability to Allow/Block Observables from Security Incidents such as domains, IP addresses, files, URLs using Microsoft Defender for Endpoint.

-   **Version 1.2.4 - March 2026**

    Fixed: Handled special characters in hostname field.

-   **Version 1.2.1 - February 2026**

    Fixed: Malformed URL errors by properly handling special characters in hostnames during EDR machine lookup.

-   **Version 1.2.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.1.20 - October 2025**

    Fixed: Requests being built incorrectly, ensuring accurate host detail retrieval.

-   **Version 1.1.10 - August 2025**

    Fixed: Get Host Details requests being built with incorrect parameters, causing failures in retrieving accurate host information.

-   **Version 1.0.12 - June 2025**

    Fixed: Query failure due to insufficient 'query\_match' access on sn\_sec\_core\_integration\_item.sys\_scope for users with sn\_si.analyst role, impacting Defender for Endpoint integration.

-   **Version 1.0.11 - May 2025**

    Fixed: Bugs have been addressed and resolved as part of this release.

-   **Version 1.0.9 - November 2024**

    Changed: Migration of Workflows to Flow Designer flows.

-   **Version 1.0.7 - August 2024**
    -   New: Migrated workflows to flow designer for Microsoft Defender enrichment capabilities.
    -   Changed: Microsoft Defender for endpoint is now compatible to be configured for GCC environments.
-   **Version 1.0.6 - March 2024**
    -   Changed: The Comments field in the Run additional actions capability is now set as a mandatory field.
    -   Fixed:
        -   The Get Host Details and Get Logged on Users actions fail due to a large response
        -   Create indicators in Microsoft Defender endpoint action fails when a different time format was chosen than YYYY-MM-DD HH:MM:SS.
-   **Version 1.0.5 - August 2023**
    -   Changed: The MS Defender Capabilities Isolate Host and Run Antivirus scan dialogue boxes' Type field is now a drop down instead of a text.
    -   Fixed: If the machine is not found by the name field of the CI item in the Defender, you can search for the machine name using the FQDN field.
-   **Version 1.0.4 - April 2023**

    Changed: Updated to support this integration on the Security Incident Response workspace.

-   **Version 1.0.2 - February 2023**

    New: Support for Analyst workspace.

-   **Version 1.0.1 - November 2022**
    -   Fixed:
        -   Microsoft Defender for Endpoint Host Details' flow is retrieving all machine details instead of retrieving details for the required Configuration Item.
        -   POL\_ON Defender Endpoint Observable Indicator UI page is broken.
-   **Version 1.0.0 - February 2022**

    The Microsoft Defender For Endpoint enables organizations to proactively inspect, analyze, and contain known and unknown threats on any endpoint.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

