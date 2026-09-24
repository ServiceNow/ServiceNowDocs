---
title: Install ACC for DEX on Windows
description: Install Agent Client Collector \(ACC\) to work with Digital End-User Experience \(DEX\) to monitor and collect data, provide insights into system performance, identify issues, and enable proactive maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-windows.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [install acc windows, agent client collector windows, acc for dex, install agent client collector, collect dex metrics]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Install ACC for DEX on Windows

Install Agent Client Collector \(ACC\) to work with Digital End-User Experience \(DEX\) to monitor and collect data, provide insights into system performance, identify issues, and enable proactive maintenance.

## Before you begin

Install the ITOM Cloud Services plugin.

[Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-acc-reg-key.md).

Confirm the following device and network settings before you install the agent:

-   Authentication: Digital End-User Experience uses Mutual Transport Layer Security \(mTLS\) to authenticate devices.
-   Ports and protocols: communication with the ServiceNow cloud occurs over port 443 using mTLS, with specific certificates and proxy settings.
-   Firewalls: outbound HTTPS traffic on TCP port 443 is permitted from every device running an ACC agent to the designated ServiceNow cloud FQDNs or IP ranges.
-   Proxy: if device connectivity to the internet is routed through a proxy network, configure the proxy. For details, see [Configure ACC to use a proxy for all traffic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configure-acc-to-use-proxy.md).
-   Populate the **sys\_user** table so that the CI record in production is assigned with the first and last name of the logged-in user of the device.
-   For enterprise-wide deployments, contact your Microsoft Intune or Microsoft Configuration Manager application administrator.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Retrieve the agent registration key:

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.
    2.  Select the relevant agent registration key.
    3.  Copy the registration key value and store it in a place where you can easily retrieve it, when needed.
2.  Retrieve the publicly accessible gateway URL, based on your location.

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
3.  On the Windows server where the agent is installed, enter the following command:

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

</td></tr><tr><td>

LOCALUSERNAME

</td><td>

\[Optional\] Specify **SYSTEM** to run ACC as a local system account user.**Note:** If you specify this parameter, you don't need to complete the procedure [Run ACC as a local system account user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/run-acc-local-sys-account.md).

</td></tr></tbody>
</table>4.  Start the Agent Client Collector service using the default ServiceNow user role created during this installation.

    The default ServiceNow user role has the following privileges:

    -   Performance Monitor: Viewing all performance counters in the system.
    -   Log on as a service: Starting network services and services that run continuously, even when no one is logged in to the console.
    -   Debug program: Monitoring the installed applications and collecting in-depth metrics and remedial actions, such as restart and stop.
5.  To collect DEX metrics, restart the ACC service using one of the following methods:

    -   Add **Remote Desktop user** to ServiceNow user.
    -   [Run as a local system account user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/run-acc-local-sys-account.md).
    -   [Run as a managed group user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/run-acc-as-managed-group-user.md).
6.  Restart the Agent Client Collector service.

7.  Verify that the agent registered with your instance and is collecting host data.

    For details, see [Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md).


**Related topics**  


[Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-acc-reg-key.md)

[Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md)

[Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md)

