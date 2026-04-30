---
title: Upgrade the Agent Client Collector manually on a Linux system
description: Perform a manual upgrade of your existing Agent Client Collector version on a system running a Linux OS if the single-line command script is not connected to the instance or you want to use enhanced customization options.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACC installation on a Linux system, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Upgrade the Agent Client Collector manually on a Linux system

Perform a manual upgrade of your existing Agent Client Collector version on a system running a Linux OS if the single-line command script is not connected to the instance or you want to use enhanced customization options.

## Before you begin

-   Ensure that you have configured the Agent Client Collector web server. For more information, see [Configure the websocket server on the MID Server](acc-configure-web-server.md).
-   Restart the MID Web Server.
-   Collect host data, to ensure that all files are up to date. For details, see [Run host data collection for an agent](collect-host-data-agent.md).
-   Ensure that you have installed a Linux version of the Agent Client Collector. For more information, see [Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md).
-   Role required: agent\_client\_collector\_admin

## About this task

The upgrade procedure is the same for both MID Server and MID-less deployments.

## Procedure

1.  Back up the `agent-id` and configuration files.

    ```
    mkdir -p /tmp/acc-upgrade-backup
    sudo cp -rp /etc/servicenow/agent-client-collector/acc.yml /tmp/acc-upgrade-backup
    sudo cp -rp /etc/servicenow/agent-client-collector/check-allow-list.json /tmp/acc-upgrade-backup
    sudo cp -rp /var/cache/servicenow/agent-client-collector/agent_now_id /tmp/acc-upgrade-backup
    ```

2.  Uninstall the package.

    1.  Stop the service.

        `sudo systemctl stop acc`

    2.  Disable the service.

        `sudo systemctl disable acc`

    3.  Uninstall the package:

        -   For RHEL/CentOS/SUSE: `sudo rpm -e agent-client-collector`
        -   For Ubuntu/Debian: `sudo dpkg -r agent-client-collector`
3.  Download the installation file.

    For example, when working with an Ubuntu/Debian OS, use both of the following:

    `curl -L -O https://<MID-WEBSERVER-URI:PORT>/static/acc_installers/agent-client-collector/glide/distribution/builds/package/app-signed/agent-client-collector-<version number>-<Ubuntu/Debian version>_amd64-deb-deb.zip -O`

    `https://<MID-WEBSERVER-URI:PORT>/static/acc_installers/agent-client-collector/glide/distribution/builds/package/app-signed/agent-client-collector/agent-client-collector-<version number>-<Ubuntu/Debian version>_amd64.deb`

4.  Verify and install the package.

    1.  Unzip the compressed file.

        `unzip agent-client-collector-2.3.0-debian-9_amd64-deb-deb.zip`

    2.  Validate the installer file signature.
        -   RHEL/Centos/SUSE OS:

            `openssl dgst -sha256 -verify {<ServiceNow DGST pem key>} -signature {<signature file>} agent-client-collector-<version number>-x86_64.rpm`

        -   Ubuntu/Debian OS:

            ```
            gpg --import ServiceNow_Digicert_Public.gpg
            dpkg-sig --verify agent-client_collector-<version number>-<Ubuntu/Debian version>_amd64.deb
            ```

    3.  Install the package.
        -   RHEL/CentOS/SUSE: `sudo rpm -vi --force agent-client-collector-<version number>-x86_64.rpm`
        -   Ubuntu/Debian: `sudo dpkg -1 agent-client-collector-<version number>-<Ubuntu/Debian version>_amd64.deb`
5.  Restore the `agent-id` and configuration files.

    ```
    sudo -u servicenow cp -rp /tmp/acc-upgrade-backup/acc.yml /etc/servicenow/agent-client-collector/acc.yml
    sudo -u servicenow cp -rp /tmp/acc-upgrade-backup/check-allow-list.json /etc/servicenow/agent-client-collector/check-allow-list.json
    sudo -u servicenow cp -rp /tmp/acc-upgrade-backup/agent_now_id /var/cache/servicenow/agent-client-collector/agent_now_id
    ```

6.  Configure the agent to run as a service.

    `sudo systemctl enable acc`

7.  Start the service.

    `sudo systemctl start acc`

8.  View the logs to verify that the startup was successful.

    `sudo tail -f /var/log/servicenow/agent-client-collector/acc.log`


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

