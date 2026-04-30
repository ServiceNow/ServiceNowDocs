---
title: Uninstall Agent Client Collector from macOS using a single-line command
description: Uninstall Agent Client Collector from macOS machine by running an efficient single-line command. If the agent is connected to the instance, uninstall Agent Client Collector manually.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC installation on a macOS system, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Uninstall Agent Client Collector from macOS using a single-line command

Uninstall Agent Client Collector from macOS machine by running an efficient single-line command. If the agent is connected to the instance, uninstall Agent Client Collector manually.

## Before you begin

-   The uninstall procedure is the same for both MID Server and MID-less deployments.
-   Role required: agent\_client\_collector\_admin

## Procedure

-   Run the following command.

    ```
    bash -c "$(curl -L https://<Instance URL>/api/sn_agent/agents/install_agent)" -s "--remove"
    ```

    **Note:** Uninstalling the Agent Client Collector removes the `acc.yml` file and its directory from your machine. The user and group **\_servicenow**, created as part of the installation process, is also removed.


**Parent Topic:**[Agent Client Collector installation on a macOS system](../concept/acc-install-mac-os.md)

