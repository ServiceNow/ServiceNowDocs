---
title: Service Graph Connector for Meraki release notes
description: Version history for the ServiceNow Service Graph Connector for Meraki application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-sgc-meraki.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Service Graph Connector for Meraki release notes

Version history for the ServiceNow® Service Graph Connector for Meraki application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 4.0.4 - September 2026**
    -   Changed: Camera and sensor relationships — Cameras and sensors discovered from Meraki are related to their network service instance in the CMDB. This relationship ensures that location data resolves correctly for these devices.
    -   New: Per-organization uplink exclusions — You can exclude specific Meraki organizations from uplink data collection.
    -   Fixed: Networks excluded from uplink collection no longer display a duplicate warning indicator.
-   **Version 3.0.5 - August 2026**
    -   Summary: The Meraki connector has been fully converted to the Fluent SDK \(Now SDK\) TypeScript format, with new API discovery extension points, per-network API call toggles, licensing model support for Organization CIs, and Network Service Instance relationships for sensors and cameras.
    -   Features &amp; Enhancements:
        -   The Meraki connector has been fully migrated from legacy XML to the Now SDK \(Fluent\) TypeScript format, enabling modern source-controlled development and CI/CD builds. Script includes, ACLs, scheduled jobs, and system properties are now authored in TypeScript.
        -   Extension points for new Meraki API discovery have been added, allowing the connector to discover and collect data from additional Meraki API endpoints as they become available.
        -   New system properties, including sn\_tsom\_meraki.disable\_per\_network\_api\_callsand a rate-limit toggle, allow administrators to disable per-network API calls, reducing API consumption for large Meraki deployments with many networks.
        -   Licensing model information is now collected and stored as a key-value pair on Meraki Organization CIs, providing visibility into the licensing tier \(e.g., co-term, per-device\) for each organization.
        -   Network Service Instance relationships are now created for Meraki sensors and cameras, linking these devices to their parent network service for improved topology visibility in CMDB.
-   **Version 2.9.0 - July 2026**
    -   This release improves device data accuracy, adds flexibility for custom attribute mapping, and introduces batch processing controls for large-scale deployments.
        -   What's new
            -   Custom attribute mapping — Operators can define how Meraki device attributes map into TSOM without modifying core connector code. Customizations are upgrade-safe and compatible with existing workflows. Part of a coordinated rollout across Fortinet and VeloCloud connectors.
            -   Orchestrator URL in device records — The Meraki Orchestrator URL is now surfaced in device metadata, enabling direct navigation from TSOM records to the Meraki dashboard for faster troubleshooting and audit tracing.
            -   Accurate network identification — Network keys and display names now align with Meraki's official network taxonomy, reducing discrepancies between TSOM and actual network configurations.
        -   Issues fixed
            -   Configurable batch size for large environments — A hardcoded discovery sync batch limit that caused timeouts in deployments exceeding 500 devices has been replaced with an administrator-configurable system property.
            -   Localization strings updated.
-   **Version 2.4.1 - June 2026**
    -   New:
        -   Adds license expiration date tracking for co-term organizations
        -   Adds a device inventory field: claimed at date
    -   Fixed:
        -   Fixes site import reliability — corrects address default value
        -   Fixes organization data handling with a null org\_id guard
    -   Changed: Updates localization strings
-   **Version 2.2.0 - May 2026**

    Updates in this release improve the accuracy and consistency of Meraki Discovery performance test results. The application has been renamed to Service Graph Connector for Meraki Telco SD-WAN to better reflect its purpose and scope.

-   **Version 2.1.0 - April 2026**
    -   What's Changed:
        -   Automated ETL duplication for connectors: Connector apps previously required manual copying of ETL definitions from TSOM Core on install or upgrade. This is now fully automated — connectors self-update their ETL configuration without any manual steps.
        -   Improved resilience for connectors: Connectors now handle missing or null values returned by vendor APIs more gracefully. Instead of failing on incomplete API responses, connectors apply sensible defaults and continue processing, improving data reliability in CMDB and reducing connector errors.
-   **Version 2.0.0 - March 2026**

    Service Graph Connector for Cisco Meraki release notes.

-   **Version 1.1.3 - February 2026**

    This application contains connectors for Cisco Meraki discovery, alerts, and performance data collection. These connectors integrate with Cisco Meraki systems to enable real-time monitoring, automated alerting, and performance analysis.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

