---
title: Create an AI connection for OpenAI
description: Create an AI connection for OpenAI in AI Control Tower using the  AI Service Graph Connector for OpenAI \(version 1.0.0\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-openai.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-06-30"
reading_time_minutes: 1
breadcrumb: [OpenAI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for OpenAI

Create an AI connection for OpenAI in AI Control Tower using the  AI Service Graph Connector for OpenAI \(version 1.0.0\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **OpenAI** from the available connectors and then select **Create connection**.

3.  Review setup instructions page appears.

    **Note:** Verify to have the OpenAI prerequisites and perform the OpenAI setup.

4.  Select **Continue**.

    **Note:** OpenAI Setup contains Configure OpenAI connection and Configure Import schedules.

5.  Configure OpenAI connection:

    **Note:** These required credentials are for OpenAI Standard API key.

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL**.

    3.  Enter the **API key**.

        **Note:** To get API keys, navigate to OpenAI profile &gt; User profile &gt; Organization settings &gt; API keys &gt; +Create new secret key

    4.  Select **Create and test connection**

        A banner appears displaying Connection verified.

    5.  Select **Continue**.

6.  Configure import schedules:

    1.  Open the discovery scheduled job.

    2.  Select the **Active** check box.

    3.  Select Run according to your preference.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  To run frequency by demand, select **Execute now**.

    5.  Select **Continue**.

    **Note:** OpenAI Usage Setup contains Configure OpenAI connection and Configure Import schedules.

7.  Enter the details on Configure OpenAI Usage connection:

    **Note:** These required credentials are for Admin API key.

    1.  Enter the **Connection Name**.

    2.  Enter the **Connection URL**.

    3.  Enter the **API key**.

        **Note:** To get API keys, navigate to OpenAI profile &gt; User profile &gt; Organization settings &gt; Admin keys &gt; +Create new Admin key &gt; Name &gt; Create admin key

    4.  Select **Update and test connection**.

    5.  Select **Continue**.

8.  Configure import schedules:

    1.  Open the Model usage scheduled job.

    2.  Select the **Active** check box.

    3.  Select Run frequency according to your preference.

    4.  To run frequency on demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

9.  Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

