---
title: Install Agent Client Collector on Windows using ITOM Cloud Services
description: Install Agent Client Collector on a Windows machine without a MID Server by using ITOM Cloud Services. When you send information through the cloud, you enable the MID Server to be used for more persistent resources.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector installation on a Windows machine, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Install Agent Client Collector on Windows using ITOM Cloud Services

Install Agent Client Collector on a Windows machine without a MID Server by using ITOM Cloud Services. When you send information through the cloud, you enable the MID Server to be used for more persistent resources.

## Before you begin

Install the ITOM Cloud Services plugin \(sn\_itom\_cloud\_svc\).

Create an agent registration key, as described in [Configure an agent registration key](agent-registration-key-configuration.md).

Role required: agent\_client\_collector\_admin

## About this task

For details on working with Cloud Services, see [DEX Architecture](https://www.servicenow.com/docs/access?context=dex-architecture&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Procedure

1.  Retrieve the publicly accessible gateway URL, based on your location:

    -   AMER \(Americas\): `itomcnc-prod-gateway.amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway.emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway.apac.sncapps.service-now.com:443`
2.  On the Windows server where the agent is installed, enter the following command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>"
    ```

3.  The following table shows the parameter values in the command.

<table id="table_q2g_1pz_xxb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable ITOM Cloud Services \(**true**\). If you don't specify a value, the regular MID Server websocket installation is invoked.For details on configuring a websocket on the MID Server, see [Configure the websocket server on the MID Server](acc-configure-web-server.md).

</td></tr><tr><td>

ACC\_CNC

</td><td>

Public gateway endpoint for Agent Client Collector that you can specify.

</td></tr><tr><td>

REGISTRATION\_KEY

</td><td>

Active and valid agent registration key for the agent to communicate with.

</td></tr><tr><td>

INSTANCE\_URL

</td><td>

ServiceNow instance that the agent is registering with.

</td></tr></tbody>
</table>
**Parent Topic:**[Agent Client Collector installation on a Windows machine](../concept/acc-windows-install-concept.md)

