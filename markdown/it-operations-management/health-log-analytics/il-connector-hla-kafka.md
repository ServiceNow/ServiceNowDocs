---
title: Configure Apache Kafka integrations
description: Configure an integration for streaming log data from Apache Kafka to your ServiceNow instance for processing by Health Log Analytics.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-04-08"
reading_time_minutes: 5
keywords: [Apache Kafka, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure Apache Kafka integrations

Configure an integration for streaming log data from Apache Kafka to your ServiceNow instance for processing by Health Log Analytics.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the IP address of the MID Server is exposed by network address translation \(NAT\), a load balancer or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).

-   Consider whether to pull the log data to a single MID Server or to a MID Server cluster.

    In MID Server clusters, multiple MID Servers are grouped together for failover protection. The active integration runs on a single MID Server in the cluster. If that MID Server fails, the system moves its tasks to the next available MID Server in the cluster in a configured order.

    If you decide to use a MID Server cluster, ensure the following:

    -   The MID Server cluster includes only MID Servers that support basic authentication.

        **Note:** mTLS is not supported for log ingestion.

    -   Log ingestion is enabled for each MID Server in the cluster.

        **Note:** If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.

    -   No more than the default maximum of 10 integrations will pull logs to a single MID Server.

        A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 integrations running on it, even when that MID Server is down.


Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Browse integrations** tab, search for `Kafka`.

4.  Select the Kafka integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can either cancel the setup and complete the prior requirements first, or continue in draft mode and complete them later. Note that you can't activate the integration until all prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see the **Provide details** table in [Apache Kafka integration configuration fields](../reference/il-connector-hla-kafka-fields.md).

6.  Select **Next**.

7.  On the **Set data retrieval method** form, fill in the fields.

    For a description of the fields, see the **Set data retrieval method** table in [Apache Kafka integration configuration fields](../reference/il-connector-hla-kafka-fields.md).

8.  Select **Advanced settings** and fill in the advanced configuration fields.

    For a description of the fields, see the **Advanced settings** table in [Apache Kafka integration configuration fields](../reference/il-connector-hla-kafka-fields.md).

9.  Select **Test and save** to save the integration to the database and test connectivity.

10. Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        In the pop-up screen, select **Test &amp; save** to save the integration to the database and test connectivity. If an error is returned, adjust the configuration as suggested in the error message and then try to activate the integration again.

        Once the test is successful, the integration is activated and the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

        **Note:** To test and save the integration without activating it, select the **Test &amp; save** button at the top of the page.

    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the installation later. For more information, see the **What to do next** section.


## What to do next

Leverage the information on the **Overview** tab to refine how HLA reads the log data. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

**Tip:** Use the More options menu \(![](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**, where you can review raw log messages ingested by the integration.

For more information, see:

-   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
-   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
-   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

If you saved the integration as a draft, perform these steps to activate it later:

1.  Complete all the prior requirements.
2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration tile.
3.  On the configuration screen, select **Activate**.

    Select **Test &amp; save** to save the integration to the database and test connectivity. If an error is returned, adjust the configuration as suggested in the error message and then try to activate the integration again.

    Once the test is successful, the integration is activated and the **Overview** tab is displayed. The integration tile is available in the **Installed integrations** tab on the Integrations Launchpad.

    **Note:** To test and save the integration without activating it, select the **Test &amp; save** button at the top of the page.


-   **[Apache Kafka integration configuration fields](../reference/il-connector-hla-kafka-fields.md)**  
Description of the fields on the Apache Kafka integration configuration forms for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

