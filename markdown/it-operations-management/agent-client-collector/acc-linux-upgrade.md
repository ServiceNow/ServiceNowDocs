---
title: Upgrade Agent Client Collector on a Linux system
description: Upgrade your existing Agent Client Collector version on a system running a Linux OS if the single-line command script is not connected to the instance or you want to use enhanced customization options.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC installation on a Linux system, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Upgrade Agent Client Collector on a Linux system

Upgrade your existing Agent Client Collector version on a system running a Linux OS if the single-line command script is not connected to the instance or you want to use enhanced customization options.

## Before you begin

-   The upgrade procedure is the same for both MID Server and MID-less deployments.
-   Role required: agent\_client\_collector\_admin

## Procedure

1.  Back up sensitive files by running the following command.

    ```
    tar -Pcvzf /root/acc_backup.tar.gz /etc/servicenow/agent-client-collector \
    /var/cache/servicenow/agent-client-collector/agent_now_id \
    /usr/lib/systemd/system/acc.service
    ```

2.  Download the .rpm/.deb agent package and signature files, as described in [Install Agent Client Collector on a Linux system](install-acc-linux.md).

3.  Upgrade the package.

    -   In an RPM-based system:

        `rpm -Uv agent-client-collector-<version number>-x86_64.rpm`

    -   In a DEB-based system:

        `dpkg -i agent-client-collector-<version number>-<distro>_amd64.deb`

4.  Restore the systemd service file \(if you customized the file\), using either an automation tool or by reloading systemd configuration.

    ```
    tar -C / -Pxvzf /root/acc_backup.tar.gz usr/lib/systemd/system/acc.service
    
    ```

    ```
    systemctl daemon-reload
    ```

5.  Change the **owner:group** setting to the correct one by running the following command.

    ```
    chown -R servicenow:servicenow /{etc,var/cache,var/log,usr/share}/servicenow/agent-client-collector
    ```

6.  Restart the service and verify that it connects to its backend-url.

    ```
    systemctl restart acc
    tail -f /var/log/servicenow/agent-client-collector/acc.log
    
    ```


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

