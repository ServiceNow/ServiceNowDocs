---
title: Create an AI connection for n8n
description: Create an AI connection for n8n in AI Control Tower using the  n8n connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-a-ai-connection-for-n8n.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [n8n, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for n8n

Create an AI connection for n8n in AI Control Tower using the  n8n connector.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connection**.

2.  Click **Add**.

3.  Select **n8n** from all the available connectors.

4.  Click **Create connection**.

    Setup page appears

5.  Configure and test connection.

    1.  Enter the **Connection Name**

    2.  Enter the **Connection URL**\(https://&lt;n8n-instance&gt;\)

    3.  Enter the **API Key**

    4.  Select **Create and test connection**

    5.  Select **Continue**

        Setup page appears

6.  Configure import schedule

    1.  Select a parent import schedule job

    2.  Select the Active check box

    3.  Select run and time to schedule the job

    4.  Select all the additional settings if necessary

    5.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped out inactive

        **Note:** Ensure to execute the Discovery-scheduled job first.

    6.  To run frequency by demand, select **Execute now**

        **Note:** This is an optional step as the schedule imports run according to the schedule

    7.  Select **Save**

    8.  Select **Continue**

7.  Select **View all connections** to view the newly created connection.


## Result

The AI connection for n8n is created and configured.

