---
title: Create an AI connection for n8n
description: Use the  AI Service Graph Connector for n8n  to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [n8n, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for n8n

Use the  AI Service Graph Connector for n8n  to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Service Graph connectors** &gt; **n8n** &gt; **Setup**.

2.  Select **SGC Central** tab.

3.  Select **Add**.

4.  Select **n8n** from all the available connectors.

5.  Select **Create connection**.

    Setup page appears

6.  Configure and test connection.

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL**\(https://&lt;n8n-instance&gt;\)

    3.  Enter the **API Key**.

    4.  Select **Create and test connection**.

    5.  Select **Continue**.

        Setup page appears

7.  Configure import schedule

    1.  Select a parent import schedule job.

    2.  Select the Active check box.

    3.  Select a run and time to schedule the job.

    4.  Select all the additional settings if necessary.

    5.  Promote that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped base system inactive.

        **Note:** Promote to execute the Discovery scheduled job first.

    6.  To run frequency by demand, select **Execute now**

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    7.  Select **Save**.

    8.  Select **Continue**.

8.  Select **View all connections** to view the newly created connection.


## Result

AI connection is created for n8n.

