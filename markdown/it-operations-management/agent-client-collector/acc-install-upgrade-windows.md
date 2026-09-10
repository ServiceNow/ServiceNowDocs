---
title: Upgrade the Agent Client Collector manually on a Windows system
description: Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-install-upgrade-windows.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install ACC on a Windows machine manually, ACC installation on a Windows machine, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Upgrade the Agent Client Collector manually on a Windows system

Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.

## Before you begin

Backup the Agent Client Collector configuration files, such as `acc.yml`, `check-allow-list.json`, `agent_now_id` and `agent_now_keystore`. The `agent_now_id` is located in the cache directory: `C:\ProgramData\Servicenow\agent-client-collector\cache`

Backing up configuration files is a safety precaution to safeguard the files during the upgrade. Configuration files need to be restored only if there are upgrade issues which require new installation.

Enable golden image mode for cloning additional agents by setting the msi property **GOLDEN\_IMAGE=true**.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Upgrade to the new agent version, as described in [Install the Agent Client Collector on a Windows machine manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-install-windows.md).

    You can use either the manual or single-line procedure. When restoring backup files, the system replaces the configuration file values.

2.  After installation is complete, you can delete the backup files.


**Parent Topic:**[Install the Agent Client Collector on a Windows machine manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-install-windows.md)

