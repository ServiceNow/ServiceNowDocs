---
title: Uninstall the Agent Client Collector from macOS using a single-line command
description: Uninstall the Agent Client Collector from macOS machine by running an efficient single-line command. If the agent is connected to the instance, uninstall Agent Client Collector manually.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector installation on macOS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Uninstall the Agent Client Collector from macOS using a single-line command

Uninstall the Agent Client Collector from macOS machine by running an efficient single-line command. If the agent is connected to the instance, uninstall Agent Client Collector manually.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

-   Run the following command.

    ```
    bash -c "$(curl -L https://<Instance URL>/api/sn_agent/agents/install_agent)" -s "--remove"
    ```

    **Note:** Uninstalling the Agent Client Collector removes the `acc.yml` file and its directory from your machine. The user and group **\_servicenow**, created as part of the installation process, is also removed.


**Parent Topic:**[Agent Client Collector installation on macOS system](../concept/acc-install-mac-os.md)

