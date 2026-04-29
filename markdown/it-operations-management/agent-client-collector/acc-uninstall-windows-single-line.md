---
title: Uninstall Agent Client Collector from a Windows system using a single-line command
description: Uninstall the Agent Client Collector from a Windows machine by running an efficient single-line command. If the script is not connected to the instance, you might have to uninstall Agent Client Collector manually.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install the ACC on a Windows machine using silent installation, ACC installation on a Windows machine, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Uninstall Agent Client Collector from a Windows system using a single-line command

Uninstall the Agent Client Collector from a Windows machine by running an efficient single-line command. If the script is not connected to the instance, you might have to uninstall Agent Client Collector manually.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

-   Uninstall Agent Client Collector by running the following command in a command window.

    `msiexec /quiet /x <path_to_acc_msi_file>` .

    **Note:** Uninstalling the Agent Client Collector removes the `acc.yml` file and its directory from your machine.


**Parent Topic:**[Install the Agent Client Collector on a Windows machine using silent installation](acc-windows-install-silent.md)

