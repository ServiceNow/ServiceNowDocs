---
title: Configure Splunk UDP integrations
description: Configure an integration to stream log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder. Health Log Analytics processes the ingested log data.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-04-08"
reading_time_minutes: 4
keywords: [Splunk UDP, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure Splunk UDP integrations

Configure an integration to stream log messages to your ServiceNow instance over the UDP transport protocol using a Splunk heavy forwarder. Health Log Analytics processes the ingested log data.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Browse integrations** tab, enter `Splunk` in the search field.

4.  Select the Splunk UDP integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can either cancel the setup and complete the prior requirements first, or continue in draft mode and complete them later. Note that you can't activate the integration until all prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see **Provide details** table in [Splunk UDP integration configuration fields](../reference/il-connector-hla-splunkudp-fields.md).

6.  Select **Advanced settings** and fill in the advanced configuration fields.

    For a description of the fields, see the **Advanced settings** table in [Splunk UDP integration configuration fields](../reference/il-connector-hla-splunkudp-fields.md).

7.  Select **Next**.

8.  Follow the procedure on the **Set-up instruction** screen to install the integration in the third-party console.

    **Note:** The procedure varies based on your configurations.

9.  Select **Save draft**.

10. Select **Activate** to activate the integration.

    **Note:** You can only activate a configured integration when you have fulfilled all the integration prerequisites. If you installed the integration in draft mode, you can activate it later by performing these steps:

    1.  Complete the integration prerequisites.
    2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration.
    3.  In the **Set-up instruction** screen, select **Activate** to activate the integration.

## Result

The integration is activated and the **Overview** screen is displayed. The tile for the integration is available in the **Installed integrations** tab on the Integrations Launchpad.

## What to do next

Leverage the information on the **Overview** tab to refine how HLA reads the log data. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

**Tip:** Use the More options menu \(![](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**, where you can review raw log messages ingested by the integration.

For more information, see:

-   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
-   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
-   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

-   **[Splunk UDP integration configuration fields](../reference/il-connector-hla-splunkudp-fields.md)**  
Description of the fields on the Splunk UDP integration configuration forms for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

