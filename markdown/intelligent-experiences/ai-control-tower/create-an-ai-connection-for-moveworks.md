---
title: Create an AI connection for Moveworks
description: Create an AI connection for Moveworks in AI Control Tower using the AI Service Graph Connector for Moveworks \(Version 2.0.1\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-moveworks.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Moveworks, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Moveworks

Create an AI connection for Moveworks in AI Control Tower using the AI Service Graph Connector for Moveworks \(Version 2.0.1\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **AI Connector for Moveworks** from the available connectors.

4.  Click **Create connection**.

5.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

6.  Configure and test connection

    1.  Enter the **Connection Name**

    2.  Enter the **Connection URL**

    3.  Enter your **API Key**API Key

    4.  Enter the **Moveworks Org Name**

        The Org name is available in the browser of the Moveworks instance \(Example: my-org-name.moveworks.com\) or navigate to Organizational Details &gt; General information.

    5.  Click **Update and test connection**

    6.  Click **Continue**

7.  Configure import schedule

    1.  Verify that both the parent-scheduled jobs, Discovery and Execution are active as they’re shipped inactive

        **Note:** Ensure to execute the Discovery-scheduled job first.

    2.  Select Run according to your preference

    3.  To run frequency by demand, select **Execute now**

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

8.  Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Click **View all connections** to view the newly created connection.

The AI connection for Moveworks is created and configured.

