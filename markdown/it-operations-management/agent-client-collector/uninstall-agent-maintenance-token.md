---
title: Uninstall an agent using a maintenance token
description: Uninstall an agent from a Windows device using a maintenance token. Administrators require maintenance tokens to ensure that unauthorized employees can't perform an uninstall.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/uninstall-agent-maintenance-token.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Uninstall an agent using a maintenance token

Uninstall an agent from a Windows device using a maintenance token. Administrators require maintenance tokens to ensure that unauthorized employees can't perform an uninstall.

## Before you begin

Enable requiring a maintenance token for uninstalls, as described in [Require a maintenance token for Windows uninstalls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/require-maintenance-token-uninstall.md).

Create a maintenance token to be used when uninstalling an agent, as described in [Create a maintenance token](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/create-maintenance-token.md).

Role required: sn\_agent.token\_admin

## Procedure

1.  Navigate to the Control Panel on your Windows machine and select the Agent Client Collector application to uninstall.

    After the uninstall process begins, the **Uninstall Token Required** dialog box opens.

    \[Omitted image "uninstall-token-request.png"\] Alt text: Dialog box to enter maintenance token for uninstalling an agent

2.  Retrieve the maintenance token that you created.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Maintenance Token**.

    2.  Select the relevant maintenance token.

    3.  Select **View Maintenance Token** in the Related Links section.

    4.  Select the **Copy Token** \(\[Omitted image "copy-token-icon.png"\] Alt text: Copy token icon to copy the maintenance token value\) icon to copy the maintenance token value.

3.  Paste the maintenance token in the **Maintenance Token** field.

4.  Select **OK**.

    **Note:** Alternatively, you can enable requiring a maintenance token by using the following single line command:

    ```
    msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events ACC_ALLOW_LIST=False UNINSTALLVALIDATION=1
    ```

    The agent is uninstalled from your Windows machine.

    If you provide an invalid maintenance token, uninstall is blocked. For more information, check the uninstall logs at `<user folder>\AppData\Local\Temp\ACC_Logs`.


