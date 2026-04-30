---
title: Configure air gap solution for Service Graph Connector for SolarWinds in a ServiceNow instance
description: Configure the air gap solution for the Service Graph Connector for SolarWinds in your ServiceNow instance after you finish the configuration in your high-secure and low-secure servers.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Configuring air gap connections, SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure air gap solution for Service Graph Connector for SolarWinds in a ServiceNow instance

Configure the air gap solution for the Service Graph Connector for SolarWinds in your ServiceNow instance after you finish the configuration in your high-secure and low-secure servers.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**, and download the `ServiceNow IntegrationHub Action Step – PowerShell` plugin.

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **SolarWinds** &gt; **Setup** &gt; **Add Multiple Instances** &gt; **Add Another Connection**.

3.  Select the **Add Another Connection** task, and then select **Configure**.

4.  In the Select Data Source Type section, select **Airgap Data Sources**, and then select **Add Connection**.

5.  Fill in the fields on the Create Connection form.

<table id="table_uvm_yh2_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Display name for the connection.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server that you deployed in your low-secure server.You can obtain the **sys\_id** of the MID Server from the ecc\_agent table.

</td></tr><tr><td>

Parent Directory

</td><td>

Path of the SolarWinds directory where the data is stored in your low-secure server.See [Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server](sgc-cmdb-solarwinds-airgap-low-secure.md).

</td></tr><tr><td>

Archive Data After Retrieval

</td><td>

Option to archive data after retrieval.

</td></tr><tr><td>

Archive Path \[Optional\]

</td><td>

Folder where the data is to be archived if the **Archive Data After Retrieval** check box is selected.

</td></tr></tbody>
</table>6.  Select **Create Connection**.


**Related topics**  


[Perform a test data load for the air gap solution for Service Graph Connector for SolarWinds](sgc-cmdb-solarwinds-airgap-test-load.md)

