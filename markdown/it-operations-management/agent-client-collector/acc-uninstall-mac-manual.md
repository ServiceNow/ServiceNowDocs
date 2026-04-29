---
title: Uninstall the Agent Client Collector from a macOS machine manually
description: Uninstall the Agent Client Collector from a macOS machine manually instead of using the single-line procedure when the specific agent is not connected to the instance.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC installation on a macOS system, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Uninstall the Agent Client Collector from a macOS machine manually

Uninstall the Agent Client Collector from a macOS machine manually instead of using the single-line procedure when the specific agent is not connected to the instance.

## Before you begin

-   The upgrade procedure is the same for both MID Server and MID-less deployments.
-   Role required: agent\_client\_collector\_admin

## Procedure

1.  In a command window, disable and stop the service:

    `sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist`

2.  Delete the following files/directories:

    ```
    sudo rm /Library/LaunchDaemons/com.sn.acc.plist
    sudo rm -rf /opt/servicenow/agent-client-collector
    sudo rm -rf /var/run/servicenow/agent-client-collector
    sudo rm -rf /Library/Application\ Support/servicenow/agent-client-collector
    ```

3.  Remove the **\_servicenow** user and group.

    ```
    sudo /usr/bin/dscl . -delete /Users/_servicenow
    sudo /usr/bin/dscl . -delete /Groups/_servicenow
    ```

4.  Remove the **pkg** from the list of installed packages.

    ```
    sudo pkgutil --forget com.servicenow.agent-client-collector
    ```


**Parent Topic:**[Agent Client Collector installation on a macOS system](../concept/acc-install-mac-os.md)

