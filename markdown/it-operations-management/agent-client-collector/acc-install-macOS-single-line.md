---
title: Perform a single-line Agent Client Collector installation on macOS
description: Use an efficient single-line command script to install Agent Client Collector on a machine that uses macOS operating system. Use the manual installation procedure if the agent is not connected to the instance or you want enhanced customization options.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACC installation on a macOS system, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Perform a single-line Agent Client Collector installation on macOS

Use an efficient single-line command script to install Agent Client Collector on a machine that uses macOS operating system. Use the manual installation procedure if the agent is not connected to the instance or you want enhanced customization options.

## Before you begin

-   Ensure that you have configured the Agent Client Collector web server.
-   Verify that your server's OS and version matches the list of supported OS versions as described in [Agent Client Collector installation](../concept/acc-installation.md).
-   Ensure that you have the **pkgutil** packages available, to be used by the install script.
-   Ensure that the target agents have connectivity to the following:
    -   ServiceNow install server \[install.service-now.com\]
    -   ServiceNow instance
    -   The MID Server to which the agent will connect

Role required: agent\_client\_collector\_admin

## Procedure

1.  Retrieve the MID Server websocket URL parameters.

    1.  Navigate to **Agent Client Collector** &gt; **Websocket Endpoint**.

    2.  Select the relevant websocket endpoint.

    3.  Copy the **Endpoint URL** field value to be used in the installation command.

2.  Retrieve the API Key.

    1.  Navigate to **Agent Client Collector** &gt; **Deployment** &gt; **MID Web Server API Key**.

    2.  Copy the **API Key** value, to be used in the installation command.

3.  Run the following command on the server where the Agent Client Collector is being installed.

    ```
    ACC_API_KEY=<api_key> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events bash -c "$(curl -L https://<instance URL>/api/sn_agent/agents/install_agent)"
    ```

    Enter the following values in the command line:

<table id="table_wff_w2q_nqb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

ACC\_API\_KEY

</td><td>

Replace the **&lt;api\_key&gt;** string with the API key used to access the MID Server websocket. If no value is specified, you will be prompted to enter the API key value during the script's execution.

</td></tr><tr><td>

ACC\_MID

</td><td>

Replace the **&lt;mid\_ip&gt;** string with the URL of the MID Server websocket. When specifying multiple MID Servers, enter a string separated by commas for each MID Server.

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

\(Optional\) Add the string **ACC\_ALLOW\_LIST=0** to disable the allow list. By default, the allow list is enabled.**Note:** Disabling the allow list compromises your system's security and is recommended only as a temporary measure until you finish updating the allow list. After completing the update, re-activate the allow list by removing **ACC\_ALLOW\_LIST=0** from the single-line command string.

</td></tr><tr><td>

ACC\_VALIDATE\_SIG

</td><td>

\(Optional\) Add the string **ACC\_VALIDATE\_SIG=0** to disable verifying the installer certificate validation. By default, validation is enabled.Default: Validation is enabled.

**Note:** Disable certification validation only when using non-standard signature validation tools.

</td></tr></tbody>
</table>
**Parent Topic:**[Agent Client Collector installation on a macOS system](../concept/acc-install-mac-os.md)

