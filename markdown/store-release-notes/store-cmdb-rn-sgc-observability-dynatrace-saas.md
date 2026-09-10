---
title: Service Graph Connector for Observability - Dynatrace SaaS release notes
description: Version history for the ServiceNow Service Graph Connector for Observability - Dynatrace SaaS application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-sgc-observability-dynatrace-saas.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Service Graph Connector for Observability - Dynatrace SaaS release notes

Version history for the ServiceNow® Service Graph Connector for Observability - Dynatrace SaaS application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.0 - September 2026**
    -   New:
        -   The following new Kubernetes entities are ingested into the CMDB: Container, Cluster, Namespace, Node, Pod, Service, and Workload.
        -   Kubernetes data sources can now run on their own schedule, decoupled from the Host job, so Kubernetes data can be pulled at a different and more frequent cadence than core entities data.
        -   Kubernetes data sources use a new, configurable, hours-based initial-fetch window \(default: 2 hours\) for the first sync, preventing large historical pulls on the initial run.
        -   Kubernetes payloads that exceed the platforms inline processing limit \(observed up to ~132 MB\) can be now saved as an attachment, preventing import failures in large Kubernetes environments.
        -   Kubernetes labels and annotations are now imported and preserved as CI tags.
        -   A new SGC Central activity step is available for migrating from the Classic connector to the new connector.
        -   Kubernetes Pods and Containers are automatically marked absent in CMDB.
    -   Changed:
        -   Hosts, Processes, Frontends, and Services from Dynatrace are now automatically marked as retired based on the last seen window from Dynatrace. This window can be configured in the ci\_retirement\_threshold\_days connection property.
        -   Process CI reconciliation against Discovery has been improved across DB2, MSSQL, Apache, NGINX, IIS, and PostgreSQL, reducing duplicate process CIs.
    -   Fixed:
        -   The connector now links existing VM CIs to their Server CI using object ID matching, instead of creating a duplicate VM CI.
        -   Dynatrace DQL query is optimized to improve overall data loading performance.
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

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

