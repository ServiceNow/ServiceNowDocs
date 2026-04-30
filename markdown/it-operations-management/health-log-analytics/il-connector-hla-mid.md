---
title: Configure MID Server integrations
description: Configure an integration for collecting and streaming MID Server log messages to your ServiceNow instance for processing by Health Log Analytics.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-04-08"
reading_time_minutes: 3
keywords: [MID Server, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure MID Server integrations

Configure an integration for collecting and streaming MID Server log messages to your ServiceNow instance for processing by Health Log Analytics.

## Before you begin

**Important:** You can create only one MID Server integration per MID Server.

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Browse integrations** tab, enter `mid` in the search field.

4.  Select the MID Server integration tile.

    **Note:** If you started the integration process without meeting all the prerequisites listed in the Before you begin section, a message appears. You have the option to cancel the integration and complete the missing requirements, or continue in draft mode and fulfill them later. Keep in mind that you can only activate a configured integration when all the prerequisites are met.

5.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see the **Provide details** section in [MID Server integration configuration fields](../reference/il-connector-hla-mid-fields.md).

6.  Select **Advanced Settings** and fill in the fields.

    For a description of the fields, see the **Advanced Settings** section in [MID Server integration configuration fields](../reference/il-connector-hla-mid-fields.md).

7.  Select **Save**.

    The integration is saved and the tile is available in the **Installed integrations** tab on the Integrations Launchpad.

8.  Select **Activate** to activate the integration.

    **Note:** You can only activate a configured integration when you have fulfilled all the prerequisites listed in the Before you begin section.

    The integration is activated and the **Overview** tab is displayed.

9.  If you installed the integration in draft mode, perform these steps to activate it:

    1.  Complete the integration prerequisites.

    2.  In the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**, locate and select the integration.

    3.  On the **Details** tab, select **Activate** to activate the integration.


## Result

MID Server log messages start streaming to your ServiceNow instance. The tile for the integration is available in the **Installed integrations** tab on the Integrations Launchpad.

## What to do next

Review the log data streaming status and sources of the integration on the **Overview** tab. Leverage the displayed information to refine how HLA reads the log data by adjusting your integration configuration. For more information, see [Review log data streaming status and sources of an integration](il-connector-overview-tab.md).

**Note:** You can go directly from this tab to the Data Input Mapping, Source Type Structures, and Log Sources pages with context from the integration. If the log data is not properly mapped, structured, or sourced, you can go back and adjust the configuration of the integration. If the Service Operations Workspace Log Analytics application is installed, the View menu also provides direct access to the Log Viewer, where you can see the raw logs that the integration ingests.

1.  Select the View menu icon \(![View menu icon.](../../health-log-analytics-operator/image/icon-menu-sow.png)\).
2.  Choose the appropriate menu option.
3.  Review the displayed information.
4.  Adjust the integration configuration if needed.

-   **[MID Server integration configuration fields](../reference/il-connector-hla-mid-fields.md)**  
Description of the fields on the MID Server integration configuration forms for Health Log Analytics.

**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

