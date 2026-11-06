---
title: Install ACC for DEX on macOS
description: Install Agent Client Collector \(ACC\) on a macOS device so that DEX can collect performance data and identify issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/install-acc-for-dex-macos.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 3
keywords: [install acc macos, agent client collector mac, acc for dex, install agent client collector, install acc mac]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Operations Management]
---

# Install ACC for DEX on macOS

Install Agent Client Collector \(ACC\) on a macOS device so that DEX can collect performance data and identify issues.

## Before you begin

-   The ITOM Cloud Services Core plugin \(sn\_itom\_cloud\_svc\) must be installed.
-   Your instance must be onboarded to use ITOM Cloud Services. For details, contact Customer Support.
-   An agent registration key must be configured.
-   The device must authenticate to ITOM Cloud Services, which uses mutual Transport Layer Security \(mTLS\) to authenticate devices.
-   Outbound HTTPS traffic on TCP port 443 must be permitted from every device running an ACC agent to the designated ServiceNow cloud FQDNs or IP ranges.
-   If device connectivity to the internet is routed through a proxy network, the proxy must be configured. For details, see [Configure ACC to use a proxy for all traffic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configure-acc-to-use-proxy.md).
-   The User \[sys\_user\] table must be populated with the first name and last name of the user logged in to the device. The CI record in the production environment is then assigned to the correct user.

For enterprise-wide deployments, contact your Jamf application administrator.

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

4.  Enter `sudo -i` and enter your device password.

    **Note:** You must have administrative privileges on the device to install the agent.

5.  On the device where you’re installing the Agent Client Collector, enter the following command:

    ```
    CONNECT_WITHOUT_MID="true" ACC_CNC="<gateway_endpoint>" REGISTRATION_KEY="<registration_key>" INSTANCE_URL="https://<instance_url>" bash -c "$(curl -L https://<instance_url>/api/sn_agent/agents/install_agent)"
    ```

    The following table describes the parameter values in the command.

<table id="table_i4m_yjq_wxb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CONNECT\_WITHOUT\_MID

</td><td>

Specify `true` to enable MID-less installation. If you don't specify a value, the regular MID Server WebSocket installation is invoked.

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

Optional **ACC\_VALIDATE\_SIG=0** string that you can add to disable installer certification validation. Default: Validation is enabled.

**Note:** Disable the certification validation only when you're using nonstandard signature validation tools.

</td></tr></tbody>
</table>6.  Configure the ServiceNow sudoers file.

    For details on the procedure, see [Configure the ServiceNow sudoers file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/config-sudoers-file.md).

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


[Create an ACC registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/create-acc-reg-key.md)

[DEX architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-architecture.md)

[Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/verify-acc-agent-registration.md)

[Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/uninstall-acc-agent.md)

