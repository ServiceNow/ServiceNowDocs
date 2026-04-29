---
title: Configuring air gap connections for Microsoft SCCM
description: The Service Graph Connector for Microsoft SCCM supports an air gap solution for networks that are configured in a manner that doesn't support a MID agent.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring air gap connections for Microsoft SCCM

The Service Graph Connector for Microsoft SCCM supports an air gap solution for networks that are configured in a manner that doesn't support a MID agent.

An air gap is a security measure that involves isolating a computer or network and preventing it from establishing an external connection. Air-gapped networks keep critical systems secure by isolating them from external connections to protect the systems from cyber threats. Air gap connections for the Service Graph Connector for Microsoft SCCM enable controlled data transfer for Microsoft SCCM instances that are deployed to a subnet that neither has internet access nor is reachable by a MID Server agent.

Air gap connections are available from version 3.7.0 of the Service Graph Connector for Microsoft SCCM. You can add either standard data sources or air gap data sources by using SGC Central. To access the SGC Central setup, see [Configure Service Graph Connector for Microsoft SCCM using SGC Central](../../sgc-central/task/sgcc-configure-sccm-integ.md).

The air gap solution for the Service Graph Connector for Microsoft SCCM is presented in the architecture diagram.

![](../image/sgc-sccm-airgap-arch.png)

Perform the following sequence of tasks to configure the air gap solution before you add air gap data sources:

1.  [Configure air gap solution for Microsoft SCCM in a high-secure server](../task/sgc-sccm-airgap-high-secure.md)
2.  [Configure air gap solution for Microsoft SCCM in a low-secure server](../task/sgc-sccm-airgap-low-secure.md)
3.  [Configure air gap solution for Microsoft SCCM in a ServiceNow instance](../task/sgc-sccm-airgap-sn-instance.md)
4.  [Perform a test data load for the air gap solution for Microsoft SCCM](../task/sgc-sccm-airgap-test-load.md)
5.  [Perform a full data load for the air gap solution for Microsoft SCCM](../task/sgc-sccm-airgap-data-load.md)

