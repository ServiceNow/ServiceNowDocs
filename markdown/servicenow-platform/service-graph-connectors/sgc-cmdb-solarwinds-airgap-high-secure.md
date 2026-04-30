---
title: Configure air gap solution for Service Graph Connector for SolarWinds in a high-secure server
description: Configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure server.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 2
breadcrumb: [Configuring air gap connections, SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure air gap solution for Service Graph Connector for SolarWinds in a high-secure server

Configure the air gap solution for the Service Graph Connector for SolarWinds in your high-secure server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **SolarWinds** &gt; **Setup** &gt; **Add Multiple Instances** &gt; **Add Another Connection**.

2.  Download the `SgSolarWindsHighSecureSetup.ps1` and `GetSolarWindsData.ps1` PowerShell scripts from the link provided in the Add Another Connection section.

3.  Log on to your high-secure server.

4.  Create a SolarWinds directory.

    All the configurations required for the air gap solution are created in the SolarWinds directory.

5.  Copy the `GetSolarWindsData.ps1` and `SgSolarWindsHighSecureSetup.ps1` PowerShell scripts that you downloaded in step [2](sgc-cmdb-solarwinds-airgap-high-secure.md#download-high-secure-ps-scripts) to the SolarWinds directory.

6.  Start a PowerShell session, and run the `SgSolarWindsHighSecureSetup.ps1` script to generate the JSON configuration file that is used by the `GetSolarWindsData.ps1` script.

    1.  At the prompt, enter the path for the SolarWinds directory that you created in step [4](sgc-cmdb-solarwinds-airgap-high-secure.md#step_otv_xyt_42c).

    2.  Enter a name for the configuration file, or press the Return key to accept the default value.

    3.  Enter the values for the global properties, or press the Return key to accept the default values.

        -   **npmInstalled**: Set the value to `true` if the module is installed on the SolarWinds instance. Set the value to `false` if the module isn't installed on the SolarWinds instance.
        -   **samInstalled**: Set the value to `true` if the module is installed on the SolarWinds instance. Set the value to `false` if the module isn't installed on the SolarWinds instance.
        -   **pageSize**: Enter the number of records to be fetched in a SolarWinds API call.
        -   **endpoint**: Update the **Host** field with the host name for your SolarWinds instance.
        -   **port**: Specify the port on which the SolarWinds instance allows API calls.
        -   **credentialsPath**: Specify the location to store the SolarWinds credentials XML file.
        -   **logDirectory**: Specify the location to store the log file from the `GetSolarWindsData.ps1` script.
    4.  Specify names for the data source data directories, or press the Return key to accept the default values.

        The directories are created if they don’t already exist.

    5.  Enter the SolarWinds credentials.

        **Note:** You can either use Windows credential manager to store the user name and password, or implement your own mechanism for storing the credentials. The `GetSolarWindsData.ps1` script must have access to the credentials to trigger REST calls.

    6.  Exit the PowerShell session.

7.  Provide write and delete permissions for the SolarWinds directory and the child directories.

    You must provide delete permissions for old records to be cleaned up.


**Related topics**  


[Configure air gap solution for Service Graph Connector for SolarWinds in a low-secure server](sgc-cmdb-solarwinds-airgap-low-secure.md)

