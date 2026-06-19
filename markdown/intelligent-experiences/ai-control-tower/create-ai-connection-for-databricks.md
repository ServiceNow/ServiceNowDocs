---
title: Create an AI connection for Databricks
description: Create an AI connection for Databricks in AI Control Tower using the  AI Service Graph Connector for Databricks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connection-for-databricks.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Databricks, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Databricks

Create an AI connection for Databricks in AI Control Tower using the  AI Service Graph Connector for Databricks.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **Databricks** from all the available connectors.

4.  Click **Create connection**.

    The Review setup instructions page displays

5.  Verify to follow all the prerequisite steps.

    Setup page appears.

6.  Create and test connection

    1.  Enter the **Connection Name**

    2.  Enter the **Connection URL**

    3.  Enter the **OAuth Client ID**

    4.  Enter the **OAuth Client Secret**

    5.  Enter the **OAuth Token URL**

    6.  Select **Create and test connection**

    7.  Select **Continue**

7.  Configure import schedule

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped inactive

        **Note:** Ensure to execute the Discovery-scheduled job first

    2.  Select Run according to your preference.

    3.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule

    4.  Select **Continue**.

    5.  Select **View all connections** to view the newly created connection.


## Result

The AI connection for Databricks is created and configured.

