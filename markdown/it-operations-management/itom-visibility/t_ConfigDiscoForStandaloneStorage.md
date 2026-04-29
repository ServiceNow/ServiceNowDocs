---
title: Configure SMI-S Provider for storage Discovery
description: Use this procedure for configuring a standalone storage device with the required SMI-S Provider for Discovery.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Storage Discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Configure SMI-S Provider for storage Discovery

Use this procedure for configuring a standalone storage device with the required SMI-S Provider for Discovery.

## Before you begin

Role required: admin

## Procedure

1.  On the storage device, if the SMI-S Provider is not present, install the SMI-S Provider software.

    The SMI-S Provider software is often part of the device management software. For more information, download the SMI-S Provider instructions from the storage provider manufacture.

2.  For NetApp storage devices, [install the SMI-S agent](https://www.servicenow.com/docs/access?context=r_CIMCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) on the storage device host.

    **Note:** Discovery can also perform native discovery of NetApp servers without accessing the SMI-S server. See [NetApp Server and Cluster discovery](../concept/netapp-discovery.md) for more information.

3.  Start the SMI-S Provider service.

4.  In the SMI-S Provider or agent, configure the **Discovery Interval** with a synchronization rate that allows the wbem probe to receives the most current information during discovery.

5.  On the ServiceNow instance, set up [CIM credentials](https://www.servicenow.com/docs/access?context=r_CIMCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

6.  Create a Discovery Schedule with the IP addresses of each SMI-S Provider.

7.  Create a [Discovery behavior](../concept/c_DiscoveryBehaviors.md) that uses a functionality definition with a **wbem** port probe to make the initial port-scanning phase \(Shazzam\) more efficient.

8.  Run a basic IP address Discovery.


**Parent Topic:**[Storage Discovery via SMI-S and CIM](../reference/r_DataCollDiscoStorageviaSMISCIM.md)

