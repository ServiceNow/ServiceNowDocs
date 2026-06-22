---
title: Telecom Discovery using Service Graph Connectors \(SGC\)
description: Service Graph Connectors are predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources \(for example, northbound APIs of EMS/NMS/Controllers, which manage various xNFs\) across different network domains, while enabling a structured, telecom-model-aligned view of network resources and services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/telecom-service-ops/telecom-visibility/telecom-discovery-using-service-graph-connector.html
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Telecom Discovery using Service Graph Connectors \(SGC\)

Service Graph Connectors are predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources \(for example, northbound APIs of EMS/NMS/Controllers, which manage various xNFs\) across different network domains, while enabling a structured, telecom-model-aligned view of network resources and services.

They can be used alongside any existing Service Graph Connectors, such as those for security, servers, software, monitoring, internet of Things \(IoT\), and cloud.

## Architecture using Telecom Service Graph Connectors

This is an example of the implementation for the Nokia Altiplano Service Graph Connector. The architecture of other connectors may vary.

\[Omitted image "telecom-architecture-sgc.png"\] Alt text: discovery and reconciliation architecture.

## IntegrationHub ETL \(3.2\)

This store app to create and manage ETL transform maps, which integrate third-party data into the CMDB or into non-CMDB tables without compromising the integrity of data. IntegrationHub ETL provides a simplified user interface that guides you through the integration process end-to-end, including a test integration run of sample data.

For more information, see [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md).

## Robust Transform Engine \(RTE\)

This plugin is used to transform raw source data that is stored in staging tables, into the data that is mapped and integrated into the CMDB. RTE uses ETL transform maps that were created for integration during data transformation.

For more information, see [Create a robust import set transformer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/create-robust-import-set-transformer.md).

## MID Server

MID Server is a Java application that runs as a Windows service or UNIX daemon on a server within your local network. The ServiceNow® MID Server facilitates communication and data transfer between a ServiceNow instance and external applications, data sources, and services.

For more information, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-server/mid-server-landing.md).

## Identification &amp; Reconciliation Engine \(IRE\)

IRE offers a centralized framework for identifying and reconciling data from multiple sources. It confirms the integrity of the CMDB and some non-CMDB tables when various data sources are used to create or update CI records.

For more information, see the [CMDB Identification and Reconciliation \(IRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/c_CMDBIdentifyandReconcile.md).

## CMDB Compliance Certification Audits for Telecom Discrepancy Identification &amp; Reconciliation

[CMDB Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/c_Compliance.md) is a toolset that enables administrators to certify CMDB data for accuracy and resolve any discrepancies found. In Telecom Discrepancy Identification &amp; Reconciliation, we use the [Certification audits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/c_CertificationAudits.md) feature to discover and analyze discrepancies in the CMDB, generate [Certification follow-on tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/configuration-management-database-cmdb/c_CertificationFollowOnTasks.md), and enable remediation workflows.

For more information on how it’s used for Discrepancy Identification &amp; Reconciliation, see [Telecom Discrepancy Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-service-ops/telecom-visibility/telecom-reconciliation.md).

## TNI Entity Creation Logic

Whenever the system identifies that the customer has TNI installed, it will automatically create a TNI entity record for all network data discovered.

If TNI is installed, a payload like the following one will be added to the IRE payload for each item \(with inventory\_category populated based on the className\):

```
related = [{
            "className": "tni_entity",
            "values": {
                "inventory_category": ""
            }
        }];

```

As a result, the discovered CI is in both the cmdb\_ci and tni\_entity tables.

## Telecom Service Graph Connectors supported

[Service Graph Connector for Nokia Altiplano](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-service-ops/telecom-visibility/service-graph-connector-for-nokia-altiplano.md).

See other available [Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md).

## Supported versions

Supported ServiceNow® versions: Yokohama and beyond.

-   **[Service Graph Connector for Nokia Altiplano](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-service-ops/telecom-visibility/service-graph-connector-for-nokia-altiplano.md)**  
Use the Service Graph Connector for Nokia Altiplano Access Network SDN Controller to pull in data from the Nokia Altiplano software into your ServiceNow instance using REST APIs.
-   **[Configure Service Graph Connector for Nokia Altiplano](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-service-ops/telecom-visibility/configuring-service-graph-connector-nokia-altiplano.md)**  
This document explains how to configure the Service Graph Connector for Nokia Altiplano using Guided setup to integrate network resource data from the Nokia Altiplano Access Controller \(REST API\) into the ServiceNow CMDB. It includes steps for setup, authentication, and scheduling to confirm accurate integration of network data.

**Parent Topic:**[Exploring Telecom Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/telecom-service-ops/telecom-visibility/exploring-telecom-discovery.md)

