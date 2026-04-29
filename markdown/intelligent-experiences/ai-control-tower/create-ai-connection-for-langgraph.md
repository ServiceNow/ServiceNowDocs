---
title: Create AI connection for LangGraph
description: Use the AI Service Graph Connector for LangGraph plugin to create AI connections to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these agents. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LangGraph, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connection for LangGraph

Use the AI Service Graph Connector for LangGraph plugin to create AI connections to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these agents. This usage information is consumed by the AI Control Tower value dashboard.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and n\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connection**.

2.  Select **Add**.

3.  Select **LangGraph** from all the available connectors.

4.  Click **Create connection**.

    Setup instructions page displays.

5.  Verify to follow all the prerequisite steps.

    Setup page appears

6.  Create and test connection

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL for LangSmith API**.

    3.  Enter the **Connection URL for LangSmith Rest API**.

    4.  Enter the **API Key**.

        **Note:** Log in to LangGrapH instance and navigate to settings and select API Keys and create an API Key.

    5.  To use a MID Server, select the MID Server check box.

    6.  Click **Create and test connection**.

    7.  Click **Continue**.

7.  Configure import schedule

    1.  Ensure that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive.

        **Note:** Ensure to execute the Discovery-scheduled job first.

    2.  Set the run frequency.

    3.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Click **Continue**.

    5.  Click **View all connections** to view the newly created connection.


## Result

AI connection is created for LangGraph.

