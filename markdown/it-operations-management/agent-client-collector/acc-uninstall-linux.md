---
title: Uninstall Agent Client Collector from a Linux system using a single-line command
description: Uninstall the Agent Client Collector from a Linux machine by running an efficient single-line command. If the script is not connected to the instance, you might have to uninstall Agent Client Collector manually.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector installation on a Linux OS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Uninstall Agent Client Collector from a Linux system using a single-line command

Uninstall the Agent Client Collector from a Linux machine by running an efficient single-line command. If the script is not connected to the instance, you might have to uninstall Agent Client Collector manually.

## Before you begin

-   The uninstall procedure is the same for both MID Server and MID-less deployments.
-   Role required: agent\_client\_collector\_admin

## Procedure

-   Uninstall Agent Client Collector by running the following command in a command window where `<instance url>` is the URL of the ServiceNow instance.

    `bash -c "$(curl -L https://<instance url>/api/sn_agent/agents/install_agent)" -s "--remove"` .

    **Note:** Uninstalling the Agent Client Collector removes the `acc.yml` file and its directory from your machine.


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

