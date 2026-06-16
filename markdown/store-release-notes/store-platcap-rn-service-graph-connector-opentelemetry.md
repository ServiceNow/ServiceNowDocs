---
title: Service Graph Connector for OpenTelemetry release notes
description: Version history for the Service Graph Connector for OpenTelemetry application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-opentelemetry.html
release: store
topic_type: reference
last_updated: "2024-05-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for OpenTelemetry release notes

Version history for the Service Graph Connector for OpenTelemetry application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.1 - May 2024**

    New: Added the ability to perform delta loads in between full loads. A step has been added to the guided setup to enable scheduling incremental imports. It is suggested to schedule incremental or delta loads to run no more frequently than once every 15 minutes.

-   **Version 1.3.0 - December 2023**
    -   New: Added mapping of a Kubernetes cluster UID from OpenTelemetry to the corresponding CMDB attribute in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table.
    -   Changed:
        -   Updated references of "Lightstep" to "CloudObs" in various places.
        -   Updated link on alert rule to read as "Cloud Observability" instead of "OpenTelemetry."
        -   Updated the guided setup to include the Cloud Observability setup instructions in the ServiceNow Cloud Observability setup \[KB1527588\] article in the Now Support Knowledge Base.
-   **Version 1.2.0 - July 2023**
    -   The Service Graph Connector for OpenTelemetry is a solution developed by ServiceNow to provide visibility into cloud-native applications and Kubernetes environments. It leverages OpenTelemetry data and the ServiceNow Cloud Observability platform \(formerly Lightstep\) to map service dependencies across platforms and discover Kubernetes infrastructure
    -   By analyzing both metrics and traces, the Service Graph Connector for OpenTelemetry can infer your service topology accurately, automatically, and in near real-time. SRE and Operations teams can better predict the impact of planned changes or reduce MTTR when incidents occur
    -   Leveraging OpenTelemetry data, this Service Graph Connector does not require a proprietary agent other than the OpenTelemetry collector itself \(open source\). This solution adheres to the Common Service Data Model, ensuring that your CMDB data is populated for optimal use in your ServiceNow workflows.
    -   This integration imports the following type of data from OpenTelemetry to ServiceNow CMDB, via ServiceNow Cloud Observability backend:
        -   Application Services
        -   Service Relationships
        -   Kubernetes objects \(cluster, name space,workload,node, pods, containers, container images\) and services
    -   This Service Graph Connector also supports the ability to configure the ingestion of ServiceNow Cloud Observability Alerts through Event Management and automatically correlate them to the discovered CIs

