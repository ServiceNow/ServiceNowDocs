---
title: Install ACC for DEX on macOS
description: Install Agent Client Collector \(ACC\) to monitor and collect data in a centralized and organized manner, provide insights into system performance, identify issues, and enable proactive maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-macos.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [install acc macos, agent client collector mac, acc for dex, install agent client collector, install acc mac]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Install ACC for DEX on macOS

Install Agent Client Collector \(ACC\) to monitor and collect data in a centralized and organized manner, provide insights into system performance, identify issues, and enable proactive maintenance.

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key.
-   Confirm that the device can authenticate to ITOM Cloud Services, which uses Mutual Transport Layer Security \(mTLS\) to authenticate devices.
-   Confirm that outbound HTTPS traffic on TCP port 443 is permitted from every device running an ACC agent to the designated ServiceNow cloud FQDNs or IP ranges.
-   If device connectivity to the internet is routed through a proxy network, configure the proxy. For details, see [Configure ACC to use a proxy for all traffic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configure-acc-to-use-proxy.md).
-   Populate the **sys\_user** table so that the CI record in production is assigned with the first and last name of the logged-in user of the device.
-   For enterprise-wide deployments, contact your Jamf application administrator.

Role required: root

## Procedure

1.  Retrieve the agent registration key:

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.

    2.  Select the relevant agent registration key.

    3.  Copy the registration key value and store it in a place where you can easily retrieve it when needed.

2.  Retrieve the publicly accessible gateway URL, based on your location:

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
3.  On the device where you're installing the Agent Client Collector, open a Terminal session and access the root folder.

4.  Enter `sudo -i` and provide your device password.

    **Note:** You must have administrative privileges on the device to install the agent.

5.  On the server where you’re installing the Agent Client Collector, enter the following command:

    ```
    CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>" bash -c "$(curl -L https://<instance_url>/api/sn_agent/agents/install_agent)"
    ```

    The following table describes the parameter values in the command.

<table id="table_i4m_yjq_wxb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify **true** to enable MID-less installation. If you don't specify a value, the regular MID Server websocket installation is invoked.

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
</table>6.  Configure the ServiceNow sudoers file.

    For details on the procedure, see [Configure ServiceNow sudoers file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/config-sudoers-file.md).

7.  Restart the Agent Client Collector service by unloading and loading the launch daemon.

    ```
    sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist
    sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist
    ```

    **Note:** Restart the service after any change to the `acc.yml` file or the sudoers file.

8.  View the agent log to confirm that the installation completed.

    ```
    tail -f /Library/Application\ Support/servicenow/agent-client-collector/log/acc.log
    ```


**Related topics**  


[Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-acc-reg-key.md)

[DEX Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-architecture.md)

[Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md)

[Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md)

