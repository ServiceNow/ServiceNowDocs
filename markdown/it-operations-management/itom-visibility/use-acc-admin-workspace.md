---
title: Use the Agent Client Collector \(ACC\) admin workspace
description: Use the Agent Client Collector \(ACC\) admin workspace to monitor the status of your agents.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 1
breadcrumb: [Use ITOM Infra Services Workspace, ITOM Infra Services Workspace, ITOM Visibility, IT Operations Management]
---

# Use the Agent Client Collector \(ACC\) admin workspace

Use the Agent Client Collector \(ACC\) admin workspace to monitor the status of your agents.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the **ACC agents** icon ![ACC agents icon](../../now-assist-itom/image/acc-agents-icon.png).

    The ACC agents page appears, displaying an overview of the agents in your system on the Dashboard tab.

    ![ACC agents dashboard](../../now-assist-itom/image/acc-agents-dashboard.png "ACC agents dashboard")

3.  Select the **Agents** tab to view a list of the agents.

    ![ACC agents page in Workspace](../../now-assist-itom/image/acc-agents-workspace.png "ACC agents page in Workspace")

    You can filter the displayed agents by selecting one of the boxes at the top of the page. For example, select **Agents down** to filter the list by agents that are currently down.

4.  Select an agent in the agents list to view details of the agent.

    ![Agent details page](../../now-assist-itom/image/agent-record-page.png "Agent details page")

5.  Select the **Agent actions** button and select from actions to perform on the agent.

    |Agent action|Description|
    |------------|-----------|
    |Test Check|On the resulting pop-up window, select a check definition that you want to check on the agents.|
    |Validate ACC plugins|Validate plugins on the selected agent.|
    |Pause data collection|Pause data collection run on the agent when CPU consumption is getting too high.|
    |Upgrade|Upgrade the agent to a more recent version.|
    |Clear ACC plugins|Clear plugins on the agent to remove unwanted plugins.|
    |Collect host data|Manually refresh host data.|

    **Note:** The **Agent actions** button displays only when you have installed Agent Client Collector Framework version 6.0.0 or higher.


**Parent Topic:**[Use ITOM Infra Services Workspace](../../it-operations-management/concept/itom-infra-srv-wrksp-use.md)

**Related topics**  


[MID Server Workspace](../../it-operations-management/concept/itom-infra-srv-wrksp-mid.md)

