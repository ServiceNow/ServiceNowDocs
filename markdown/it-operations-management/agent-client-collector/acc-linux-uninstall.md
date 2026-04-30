---
title: Uninstall Agent Client Collector from a Linux system manually
description: Uninstall the Agent Client Collector from a Linux machine manually if the command script is unavailable due to the specific agent not being connected to the instance.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC installation on a Linux system, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Uninstall Agent Client Collector from a Linux system manually

Uninstall the Agent Client Collector from a Linux machine manually if the command script is unavailable due to the specific agent not being connected to the instance.

## Before you begin

-   The uninstall procedure is the same for both MID Server and MID-less deployments.
-   Role required: agent\_client\_collector\_admin

## About this task

By default, an uninstalled agent is removed from the system after 30 days. To modify this amount of time, update the **sn\_agent\_ci\_extended\_info** table, accessible from the Auto Flushes page \(enter **sys\_auto\_flush.LIST** into the instance's search filter field\).

## Procedure

1.  Stop the service.

    `sudo systemctl stop acc`

2.  Use the relevant package management tool to remove the service.

    -   yum remove agent-client-collector
    -   apt-get remove agent-client-collector
    -   zypper remove agent-client-collector
    Alternatively, you can run one of the following commands, based on the OS in use.

    -   `rpm -e agent-client-collector`
    -   `dpkg -r agent-client-collector`
3.  If you ran either the `rpm` or `dpkg` command, remove any remaining files from your system.

    ```
    # userdel -r servicenow
    # groupdel servicenow
    # rm -R /{etc,var/cache,var/log,usr/share}/servicenow/agent-client-collector
    ```

    **Warning:** Do not use the command rm -Rf, as this can cause data loss.


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

