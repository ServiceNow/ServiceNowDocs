---
title: Create an AI connection for Snowflake
description: Create an AI connection for Snowflake in AI Control Tower using the  AI Service Graph Connector for Snowflake \(version 2.0.5\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connections-for-snowflake.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 1
breadcrumb: [Snowflake, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Snowflake

Create an AI connection for Snowflake in AI Control Tower using the  AI Service Graph Connector for Snowflake \(version 2.0.5\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AI Connector for Snowflake** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays the prerequisites for setting up Snowflake Keypair connection.

    **Note:** Verify to follow all the prerequisite steps.

4.  Select **Next**.

5.  Enter the connection details:

    |Field|Description|
    |-----|-----------|
    |Connection name|A unique identifier for this connection. For example: SGC\_Snowflake\_KeyPair\_Connection|
    |Connection URL|Your Snowflake account URL in account\_locator format. For example: https://&lt;account\_locator&gt;.snowflakecomputing.com|
    |Snowflake username|The service account name created in Snowflake.|
    |Public Key Fingerprint|The SHA256 fingerprint of your public key from Snowflake.|
    |Certificate \(JKS\)|The X509 certificate \(sys\_certificate record\) containing your Java Keystore with private key.|
    |Certificate Password|The password for your keystore.|
    |Key Alias|The alias for your private key within the keystore.|

6.  **Note:** For detailed instructions on configuring JWT key-pair authentication, see the [Configuring Keystore for Snowflake Keypair authentication \[KB2834688\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB2834688) article in the Now Support Knowledge Base.

7.  Enter the details on Create and test connection:

    1.  Select **Create and test connection** to validate connectivity.
    2.  If the test succeeds, the connection is created and you can proceed to schedule imports.
    3.  If validation fails, verify your Snowflake credentials, network policies, and key-pair configuration.
8.  Configure import schedule:

    **Note:** After creating a connection, enable and configure scheduled imports.

9.  Enable Scheduled Jobs.

    **Note:** Two parent scheduled jobs are created by default but are inactive:

    -   Discovery \(Agents\) – Discovers AI agents and assets.
    -   Execution \(Usage\) – Collects usage and observability data.
10. To enable imports, select the Active check box for both scheduled jobs.

    **Note:** Configure the run frequency for each scheduled job based on your organizational needs. For example, run discovery daily to capture new assets and run execution hourly to monitor usage.

11. Execute on Demand:

    1.  To import data immediately without waiting for the scheduled time, select **Execute Now** next to the scheduled job.

    2.  Once configured, scheduled jobs run automatically according to their schedule.

    3.  Select **Continue**.

12. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

