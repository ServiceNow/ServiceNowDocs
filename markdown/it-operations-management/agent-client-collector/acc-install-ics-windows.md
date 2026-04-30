---
title: Install MID-less Agent Client Collector using a single-line command in a Windows environment
description: Install MID-less Agent Client Collector on a Windows machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Installing MID-less ACC, Configuring MID-less ACC, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Install MID-less Agent Client Collector using a single-line command in a Windows environment

Install MID-less Agent Client Collector on a Windows machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key. For details, see [Configure an agent registration key](agent-registration-key-configuration.md).
-   Role required: agent\_client\_collector\_admin

## About this task

For details on sending data through the cloud in a MID-less deployment, see [DEX Architecture](https://www.servicenow.com/docs/access?context=dex-architecture&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Procedure

1.  Retrieve the publicly accessible gateway URL, based on your location.

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
2.  On the Windows server where the agent is installed, enter the following command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>"
    ```

    The following table shows the parameter values in the command.

<table id="table_usf_fpf_wfc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable MID-less Agent Client Collector installation. If you don't specify a value, the regular MID Server websocket installation is invoked.

</td></tr><tr><td>

ACC\_CNC

</td><td>

Specify a public gateway endpoint for Agent Client Collector.

</td></tr><tr><td>

REGISTRATION\_KEY

</td><td>

Active and valid registration key for the agent to communicate with.

</td></tr><tr><td>

INSTANCE\_URL

</td><td>

ServiceNow instance that the agent is registered with.

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

Optional string. To disable the allow list, set **ACC\_ALLOW\_LIST=0**. By default, the allow list is enabled.**Note:** Disabling the allow list compromises your system's security and is intended as a temporary measure while you’re updating the allow list. After completing the update, enable the allow list by setting **ACC\_ALLOW\_LIST=1**.

</td></tr><tr><td>

ACC\_VALIDATE\_SIG

</td><td>

Optional string. To disable verification of the installer certification validation, set **ACC\_VALIDATE\_SIG=0** that you can add to disable the verification of the installer certification validation. By default, validation is enabled.**Note:** Disable the certification validation only when using non-standard signature validation tools.

</td></tr></tbody>
</table>
**Parent Topic:**[Installing MID-less Agent Client Collector](../concept/acc-itom-cloud-services.md)

**Related topics**  


[Agent Client Collector MID-less installation command parameters](../reference/acc-ics-command-params.md)

