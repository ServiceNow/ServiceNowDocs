---
title: Configure Agent Client Collector log levels
description: You configure the log levels that you want the Agent Client Collector logs to contain. All events that match or exceed the specified log level display in the Agent Client Collector logs.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using ACC logs, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure Agent Client Collector log levels

You configure the log levels that you want the Agent Client Collector logs to contain. All events that match or exceed the specified log level display in the Agent Client Collector logs.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Specify the desired log level in the `acc.yml` configuration file.

    Alternatively, you can specify the log level as an argument in the `--loglevel` command-line flag, as follows:

    ```
    acc start --log level debug
    ```

2.  Restart the agent using the service manager:

    -   **Linux**:

        ```
        sudo service acc restart
        ```

    -   **Windows**:

        ```
        sc.exe stop AgentClientCollector
        sc.exe start AgentClientCollector
        ```

    -   **macOS**:

        ```
        sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist
        ```

    **Note:** You must restart the service after changing the log level.


**Parent Topic:**[Using Agent Client Collector logs](../concept/logs-acc.md)

