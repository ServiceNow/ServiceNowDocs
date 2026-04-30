---
title: Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server
description: Configure the air gap solution for the Service Graph Connector for SolarWinds in your low-secure server after you finish the configuration in your high-secure server.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Configuring air gap connections, SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server

Configure the air gap solution for the Service Graph Connector for SolarWinds in your low-secure server after you finish the configuration in your high-secure server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **SolarWinds** &gt; **Setup** &gt; **Add Multiple Instances** &gt; **Add Another Connection**.

2.  Download the `SgSolarWindsLowSecureSetup.ps1` PowerShell script from the link provided in the Add Another Connection section.

3.  Log on to your low-secure server.

4.  Create a SolarWinds directory.

    All the configurations required for the air gap solution are created in the SolarWinds directory.

5.  Copy the `SgSolarWindsLowSecureSetup.ps1` PowerShell script that you downloaded in step [2](sgc-cmdb-solarwinds-airgap-low-secure.md#download-low-secure-ps-script) to the SolarWinds directory.

6.  Start a PowerShell session, and run the `SgSolarWindsLowSecureSetup.ps1` script.

    1.  At the prompt, enter the path for the SolarWinds directory that you created in step [4](sgc-cmdb-solarwinds-airgap-low-secure.md#step_zb4_k22_p2c).

    2.  Specify names for the data source data directories, or press the Return key to accept the default values.

        The directories are created if they don’t already exist.

    3.  Exit the PowerShell session.

7.  Provide read and delete permissions for the SolarWinds directory.


**Related topics**  


[Configure air gap solution for Service Graph Connector for SolarWinds in a ServiceNow instance](sgc-cmdb-solarwinds-airgap-sn-instance.md)

