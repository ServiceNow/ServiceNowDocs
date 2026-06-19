---
title: Create an AI connection for LangGraph
description: Create an AI connection for LangGraph in AI Control Tower using the  AI Service Graph Connector for LangGraph.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connection-for-langgraph.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LangGraph, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for LangGraph

Create an AI connection for LangGraph in AI Control Tower using the  AI Service Graph Connector for LangGraph.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **LangGraph** from all the available connectors.

4.  Click **Create connection**.

    Setup instructions page displays.

5.  Verify to follow all the prerequisite steps.

    Setup page appears

6.  Create and test connection

    1.  Enter the **Connection Name**

    2.  Enter the **Connection URL for LangSmith API**

    3.  Enter the **Connection URL for LangSmith Host API**

        **Note:** For sub-steps b and c, you don't have to change the default value unless LangSmith is hosted.

    4.  Enter the **API Key**

        **Note:** Log in to LangGraph instance and navigate to settings and select API Keys and create an API Key.

    5.  To use a MID Server, select the MID Server check box

    6.  Select **Create and test connection**

    7.  Select **Continue**

7.  Configure import schedule

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive

        **Note:** Ensure to execute the Discovery-scheduled job first.

    2.  Set the run frequency

    3.  To run frequency by demand, select **Execute now**

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

    5.  Select **View all connections** to view the newly created connection.


## Result

The AI connection for LangGraph is created and configured.

