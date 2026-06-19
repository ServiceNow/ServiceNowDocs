---
title: Create an AI connection for Snowflake
description: Create an AI connection for Snowflake in AI Control Tower using the  AI Service Graph Connector for Snowflake.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-ai-connections-for-snowflake.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 1
breadcrumb: [Snowflake, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Snowflake

Create an AI connection for Snowflake in AI Control Tower using the  AI Service Graph Connector for Snowflake.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **AI Connector for Snowflake** from all the available connectors.

4.  Click **Create connection**.

    Review setup instructions page displays the prerequisites for setting up Snowflake Keypair connection.

5.  Verify to follow all the prerequisite steps.

6.  Select **Next**.

7.  Enter the connection details:

8.  | | |
|---|---|
|Connection name|A unique identifier for this connection. For example: SGC\_Snowflake\_KeyPair\_Connection|
|Connection URL|Your Snowflake account URL in account\_locator format. For example: https://&lt;account\_locator&gt;.snowflakecomputing.com|
|Snowflake username|The service account name created in Snowflake.|
|Public Key Fingerprint|The SHA256 fingerprint of your public key from Snowflake.|
|Certificate \(JKS\)|The X509 certificate \(sys\_certificate record\) containing your Java Keystore with private key.|
|Certificate Password|The password for your keystore.|
|Key Alias|The alias for your private key within the keystore..|

    **Note:** For detailed instructions on configuring JWT key-pair authentication, see the [Configuring Keystore for Snowflake Keypair authentication \[KB2834688\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB2834688) article in the Now Support Knowledge Base.

9.  Create and test connection.

    1.  Click Create and Test Connection to validate connectivity.
    2.  If the test succeeds, the connection is created and you can proceed to schedule imports.
    3.  If validation fails, verify your Snowflake credentials, network policies, and key-pair configuration.
10. Configure import schedule

    **Note:** After creating a connection, enable and configure scheduled imports.

11. Enable Scheduled Jobs

    **Note:** Two parent scheduled jobs are created by default but are inactive:

    -   Discovery \(Agents\) – Discovers AI agents and assets.
    -   Execution \(Usage\) – Collects usage and observability data.
12. To enable imports, select the Active check box for both scheduled jobs.

    **Note:** Configure the run frequency for each scheduled job based on your organizational needs. For example, run discovery daily to capture new assets and run execution hourly to monitor usage.

13. Execute on Demand

    1.  To import data immediately without waiting for the scheduled time, click Execute Now next to the scheduled job.

    2.  Once configured, scheduled jobs run automatically according to their schedule.

14. Select **View all connections** to view the newly created connection


## Result

The AI connection for Snowflake is created and configured.

