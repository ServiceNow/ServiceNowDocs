---
title: Upgrade the Agent Client Collector manually on a Windows system
description: Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install ACC on a Windows machine manually, ACC installation on a Windows machine, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Upgrade the Agent Client Collector manually on a Windows system

Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.

## Before you begin

Backup the Agent Client Collector configuration files, such as `acc.yml`, `check-allow-list.json`, `agent_now_id` and `agent_now_keystore`. The `agent_now_id` is located in the cache directory: `C:\ProgramData\Servicenow\agent-client-collector\cache`

Backing up configuration files is a safety precaution to safeguard the files during the upgrade. Configuration files need to be restored only if there are upgrade issues which require new installation.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Select the Windows button on your keyboard and enter **Services** to open the Services page.

2.  Locate the Agent Client Collector service.

3.  Right click the Agent Client Collector service and select **Stop**.

4.  On the Windows Control Panel, select **Uninstall a program**.

5.  Select the Agent Client Collector program and select **Uninstall**.

6.  Navigate to **Agent Client Collector** &gt; **Agent Downloads** and download the MSI Installer in the **Windows Downloads** section.

7.  Install the new agent, as described in [Install Agent Client Collector on a Windows machine manually](acc-install-windows.md).

    You can use either the manual or single-line procedure. When restoring backup files, the system replaces the configuration file values.

8.  After installation is complete, stop the service.

9.  Restore the `agent_now_id` and `agent_now_keystore` configuration files.

10. Restart the Agent Client Collector service.


**Parent Topic:**[Install Agent Client Collector on a Windows machine manually](acc-install-windows.md)

