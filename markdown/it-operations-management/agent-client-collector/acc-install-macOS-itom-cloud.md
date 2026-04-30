---
title: Perform a single-line Agent Client Collector installation on macOS by using ITOM Cloud Services
description: Install Agent Client Collector on a macOS machine without a MID Server by using the ITOM Cloud Services application. When you send information through the cloud, you enable the MID Server to be used for more persistent resources.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector installation on macOS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Perform a single-line Agent Client Collector installation on macOS by using ITOM Cloud Services

Install Agent Client Collector on a macOS machine without a MID Server by using the ITOM Cloud Services application. When you send information through the cloud, you enable the MID Server to be used for more persistent resources.

## Before you begin

Install the ITOM Cloud Services plugin.

Create an agent registration key, as described in [Configure an agent registration key](agent-registration-key-configuration.md).

Role required: agent\_client\_collector\_admin

## About this task

For details on working with Cloud Services, see [DEX Architecture](https://www.servicenow.com/docs/access?context=dex-architecture&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Procedure

1.  Retrieve the agent registration key:

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.

    2.  Select the relevant agent registration key.

    3.  Copy the registration key value and store it in a place where you can easily retrieve it when needed.

2.  Retrieve the publicly accessible gateway URL, based on your location:

    -   AMER \(Americas\): `itomcnc-prod-gateway.amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway.emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway.apac.sncapps.service-now.com:443`
3.  On the server where you’re installing the Agent Client Collector, enter the following command:

    ```
    CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>" bash -c "$(curl -L https://<instance_url>/api/sn_agent/agents/install_agent)"
    ```

    The following table shows the parameter values in the command.

<table id="table_i4m_yjq_wxb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable ITOM Cloud Services. If you don't specify a value, the regular MID Server websocket installation is invoked.For details on configuring a websocket on the MID Server, see [Configure the websocket server on the MID Server](acc-configure-web-server.md).

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

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

Optional **ACC\_ALLOW\_LIST=0** string that you can add to disable the allow list.Default: The allow list is enabled.

**Note:** When you disable the allow list, you compromise your system's security. This action is intended as a temporary measure while you're updating the allow list. After you complete the update, remove **ACC\_ALLOW\_LIST=0** from the command line.

</td></tr><tr><td>

ACC\_VALIDATE\_SIG

</td><td>

Optional **ACC\_VALIDATE\_SIG=0** string that you can add to disable the verification of the installer certification validation. Default: Validation is enabled.

**Note:** Disable the certification validation only when you're using non-standard signature validation tools.

</td></tr></tbody>
</table>
**Parent Topic:**[Agent Client Collector installation on macOS system](../concept/acc-install-mac-os.md)

