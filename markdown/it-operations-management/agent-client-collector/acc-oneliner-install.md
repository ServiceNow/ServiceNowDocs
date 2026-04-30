---
title: Perform a single-line Agent Client Collector installation on Linux
description: Use an efficient single-line command script to install Agent Client Collector on a machine that uses a Linux operating system. If a script is not connected to the instance or you want to use enhanced customization options, you might have to install Agent Client Collector manually.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector installation on a Linux OS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Perform a single-line Agent Client Collector installation on Linux

Use an efficient single-line command script to install Agent Client Collector on a machine that uses a Linux operating system. If a script is not connected to the instance or you want to use enhanced customization options, you might have to install Agent Client Collector manually.

## Before you begin

-   Ensure that you have configured the Agent Client Collector web server.
-   Verify that your server's OS and version matches the list of supported OS versions as described in [Agent Client Collector installation](../concept/acc-installation.md).
-   Ensure that the unzip program is installed on your Linux machine.
-   Determine the resource limits for the agent to be configured in the `/usr/lib/systemd/system/acc.service` file after installation.
-   Ensure that you have the `openssl` and `dgst` \(for RHEL/Centos/SUSE installation\) packages available, to be used by the install script.
-   Ensure that you have the `gpg` package available for validation \(for Ubuntu/Debian installation\).
-   When performing single-line installation on more than one agent, download the agent package to your local machine. Place the package on your `ftp` server, using an Ansible script. For details on mass deployment of agents, see [Incorporating the Agent Client Collector into a custom base image for mass deployment](acc-virtual-deployment.md).
-   In order for the Agent to retrieve the OS serial numbers and TCP connections along with associated running processes, sudo access for “dmidecode” and “ss” is required on Linux systems.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Retrieve MID Server websocket URL parameters.

    1.  Navigate to **Agent Client Collector** &gt; **Websocket Endpoint** and select the relevant websocket endpoint.

    2.  Copy the value of the **Endpoint URL** field to be used in the installation command.

2.  Copy and edit the following command line, substituting your own information for the command parameters.

    `ACC_API_KEY=<api_key> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events bash -c "$(curl -L https://<instance URL>/api/sn_agent/agents/install_agent)"`

<table id="table_al4_f4s_wlb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

ACC\_API\_KEY

</td><td>

The API key used to access the MID Server websocket.If no ACC\_API\_KEY value is specified, you will be asked to enter the API key value during execution of the script.

</td></tr><tr><td>

ACC\_MID

</td><td>

The URL of the MID Server websocket.If you are specifying multiple MID Servers, enter a string separated by commas for each MID Server.

</td></tr></tbody>
</table>3.  If you need to create new check definitions to be included in the allow list that indicates the checks enabled to run on the agent, disable the allow list by adding **ACC\_ALLOW\_LIST=0** to the single-line command string.

    **Note:** This action compromises your system's security and is recommended only as a temporary measure until you finish updating the allow list. After completing the update, re-activate the allow list by removing **ACC\_ALLOW\_LIST=0** from the single-line command string.

4.  If the certificate validation process is too time consuming or if you are using the agent for development purposes, you can bypass certificate validation by adding **ACC\_VALIDATE\_SIG=0** to the single-line command string.

5.  Run the single-line command \(specified in step [2](acc-oneliner-install.md#command), above\) on the server where the Agent Client Collector is installed.

6.  Configure resource limits for the agent in the `/usr/lib/systemd/system/acc.service` file, according to your business needs.

    The default values in the file are:

    -   **CPUShares**: 128
    -   **CPUQuota**: 10%
    -   **MemoryLimit**: 192M
    -   **BlockIOWeight**: 10
    -   **LimitNICE**: +15

**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

