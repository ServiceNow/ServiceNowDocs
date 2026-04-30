---
title: View the Agent Client Collector logs
description: You can view the activity logs for an Agent Client Collector.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using ACC logs, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# View the Agent Client Collector logs

You can view the activity logs for an Agent Client Collector.

## About this task

Agent Client Collector logs are accessible from:

-   **Linux**: `/var/log/servicenow/agent-client-collector/acc.log`
-   **Windows**: The location specified by the `log-file` configuration flag. The default location is: `C:/ProgramData/ServiceNow/agent-client-collector/log/acc.log`

    If the `C:/ProgramData` directory is hidden \(such as on older Windows versions\), change the Explorer filter to show hidden elements.

-   **macOS**: The default location is: `/Library/Application\ Support/servicenow/agent-client-collector`

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

    The **Agent Client Collectors** page opens.

    ![Agent Client Collectors page](../image/ACC-Agent-Client-Collectors.png "Agent Client Collectors page")

    The displayed columns are those selected when clicking the Settings icon ![Settings icon](../../event-management/image/search-icon.png).

    The **Host** column indicates the host name of the agent.

    The **Class** column indicates the agent's CI type.

2.  Select an agent.

    The **Agent Client Collector** page opens.

3.  In the **Related Links** section, click **Grab Agent Log**.

    The **Queues** page opens for the selected Agent.

4.  Refresh the page and click the relevant entry with the value **Queue = input**.

    The **Payload** section on the **Queue** form displays the log for the Agent Client Collector.


**Parent Topic:**[Using Agent Client Collector logs](../concept/logs-acc.md)

**Related topics**  


[Enable log monitoring in a Linux environment](acc-enable-log-monitoring-linux.md)

[Enable log monitoring in a Windows environment](acc-enable-log-monitoring-windows.md)

