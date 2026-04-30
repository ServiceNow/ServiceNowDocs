---
title: JDBCProbe
description: A JDBC probe runs on the MID Server to query an external database via \[JDBC\] and returns results to ServiceNow.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# JDBCProbe

A JDBC probe runs on the MID Server to query an external database via \[JDBC\] and returns results to ServiceNow.

## About this task

Probes interact with the MID Server via the ECC Queue, therefore the response of a JDBC probe returns as an XML payload in an "input" ECC Queue record. By default, each response payload will contain up to 200 returned rows, this value can be modified by setting the probe parameter **jdbcprobe\_result\_set\_rows** to the desired number.

**Activating the Plugin**

Contact Customer Service and Support to activate the **Integration - JDBC** \(com.snc.integration.jdbc\) plugin.

## Procedure

1.  Navigate to **System Definition &gt; Plugins**.

2.  Right-click the plugin name on the list and select **Activate/Upgrade**.

    If the plugin depends on other plugins, these plugins and their activation status are listed.

3.  Select the **Load demo data** check box.

    Some plugins include demo data—sample records that are designed to illustrate plugin features for common use cases. Loading demo data is a good policy when first activating the plugin on a development or test instance. You can load demo data after the plugin is activated by repeating this process and selecting the check box.

4.  Click **Activate**.


-   **[Direct JDBC Probe](../concept/c_DirectJDBCProbe.md)**  
A direct JDBC probe specifies all the parameters necessary in the outbound ECC Queue XML payload.
-   **[JDBC Probes via Data Source](../concept/c_JDBCProbesViaDataSource.md)**  
JDBC probes are executed via a JDBC data source when an import is running against the data source.
-   **[Select \* JDBC Probe short cut](../concept/c_SelectJDBCProbeShortCut.md)**  
Alternatively, you may specify a **table\_name** parameter instead of a work element and the following query could be executed.
-   **[Parameters](../reference/r_DirectJDBCProbeParameters.md)**  
The following parameters are available in a direct JDBC probe.
-   **[Using the Work Element](../concept/c_UsingTheWorkElement.md)**  
The work element encodes SQL statements to be executed by the probe.

**Parent Topic:**[Supported integration interfaces](../../vendor-specific-integrations/reference/r_SupportedIntegrationInterfaces.md)

