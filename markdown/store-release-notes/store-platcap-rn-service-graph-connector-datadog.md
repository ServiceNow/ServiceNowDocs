---
title: Service Graph Connector for Observability - Datadog release notes
description: Version history for the Service Graph Connector for Observability - Datadog on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-datadog.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Observability - Datadog release notes

Version history for the Service Graph Connector for Observability - Datadog on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.1 - March 2026**

    Fixed: Fixed the attachment error in the host data source.

-   **Version 1.4.0 - December 2025**
    -   New: Added support for importing the dependency data of services and for creating service maps.
    -   Fixed:
        -   Fixed the issue where CIs weren't bound to events and alerts.
        -   Fixed the Host data source to bring EC2 machines.
        -   Fixed the relationship of IP Address and Network Adapter with Host.
-   **Version 1.3.0 - July 2025**
    -   New and Introduced:
        -   Pull data source for Host CIs
        -   Pull tags for Host CIs
-   **Version 1.2.1 - March 2023**
    -   The Service Graph Connector for Observability - Datadog enables customers to easily and correctly import CIs and Events from Datadog to CMDB.
    -   Connector imports the following data types from Datadog into CMDB:
        -   Servers
        -   Software Install details
        -   Process
        -   Events
        -   Application
    -   It adds the ability to configure the ingestion of events through Event Management and automatically correlates events to the discovered CIs.

