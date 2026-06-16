---
title: Splunk Search integration for Security Operations release notes
description: Version history for the Splunk Search integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-splunk-search.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Splunk Search integration for Security Operations release notes

Version history for the Splunk Search integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.0 - August 2025**

    New: Enhance SIR sighting search functionality by integrating saved searches into sighting links, streamlining navigation to associated Splunk queries and improving user experience.

-   **Version 10.4.11 - March 2025**

    Fixed: During the integration configuration if the user leaves the Link URL field blank, Splunk fails to authenticate even though the field is optional.

-   **Version 10.4.10 - November 2024**

    Changed: Migration of Workflows to Flow Designer flows.

-   **Version 10.4.5 - February 2023**
    -   Changed: Added support for analyst workspace.
    -   Fixed: Splunk sighting saved searches are not working without the MID server.
-   **Version 10.4.1 - November 2022**
    -   Fixed:
        -   Link URL is not mandatory in the configuration tile.
        -   Sighting search was failing though token-based authentication was enabled.
        -   In the case of more than one MID server, if one of the MID servers was down, the sighting search was failing most of the time.
-   **Version 10.4.0 - December 2021**

    Changed: You can now set-up the Splunk Search Integration for Security Operations without deploying the MID server since both ServiceNow and Splunk Cloud are cloud products.

-   **Version 10.3.0 - June 2020**

    New: Implementation Flow to support the new capability framework \(v2.0\)


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

