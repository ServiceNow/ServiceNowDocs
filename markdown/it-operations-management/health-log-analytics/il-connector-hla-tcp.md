---
title: Configure TCP integrations
description: Configure an integration for sending log data to your ServiceNow instance directly over a TCP/SSL socket.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/health-log-analytics/il-connector-hla-tcp.html
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-09-02"
reading_time_minutes: 4
keywords: [TCP, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure TCP integrations

Configure an integration for sending log data to your ServiceNow instance directly over a TCP/SSL socket.

## Before you begin

-   Verify that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Health Log Analytics \(HLA\) installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/install-health-log-analytics.md).
-   Verify that a service instance is available.
-   Verify that the HLA Engine is up and running.

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    \[Omitted image "hla-mid-log-ingestion.png"\] Alt text: MID Server configuration with Log Ingestion capability enabled.

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

**Note:** For information about streaming data from Logstash to your instance, see the [Streaming data from Logstash to your HLA instance](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0994735) \[KB0994735\] article in the Now Support knowledge base.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(\[Omitted image "integrations-launchpad.png"\] Alt text: Integration Launchpad icon\)

3.  In the **Browse Integrations** tab, enter `TCP` in the search field.

4.  Select the TCP integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can either cancel the setup and complete the prior requirements first, or continue in draft mode and complete them later. Note that you can't activate the integration until all prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see the **Provide details** table in [TCP integration configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/il-connector-hla-tcp-fields.md).

6.  Select **Next**.

7.  In the **Set-up instruction** screen, follow the instructions on the screen to install the integration in the third-party console.

8.  Select **Save draft**.

9.  Select **Activate** to activate the integration.

    **Note:** You can only activate a configured integration when you have fulfilled all the integration prerequisites. If you installed the integration in draft mode, you can activate it later by performing these steps:

    1.  Complete the integration prerequisites.
    2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration.
    3.  In the **Set-up instruction** screen, select **Activate** to activate the integration.

## Result

The integration is activated and the **Overview** screen is displayed. The tile for the integration is available in the **Installed integrations** tab on the Integrations Launchpad.

## What to do next

Leverage the information on the **Overview** tab to refine how HLA reads the log data. For more information, see [Review log data streaming status and sources of an integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/il-connector-overview-tab.md).

**Tip:** Use the More options menu \(\[Omitted image "more-options.png"\] Alt text:\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**, where you can review raw log messages ingested by the integration.

For more information, see:

-   [Log data auto-mapping and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-data-input-automapping.md)
-   [Source type structure adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-source-type-structure-adjustment.md)
-   [Review logs on the Log Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-logs-log-viewer-concept-sow.md)

-   **[TCP integration configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/il-connector-hla-tcp-fields.md)**  
Description of the fields on the TCP integration configuration forms for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-data-input-setup-integrations.md)

