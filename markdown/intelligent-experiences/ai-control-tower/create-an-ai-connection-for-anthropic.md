---
title: Create an AI connection for Anthropic \(v2.0.6\)
description: Create an AI connection for Anthropic in AI Control Tower using the AI Service Graph Connector for Anthropic \(version 2.0.6\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-anthropic.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Anthropic, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Anthropic \(v2.0.6\)

Create an AI connection for Anthropic in AI Control Tower using the AI Service Graph Connector for Anthropic \(version 2.0.6\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **Anthropic** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the Anthropic prerequisites and perform the Anthropic setup.

4.  Select **Continue**.

5.  Configure Anthropic connection:

    1.  Enter the following details for the connection.

        |Field|Description|
        |-----|-----------|
        |Connection name|Name to identify the Anthropic connection.|
        |Connection URL|Anthropic account URL.|
        |API Key|Anthropic API key.|

    2.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    3.  Select **Continue**.

6.  Configure import schedules:

    1.  Open the discovery scheduled job.

    2.  Select the **Active** check box.

    3.  Select Run according to your preference.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  To run frequency by demand, select **Execute now**.

    5.  Select **Continue**.

7.  Setup Analytics connection:

    1.  Select **Enable analytics usage connection setup**.

        To use analytics, you must have an Anthropic Enterprise plan subscription. Select **Submit** to continue, or **Skip** if you don't have one.

    2.  Select **Submit**.

8.  Configure usage connection:

    1.  Enter the following details for the connection.

        |Field|Description|
        |-----|-----------|
        |Connection name|Name to identify the Anthropic usage connection.|
        |Connection URL|Anthropic account URL|
        |API Key|Anthropic Analytics API key|

    2.  Enter the **Connection name**.

    3.  Enter the **Connection URL**.

    4.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    5.  Select **Continue**.

9.  Configure import schedules:

    1.  Open the discovery scheduled job.

    2.  Select the **Active** check box.

    3.  Select Run according to your preference.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  To run frequency by demand, select **Execute now**.

    5.  Select **Continue**.

10. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

