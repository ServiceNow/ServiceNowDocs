---
title: Require a maintenance token for Windows uninstalls
description: Require using a maintenance token when uninstalling an agent from a Windows device. A maintenance token provides a layer of administrative control so that unauthorized personnel can't perform the uninstall.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/require-maintenance-token-uninstall.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Require a maintenance token for Windows uninstalls

Require using a maintenance token when uninstalling an agent from a Windows device. A maintenance token provides a layer of administrative control so that unauthorized personnel can't perform the uninstall.

## Before you begin

Role required: sn\_agent.token\_admin

## Procedure

1.  Navigate to the Agent Client Collector Setup wizard, as described in [Install the Agent Client Collector on a Windows machine manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-install-windows.md).

2.  Select the **Require maintenance token for uninstall** check box on the Agent Client Collector Configuration page.

3.  Complete the installation and exit the setup wizard.

    **Note:** Alternatively, you can enable requiring a maintenance token by using the following single line command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events ACC_ALLOW_LIST=False UNINSTALLVALIDATION=1
    ```


-   **[Enable uninstall validation during agent upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/require-token-uninstall-upgrade.md)**  
Configure requiring a maintenance token to uninstall agents during agent upgrade. A maintenance token provides a layer of administrative control so that unauthorized personnel can't perform the uninstall.

**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

