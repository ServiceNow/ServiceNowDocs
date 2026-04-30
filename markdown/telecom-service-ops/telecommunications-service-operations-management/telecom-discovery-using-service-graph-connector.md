---
title: Indirect Discovery using Service Graph Connectors
description: ServiceNow Telecom Discovery using Service Graph Connectors \(SGCs\) enables you to seamlessly integrate network infrastructure data from external management systems—such as EMS, NMS, and SDN Controllers—into the Configuration Management Database \(CMDB\).
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Indirect Discovery using Service Graph Connectors

ServiceNow Telecom Discovery using Service Graph Connectors \(SGCs\) enables you to seamlessly integrate network infrastructure data from external management systems—such as EMS, NMS, and SDN Controllers—into the Configuration Management Database \(CMDB\).

This approach helps Communication Service Providers \(CSPs\) maintain a current and accurate view of their multivendor telecom network resources, services, and configurations.

By leveraging predefined connectors and robust data transformation tools, you can unify your inventory across domains and ensure that the CMDB and Telecom Network Inventory \(TNI\) reflect real-time network insights aligned with your telecom data model.

**Note:** Telecom Service Graph Connectors are part of the TSOM Visibility subscription and extend the capabilities of the standard Service Graph Connector framework.

## Service Graph Connector overview

With Telecom SGC, you can:

-   Ingest data from EMS/NMS/Controllers using northbound REST APIs.
-   Automatically populate and update CMDB and TNI records with enriched, telecom-aligned data.
-   Reconcile incoming data with existing CI records using the Identification and Reconciliation Engine \(IRE\).
-   Generate TNI entity records automatically when the TNI plugin is installed.
-   Support discrepancy detection and remediation as part of Telecom Discrepancy Identification &amp; Reconciliation.
-   Use low-code tools to configure, test, and manage your integrations end-to-end.

## Architecture overview

Telecom Service Graph Connectors rely on a modular and scalable architecture:

<table id="table_nvz_34q_vfc"><thead><tr><th>

Component

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Service Graph Connector

</td><td>

Defines the integration logic to extract and stage data from EMS/NMS systems \(for example, Nokia Altiplano or Nokia NSP\).

</td></tr><tr><td>

MID Server

</td><td>

Acts as a secure bridge between your ServiceNow instance and the external network system. For more information, see [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

IntegrationHub ETL \(3.2\)

</td><td>

Provides a guided UI for creating, testing, and managing ETL transform maps.For more information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Robust Transform Engine \(RTE\)

</td><td>

Transforms staged source data into CMDB-compliant records using defined ETL logic. For more information, see [Create a robust import set transformer](https://www.servicenow.com/docs/access?context=create-robust-import-set-transformer&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Identification and Reconciliation Engine \(IRE\)

</td><td>

Ensures data consistency and prevents duplicates by identifying and reconciling CIs.For more information, see the [CMDB Identification and Reconciliation \(IRE\)](https://www.servicenow.com/docs/access?context=c_CMDBIdentifyandReconcile&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

CMDB/TNI

</td><td>

Stores structured, accurate telecom infrastructure data for visibility and downstream processes.

</td></tr></tbody>
</table>## Supported Service Graph Connectors

-   Nokia Altiplano SGC \(sn\_sgc\_altiplano\_connector\): Integrates with the Nokia Altiplano Access Network SDN Controller via REST APIs.

**Note:** The connector can coexist with IT and Cloud Service Graph Connectors \(e.g., for servers, monitoring tools, IoT, etc.\).

## Key benefits

-   Fast time to value – Use predefined, supported connectors that require minimal configuration.
-   Multivendor support – Integrate with various management platforms across access, core, and transport networks.
-   Model-aligned visibility – Ensure telecom-specific hierarchy and relationships are accurately modeled in the CMDB.
-   Discrepancy detection ready – Feed network data directly into Telecom Discrepancy Identification &amp; Reconciliation for CMDB compliance.
-   Scalable integration – Leverage ServiceNow’s proven integration framework built for performance and extensibility.

## Telecom Network Inventory \(TNI\) data model

Telecom SGCs include logic to ensure compatibility with the Telecom Network Inventory \(TNI\) data model:

-   When the TNI plugin is installed, each discovered network element automatically includes a TNI entity record.
-   A `tni_entity` is created alongside its corresponding `cmdb_ci` record, using system-generated payload mappings \(e.g., `inventory_category`\).
-   This ensures consistency across operational and planning systems.

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

**Related topics**  


[Telecom Discovery via Nokia Altiplano](service-graph-connector-for-nokia-altiplano.md#)

