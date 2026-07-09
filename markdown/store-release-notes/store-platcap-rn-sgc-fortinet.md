---
title: Service Graph Connector for Fortinet release notes
description: Version history for the ServiceNow Service Graph Connector for Fortinet application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-sgc-fortinet.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Fortinet release notes

Version history for the ServiceNow® Service Graph Connector for Fortinet application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.9.0 - July 2026**
    -   This release enhances attribute mapping extensibility, improves device data completeness, and gives administrators greater control over performance tuning.
        -   What's new
            -   Custom attribute mapping — Operators can extend or override Fortinet device attribute mappings to TSOM records without modifying core connector code. Part of a platform-wide rollout across Fortinet, Meraki, and VeloCloud connectors.
            -   Connection URLs for discovered devices — Discovered devices now include connection URLs in TSOM for better traceability and source device linking.
            -   Configurable ETL batch size — Administrators can adjust the number of records processed per batch to match instance capacity.
        -   Issues fixed
            -   Corrected device port attribute mapping errors.
            -   Removed redundant configuration entries that could cause unexpected behavior.
        -   Before you upgrade: If your organization has customized attribute mappings, review the new extension point for a supported, upgrade-safe alternative.
        -   Other: Localization strings updated.
-   **Version 2.4.1 - June 2026**
    -   Adds Logical Interfaces Discovery
    -   Adds device attributes: High Availability mode, first tunnel up time, and ADOM ID
    -   Introduces an extension point for configuring meta fields in FortiManager API calls
    -   Improves Network Service Instance naming to align with Network Sites
    -   Updates localization strings
-   **Version 2.2.0 - May 2026**

    Identify license expiry for all devices with a single API call.

-   **Version 2.1.0 - April 2026**

    What's New: The Fortinet SGC now discovers and tracks license expiration dates for all Fortinet devices via FortiManager. Network operations teams can see upcoming renewals directly in the CMDB, reducing the risk of outages from expired licenses.

-   **Version 2.0.0 - March 2026**

    Fortinet discovery connectors

-   **Version 1.2.0 - February 2026**

    Enables discovery for Fortinet devices.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

