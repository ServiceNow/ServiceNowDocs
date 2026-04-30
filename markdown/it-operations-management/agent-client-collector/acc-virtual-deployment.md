---
title: Incorporating the Agent Client Collector into a custom base image for mass deployment
description: Deploy the Agent Client Collector on a virtual machine during mass deployment using the machine's base image. Mass deployment uses silent installation, which hides installation status.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC installation, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Incorporating the Agent Client Collector into a custom base image for mass deployment

Deploy the Agent Client Collector on a virtual machine during mass deployment using the machine's base image. Mass deployment uses silent installation, which hides installation status.

## Before you begin

Use Microsoft SCCM to manage the deployment and security of your devices, as described in the [Create a Windows service account with Log on as a Service](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867669) KB article.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Downloads**.

2.  Download the installation file of the relevant OS.

3.  Install the agent according to the relevant OS instructions.

4.  Run the following command to stop the agent service:

    -   In a Windows environment: Run the command `sc stop AgentClientCollector`
    -   In a Linux environment: Run the command `sudo systemctl stop acc`
5.  Ensure that the `acc.yml` file doesn’t include an encrypted API key.

    For example: `api-key: "<insert plain text API key here>"`

6.  Delete the contents of the agent's cache directory, keeping the directory structure intact:

    -   In a Windows environment: `C:\ProgramData\ServiceNow\agent-client-collector\cache`
    -   In a Linux environment: `/var/cache/servicenow/agent-client-collector`
7.  When installing on a Windows machine, ensure that the installation was successful by doing one of the following:

    -   Enable logging in silent installation and verify that the log file ends with the string, `Windows Installer installed the product`.
    -   Ensure that the **AgentClientCollector** service has the status `Running`.
8.  When installing on a Linux machine, access the machine where the agent is installed and modify the `/usr/share/servicenow/agent-client-collector/serial_number.txt` file in one of the following ways:

    -   Change its content with the host's serial number, by running the following command: `sudo -n dmidecode -s system-serial-number`
    -   Assign sudo permissions to the ServiceNow user to enable running the following `osqueryi` command: `sudo -E env "PATH=$PATH" osqueryi --logger_min_status=3 --line "select hardware_serial from system_info"`
    **Note:** You must change the virtual machine's host name after deployment to a unique value, to avoid damaging the host's CI.

9.  As a post-deployment step, restart the agent service.

    -   In a Windows environment: Run the command `sc start AgentClientCollector`
    -   In a Linux environment: Run the command `sudo systemctl start acc`

