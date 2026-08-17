---
title: Create an AI Connection for Hugging Face
description: Create an AI connection for Hugging Face in AI Control Tower using the AI Service Graph Connector for  Hugging Face \(version 1.1.0\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connections-for-hugging-face.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 1
breadcrumb: [Hugging Face, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI Connection for Hugging Face

Create an AI connection for Hugging Face in AI Control Tower using the AI Service Graph Connector for  Hugging Face \(version 1.1.0\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AI connector for Hugging Face** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

4.  Select **Continue**.

5.  Configure and test connection

    1.  Enter the connection details:

        |Field|Description|
        |-----|-----------|
        |Connection Name|A unique identifier for this connection. For example: SGC\_HuggingFace\_Connection.|
        |Connection URL|The Hugging Face base URL: \(https://huggingface.co\)|
        |API Token|The API token generated in your Hugging Face account settings.|
        |Organization Name|Your Hugging Face organization name. Enter this to discover organization-specific Spaces \(Optional\).|

6.  **Note:** If you're part of a Hugging Face organization, identify your organization name. You can use this when configuring the connection to discover organization-specific Spaces.

7.  Enter the details on Create and test connection:

    1.  Select Create and Test Connection to validate connectivity.
    2.  Verify that the connection test succeeds.
8.  Select **Continue**.

9.  Configuring import schedule:

    **Note:** After creating a connection, enable and configure scheduled imports.

10. Enable Scheduled Jobs:

    **Note:** Two parent scheduled jobs are created by default but are inactive:

    -   Discovery \(Agents\) – Discovers AI agents and assets.
    -   Execution \(Usage\) – Collects usage and observability data.
11. To enable imports, select the Active check box for both scheduled jobs.

    **Note:** Configure the run frequency for each scheduled job based on your organizational needs. For example, run discovery daily to capture new assets and run execution hourly to monitor usage.

12. Execute on Demand:

    1.  To import data immediately without waiting for the scheduled time, select **Execute Now** next to the scheduled job.

    2.  Once configured, scheduled jobs run automatically according to their schedule.

    3.  Select **Continue**.

13. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

