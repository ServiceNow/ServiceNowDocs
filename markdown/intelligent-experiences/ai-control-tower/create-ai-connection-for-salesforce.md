---
title: Create AI connection for Salesforce
description: Use the AI Service Graph Connector for Salesforce plugin to create AI connections to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Salesforce, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connection for Salesforce

Use the AI Service Graph Connector for Salesforce plugin to create AI connections to discover AI assets such as AI systems, models, prompts, and tools as well as usage data for these AI agents within your ServiceNow AI Control Tower. This usage information is consumed by the AI Control Tower value dashboard.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and n\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connection**.

2.  Select **Add**.

3.  Select **Salesforce** from all the available connectors.

4.  Select **Create connection**.

    Review setup instructions page displays

5.  Verify to follow all the prerequisite steps.

    Setup page appears.

6.  Create and test connection

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL**.

    3.  Enter the **OAuth Client ID**.

    4.  Enter the **OAuth Token URL**.

    5.  Select **Create and test connection**.

    6.  Select **Continue**.

7.  Configure import schedule

    1.  Promote that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped base system inactive.

        **Note:** Promote to execute the Discovery scheduled job first.

    2.  Select Run according to your preference.

    3.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

    5.  Select **View all connections** to view the newly created connection.


## Result

AI Connection is created for Salesforce.

