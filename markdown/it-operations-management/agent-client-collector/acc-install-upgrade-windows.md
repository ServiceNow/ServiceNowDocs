---
title: Upgrade the Agent Client Collector manually on a Windows system
description: Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-install-upgrade-windows.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install ACC on a Windows machine manually, ACC installation on a Windows machine, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Upgrade the Agent Client Collector manually on a Windows system

Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.

## Before you begin

Enable golden image mode for cloning additional agents by setting the msi property **GOLDEN\_IMAGE=true**.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Upgrade to the new agent version, as described in [Upgrade an agent in an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/upgrade-agent-from-instance.md).

    You can use either the manual or single-line procedure. When restoring backup files, the system replaces the configuration file values.


**Parent Topic:**[Install Agent Client Collector on a Windows machine manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-install-windows.md)

