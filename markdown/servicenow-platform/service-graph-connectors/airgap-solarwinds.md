---
title: Configuring air gap connections for Service Graph Connector for SolarWinds
description: Air gap connections for the Service Graph Connector for SolarWinds enable safe and controlled data transfer without compromising security.​
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring air gap connections for Service Graph Connector for SolarWinds

Air gap connections for the Service Graph Connector for SolarWinds enable safe and controlled data transfer without compromising security.​

An air gap is a security measure that involves isolating a computer or network and preventing it from establishing an external connection. Air-gapped networks keep critical systems secure by isolating them from external connections to protect the systems from cyber threats. Air gap connections for the Service Graph Connector for SolarWinds facilitate controlled data exchange between the air-gapped networks and external systems while maintaining the integrity of the air-gapped environment.

Air gap connections are available from version 2.5.0 of the Service Graph Connector for SolarWinds. You can add either regular data sources or air gap data sources during the guided setup. To access the guided setup, see [Configure Service Graph Connector for SolarWinds](../task/configure-solarwinds-integration.md).

Perform the following sequence of tasks to configure the air gap solution before you add air gap data sources during the guided setup:

1.  [Configure air gap solution for Service Graph Connector for SolarWinds in a high-secure server](../task/sgc-cmdb-solarwinds-airgap-high-secure.md)
2.  [Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server](../task/sgc-cmdb-solarwinds-airgap-low-secure.md)
3.  [Configure air gap solution for Service Graph Connector for SolarWinds in a ServiceNow instance](../task/sgc-cmdb-solarwinds-airgap-sn-instance.md)
4.  [Perform a test data load for the air gap solution for Service Graph Connector for SolarWinds](../task/sgc-cmdb-solarwinds-airgap-test-load.md)
5.  [Perform a full data load for the air gap solution for Service Graph Connector for SolarWinds](../task/sgc-cmdb-solarwinds-airgap-data-load.md)

