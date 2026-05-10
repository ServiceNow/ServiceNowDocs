---
title: Set up a Splunk Poller integration for Health Log Analytics
description: Set up an integration that periodically pulls log data from Splunk to your ServiceNow instance for processing by Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Splunk Polling, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up a Splunk Poller integration for Health Log Analytics

Set up an integration that periodically pulls log data from Splunk to your ServiceNow instance for processing by Health Log Analytics.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

-   The MID Server must support basic authentication.

    **Note:** mTLS is not supported for log ingestion.

-   No more than the default maximum of 10 integrations will stream logs to a single MID Server. You can modify the maximum number by adding the property `sn.occ.log_ingestion.max_datainputs_per_mid` to the MID Server and then changing the default value.

    To find out how many data inputs are streaming logs to the same MID Server, navigate to the **Streaming Sources** table and count the data inputs that stream to a specific MID Server.

-   Consider whether to pull the log data to a single MID Server or to a MID Server cluster.

    In MID Server clusters, multiple MID Servers are grouped together for failover protection. The active integration runs on a single MID Server in the cluster. If that MID Server fails, the system moves its tasks to the next available MID Server in the cluster in a configured order.

    If you want to use a MID Server cluster, verify the following:

    -   The MID Server cluster includes only MID Servers that support basic authentication.
    -   Log ingestion is enabled for each MID Server in the cluster.

        **Note:** If log ingestion is not enabled for the active MID Server, Health Log Analytics enables it automatically.

    -   No more than the default maximum of 10 integrations will stream logs to a single MID Server.

        A cluster passes capacity validation if it contains at least one MID Server with fewer than 10 integrations running on it, even when that MID Server is down.


Role required: evt\_mgmt\_admin

## About this task

You set up integrations through the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, enter `Splunk Poller` in the search field.

5.  Select the Splunk Poller integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see the **Provide details** table in [Splunk Poller integration configuration fields](../reference/il-connector-hla-splunkpoll-fields.md).

7.  Select **Next**.

8.  On the **Set data retrieval method** form, fill in the fields.

    For a description of the fields, see the **Set data retrieval method** table in [Splunk Poller integration configuration fields](../reference/il-connector-hla-splunkpoll-fields.md).

9.  Select **Advanced settings** and fill in the advanced configuration fields.

    For a description of the fields, see [Splunk Poller integration configuration fields](../reference/il-connector-hla-splunkpoll-fields.md).

10. Select **Test and save** to save the integration to the database and test connectivity.

11. Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        In the pop-up window, select **Test &amp; Save** to save the integration to the database and test connectivity. If an error is returned, adjust the configuration as suggested in the error message and then try to activate the integration again.

        When the test is successful, the integration is activated and the **Overview** tab is displayed. On the Integrations Launchpad, the integration tile is available in the **Installed integrations** tab.

    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad. It appears in the **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the integration later. For more information, see [Activate a draft integration in Health Log Analytics](il-connector-hla-activate-draft.md).


## What to do next

On the **Overview** tab, do the following:

-   Use the displayed information to refine how Health Log Analytics reads the log data. For more information, see [Review log streaming data and adjust integration settings in Health Log Analytics](il-connector-overview-tab.md).
-   Use the More options menu \(![More options menu icon.](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**. Use the **Log Viewer** to review raw log messages ingested by the integration. For more information, see:
    -   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
    -   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
    -   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

