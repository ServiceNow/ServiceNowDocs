---
title: Validate Linux installation
description: After installing the Agent Client Collector on a Linux system, validate the installation by ensuring it was completed properly.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC installation on a Linux OS system, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Validate Linux installation

After installing the Agent Client Collector on a Linux system, validate the installation by ensuring it was completed properly.

## Before you begin

Install the Agent Client Collector on a Linux system \(see [Install Agent Client Collector on a Linux system](install-acc-linux.md)\).

Role required: agent\_client\_collector\_admin

## Procedure

1.  Run the `# systemctl status acc` command.

    The **active \(running\)** indicator appears when the service is running properly.

    ```
    # systemctl status acc
    ● acc.service - Agent-Now ACC
    Loaded: loaded (/usr/lib/systemd/system/acc.service; enabled; vendor preset: disabled)
    Active: active (running) since Mon 2022-04-25 14:10:24 UTC; 6 months 23 days ago
    Main PID: 2693 (acc)
    Tasks: 10 (limit: 512)
    Memory: 143.4M (limit: 192.0M)
    CPU: 12h 57min 50.442s
    CGroup: /system.slice/acc.service
    └─2693 /usr/share/servicenow/agent-client-collector/bin/acc start --config-file
    /etc/servicenow/agent-client-collect...
    ```

2.  View the encrypted **api-key** and **agent-key-id** in use by running the `grep -E '^api-key|agent-key-id' /etc/servicenow/agent-client-collector/acc.yml` command.

    ```
    # grep -E '^api-key|agent-key-id' /etc/servicenow/agent-client-collector/acc.yml
    api-key: "encrypted:adskfjldfjlasd+ajflksadjmoreunreadablestringasdfdfkdjksdjaasdfas"
    agent-key-id: b4ac2ab4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4ac2b4a
    ```

    **Note:** The **grep** command must appear on a single line.

3.  View the agent's connection with its backend URL by running the `grep 'successfully connected' /var/log/servicenow/agent-client-collector/acc.log` command.

    ```
    # grep 'successfully connected' /var/log/servicenow/agent-client-collector/acc.log
    2022-11-17T19:03:17.94 [INFO] [agent] successfully connected to the url:
    wss://MY_BACKEND_FQDN:MY_BACKEND_PORT/ws/events
    ```

    **Note:** The **grep** command must appear on a single line.

4.  Verify the unique agent ID by running the `# echo $(hexdump -e '/1 "%02x"' /var/cache/servicenow/agent-client-collector/agent_now_id)` command.

    ```
    # echo $(hexdump -e '/1 "%02x"' /var/cache/servicenow/agent-client-collector/agent_now_id)
    14b4443df6d2394d
    ```

    The indicated agent ID appears on the Agents page in an instance \(**All** &gt; **Agent Client Collector** &gt; **Agents**\) with **Status = Up** and **Host data collection = Collected** \(both appearing in green\).

    ![Linux agents Up status](../image/acc-linux-agents-up.png "Linux agents - green status")


**Parent Topic:**[Agent Client Collector installation on a Linux OS system](../concept/acc-install-linux-concept.md)

