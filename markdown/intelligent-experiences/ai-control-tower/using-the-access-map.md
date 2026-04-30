---
title: Using the access map
description: Learn how to use the Access map in AI Control Tower.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Using the access map

Learn how to use the **Access map** in AI Control Tower.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## Procedure

1.  Select **access map** in the header of the **Security and privacy** tab.

    You can also access the map by navigating to **All** &gt; **AI Security and Privacy** &gt; **Access Map**.

2.  Select an AI agent/agentic workflow using the **Access map**.

    You can also use the **Search by agent or workflow** field, and the **AI agents** and **Agentic workflows** to refine your search. Additionally, agents with access issues will have a![Warning](../image/sp-tab-access-map-issue-icon2.png) icon.

3.  In the node map, select a node to view the connections of your AI agent/agentic workflow.

    Agents with access issues with be highlighted with a ![Red warning](../image/sp-tab-access-map-issue-icon.png) icon in the map.

4.  Select a node to get further details and configure settings.

<table id="table_ahl_13r_xfc"><thead><tr><th>

Icon

</th><th>

Label

</th><th>

Details

</th></tr></thead><tbody><tr><td>

![Agentic workflow node](../image/sp-tab-access-map-icon1.png)

</td><td>

Agentic workflow

</td><td>

-   **Description**

A brief description of the workflow

-   **Domain**

The domain scope of the workflow

-   **Execution mode**

How the workflow is executed \(Autonomous or manual\)

-   **Created by**

The creator of the workflow

</td></tr><tr><td>

![AI Agent node](../image/sp-tab-access-map-icon2.png)

</td><td>

Agent

</td><td>

-   **Description**

A brief description of the agent

-   **Domain**

The domain scope of the agent

-   **Created by**

The creator of the workflow

-   **Tables accessed**

Review the table accesses of the agent over the last month. Select **Operation** to filter specific access operations.

 **Note:** Only agents with access issues will display the **Access issues** details.

 -   **Access issues**

Details the resources and operations causing the access issues.

-   **Resource**

The resource the agent is having issues accessing

-   **Operation**

The operation the agent attempted

-   **Count**

The number of times of the agent encounter the issue

</td></tr><tr><td>

![Tool node](../image/sp-tab-access-map-icon3.png)

</td><td>

Tool

</td><td>

-   **Description**

The description of the tool.

-   **Domain**

The domain scope of the tool.

-   **Execution mode**

The execution mode of the tool \(Supervised or Autonomous\)

-   **Type**

The type of tool

-   **Target record**

The record the tool modifies.

-   **Created by**

The creator of the tool

 **Note:** Select **Open tool record** to view additional tool details.

</td></tr></tbody>
</table>
**Parent Topic:**[Using AI Control Tower](../concept/using-ai-control-tower.md)

