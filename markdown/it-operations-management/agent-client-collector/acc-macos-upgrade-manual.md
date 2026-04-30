---
title: Upgrade Agent Client Collector manually on a macOS system
description: Perform a manual upgrade of your existing Agent Client Collector version on a system running a macOS. Manual upgrade is useful if the single-line command script isn’t connected to the instance or you want to use enhanced customization options.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector installation on macOS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Upgrade Agent Client Collector manually on a macOS system

Perform a manual upgrade of your existing Agent Client Collector version on a system running a macOS. Manual upgrade is useful if the single-line command script isn’t connected to the instance or you want to use enhanced customization options.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Manually back up the `agent-id` and `acc.yml` configuration files by running the following commands.

    ```
    mkdir -p /tmp/acc-upgrade-backup
    
    cp -rp /Library/Application\ Support/servicenow/agent-client-collector/acc.yml /tmp/acc-upgrade-backup
    
    cp -rp /Library/Application\ Support/servicenow/agent-client-collector/check-allow-list.json /tmp/acc-upgrade-backup
    
    cp -rp /Library/Application\ Support/servicenow/agent-client-collector/agent_now_id /tmp/acc-upgrade-backup
    
    ```

    Manually backing up the configuration files provides an added layer of security by ensuring that your files are backed up before beginning the upgrade process.

2.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

3.  In the **macOS Downloads** section, download the relevant agent package and signature `.pkg` files.

4.  Perform package upgrade, based on the cpu your macOS runs with.

    -   Intel cpu:

        ```
        sudo installer -pkg agent-client-collector-<version number>-macos_x64.pkg
        ```

    -   Apple silicon cpu:
    ```
    sudo installer -pkg agent-client-collector-<version number>-macos_arm64.pkg
    ```

    This command also backs up and restores the agent-id and configuration files before upgrading.

5.  Verify that the upgrade was successful.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

    2.  Verify the following values for your agent:

        -   **Host data collection** = Collected
        -   **Version** = &lt;Relevant version number&gt;

**Parent Topic:**[Agent Client Collector installation on macOS system](../concept/acc-install-mac-os.md)

