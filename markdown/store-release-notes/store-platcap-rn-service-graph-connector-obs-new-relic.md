---
title: Service Graph Connector for Observability - New Relic release notes
description: Version history for the Service Graph Connector for Observability - New Relic application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-obs-new-relic.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Observability - New Relic release notes

Version history for the Service Graph Connector for Observability - New Relic application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.1 - February 2026**

    Fixed: Fixed the issue where relationships don't exist for Calculated Application Service \[cmdb\_ci\_service\_calculated\].

-   **Version 1.4.0 - December 2025**
    -   New:
        -   Added support for building relationships between application services and hosts.
        -   Added the pagination feature for the Application data source.
        -   Added support for creating Service-to-Service relationships in the service map.
    -   Fixed: Fixed the issue where the App Service Rels import wasn't triggered by the parent import set.
-   **Version 1.3.0 - August 2025**
    -   New: Onboarded the connector to SGC Central.
    -   Fixed: Resolved issues with the ingestion of alerts and events from New Relic.
-   **Version 1.2.1 - March 2023**
    -   The Service Graph Connector for Observability - New Relic imports the following type of data from New Relic to ServiceNow CMDB:
        -   Hosts
        -   Disk
        -   Network Adapter
        -   Applications
        -   Event/Alerts
    -   It adds the ability to configure the ingestion of events through Event Management and automatically correlates events to the discovered CIs.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

