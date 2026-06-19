---
title: Create an AI Connection for Hugging Face
description: Create an AI connection for Hugging Face in AI Control Tower using the  Hugging Face connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connections-for-hugging-face.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 1
breadcrumb: [Hugging Face, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI Connection for Hugging Face

Create an AI connection for Hugging Face in AI Control Tower using the  Hugging Face connector.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **AI Control Tower** &gt; **Configuration** &gt; **AI connections**.

2.  Select **Add**.

3.  Select **AI connector for Hugging Face** from all the available connectors.

4.  Select **Create connection**.

    The Review setup instructions page displays

5.  Verify to follow all the prerequisite steps.

    Setup page appears.

6.  Click **Continue**

7.  Enter the connection details.

8.  | | |
|---|---|
|Connection name|A unique identifier for this connection. For example: SGC\_HuggingFace\_Connection|
|Connection URL|The Hugging Face base URL: https://huggingface.co|
|API Token|The API token generated in your Hugging Face account settings.|
|Organization Name|Your Hugging Face organization name. Enter this to discover organization-specific Spaces \(Optional\).|

    **Note:** If you're part of a Hugging Face organization, identify your organization name. You can use this when configuring the connection to discover organization-specific Spaces.

9.  Create and test connection.

    1.  Click Create and Test Connection to validate connectivity.
    2.  Verify that the connection test succeeds.
10. Click **Continue**

11. Configuring import schedule

    **Note:** After creating a connection, enable and configure scheduled imports.

12. Enable Scheduled Jobs

    **Note:** Two parent scheduled jobs are created by default but are inactive:

    -   Discovery \(Agents\) – Discovers AI agents and assets.
    -   Execution \(Usage\) – Collects usage and observability data.
13. To enable imports, select the Active check box for both scheduled jobs.

    **Note:** Configure the run frequency for each scheduled job based on your organizational needs. For example, run discovery daily to capture new assets and run execution hourly to monitor usage.

14. Execute on Demand

    1.  To import data immediately without waiting for the scheduled time, click Execute Now next to the scheduled job.

    2.  Once configured, scheduled jobs run automatically according to their schedule.

15. Select **View all connections** to view the newly created connection


## Result

The AI connection for Hugging Face is created and configured.

