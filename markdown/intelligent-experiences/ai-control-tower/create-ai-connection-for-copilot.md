---
title: Create an AI connection for Copilot Studio
description: Create an AI connection for Copilot in AI Control Tower using the  AI Service Graph Connector for Microsoft.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connection-for-copilot.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Copilot Studio

Create an AI connection for Copilot in AI Control Tower using the  AI Service Graph Connector for Microsoft.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower workspace** &gt; **Configurations** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **AI connector for Microsoft** from all the available connectors.

4.  Click **Create connection**.

5.  Select the Microsoft Copilot check box.

6.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

7.  Select **Continue**.

8.  Setup page appears

9.  **Configure and Test Copilot connection**

    1.  Enter the **Connection name**

    2.  Enter the **Environment IDs**

        **Note:** You can obtain the Environment ID from Settings &gt; Session details &gt; Environment ID in your environment.

    3.  Enter the **OAuth client ID**

    4.  Enter the **OAuth Client Secret**

    5.  Enter the **Tenant ID**

    6.  Select **Create and test connection**

    7.  Select **Continue**

10. **Configure Copilot import schedule**

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped base system inactive

        Ensure to execute the Discovery-scheduled job first.

    2.  Set the run frequency.

    3.  To run frequency by demand, select Execute now to run

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**

    5.  Select **View all connections** to view the newly created connection


## Result

The AI connection for Copilot Studio is created and configured.

