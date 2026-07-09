---
title: Service Graph Connector for Observability - Dynatrace SaaS release notes
description: Version history for the ServiceNow Service Graph Connector for Observability - Dynatrace SaaS application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-sgc-observability-dynatrace-saas.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Observability - Dynatrace SaaS release notes

Version history for the ServiceNow® Service Graph Connector for Observability - Dynatrace SaaS application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.0 - July 2026**
    -   New:
        -   The Dynatrace entities that are to be imported are configured using segment, replacing management zone filtering from the Classic connector.
        -   CIs that aren't observed by Dynatrace within a configurable staleness threshold are automatically retired.
        -   The classic connector migration cleanup script can be used to retire stale process CIs created by the Dynatrace Classic connector.
        -   Front-end entities are now mapped to their dependent services, improving service topology visibility in ServiceNow.
    -   Changed:
        -   Process CI names are aligned with ServiceNow Discovery conventions for MSSQL, NGINX, Apache, IIS, and WebSphere.
        -   WebSphere process CIs include cell and node attributes, improving reconciliation accuracy against Discovery data.
        -   Containerized processes are filtered out by default to reduce duplicate Application CIs.
        -   Path separator and formatting inconsistencies in Windows process paths are normalized, reducing duplicate Application CIs.
-   **Version 1.0.0 - June 2026**
    -   Service Graph Connector for Observability - Dynatrace SaaS is designed for the Dynatrace SaaS \(3rd‑generation\) platform and leverages DQL-based APIs and the modern Grail architecture to import data from Dynatrace into the Configuration Management Database \(CMDB\).
    -   The Service Graph Connector for Observability - Dynatrace SaaS imports the following data from Dynatrace to the ServiceNow CMDB:
        -   Hosts
        -   Processes
        -   Services
        -   Frontends
    -   A service map is created by mapping the relationships among various applications, application services, and infrastructure elements.
    -   Note:If you're in a Dynatrace-managed \(self‑hosted\) or legacy SaaS environment, you should use the Service Graph Connector for Observability - Dynatrace.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

