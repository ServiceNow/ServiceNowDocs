---
title: Uninstall the Agent Client Collector agent from a device
description: Removing the Agent Client Collector \(ACC\) agent ensures clean device states after testing, proper decommissioning, or when you need to reinstall with different configuration settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [uninstall acc agent, remove agent client collector, uninstall agent client collector, acc agent removal, remove acc from device]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Uninstall the Agent Client Collector agent from a device

Removing the Agent Client Collector \(ACC\) agent ensures clean device states after testing, proper decommissioning, or when you need to reinstall with different configuration settings.

## Before you begin

You must have administrative privileges on the device to uninstall the agent.

Role required: agent\_client\_collector\_admin

## About this task

Uninstall the agent from your candidate test devices before you start a bulk deployment. Leaving a manually installed agent in place can cause the bulk-deployed agent to register a duplicate record for the same device.

**Important:** Uninstalling the agent from a device doesn't remove its registration from your ServiceNow instance. After you uninstall, deregister the agent. For details, see [Deregister an Agent Client Collector agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/deregister-acc-agent.md).

## Procedure

1.  Uninstall the agent using the method for your operating system.

<table id="choicetable-uninstall-acc"><thead><tr><th align="left" id="d223006e120">

Option

</th><th align="left" id="d223006e123">

Procedure

</th></tr></thead><tbody><tr><td id="d223006e129">

**macOS**

</td><td>

1.  Open a Terminal session.
2.  Access the root folder by entering `sudo -i` and providing your device password.
3.  Enter the following command:

    ```
bash -c "$(curl -L https://<instance_url>/api/sn_agent/agents/install_agent)" -s "--remove"
    ```

</td></tr><tr><td id="d223006e156">

**Windows**

</td><td>

1.  Open Control Panel.
2.  Navigate to **Programs** &gt; **Programs and Features**.
3.  Select Agent Client Collector in the list.
4.  Right-click the application and select **Uninstall**.
5.  Follow the on-screen instructions.


</td></tr></tbody>
</table>
## What to do next

Deregister the agent on your instance. For details, see [Deregister an Agent Client Collector agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/deregister-acc-agent.md).

**Related topics**  


[Deregister an Agent Client Collector agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/deregister-acc-agent.md)

[Bulk deploy Agent Client Collector on macOS using Jamf](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/bulk-deploy-acc-on-macos.md)

[Install Agent Client Collector on Windows using Microsoft Intune](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/bulk-deploy-acc-on-win.md)

