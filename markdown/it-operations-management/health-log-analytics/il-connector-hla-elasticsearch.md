---
title: Set up an Elasticsearch integration for Health Log Analytics
description: Set up an integration to stream log data seamlessly from Elasticsearch indices to your instance for Health Log Analytics processing.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Elasticsearch, data input, integration, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up an Elasticsearch integration for Health Log Analytics

Set up an integration to stream log data seamlessly from Elasticsearch indices to your instance for Health Log Analytics processing.

## Before you begin

**Note:** Health Log Analytics supports Elasticsearch versions above 7.10.2 and below 8.18.2. For advanced Elasticsearch log streaming guidance, see the [Stream logs using Elasticsearch data input - Advanced guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1080162) \[KB1080162\] article in the Now Support Knowledge Base.

-   Verify that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Install Health Log Analytics \(HLA\)](install-health-log-analytics.md).
-   Verify that a service instance is available.
-   Verify that the Health Log Analytics AI Engine is up and running.

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## About this task

You set up integrations through the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

4.  In the **Browse integrations** tab, enter `Elasticsearch` in the search field.

5.  Select the Elasticsearch integration tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

6.  On the **Provide details** form, fill in the fields.

    For a description of the fields, see the **Provide details** table in [Elasticsearch integration configuration fields](../reference/il-connector-hla-elastic-fields.md).

7.  Select **Next**.

8.  On the **Set data retrieval method** form, fill in the fields.

    For a description of the fields, see [Elasticsearch integration configuration fields](../reference/il-connector-hla-elastic-fields.md).

9.  Select **Advanced settings** to set advanced configuration fields.

    For a description of the fields, see the **Advanced settings** table in [Elasticsearch integration configuration fields](../reference/il-connector-hla-elastic-fields.md).

10. Do one of the following:

    -   If you completed all the prerequisites before starting the configuration, select **Activate**.

        In the pop-up window, select **Test &amp; Save** to save the integration to the database and test connectivity. If an error is returned, adjust the configuration as suggested in the error message and then try to activate the integration again.

        When the test is successful, you can activate the integration either with or without AI-powered capabilities. Select the appropriate option:

        -   **Activate with AI** enables AI-powered automatic mapping of log data. When the integration is activated successfully, the **Overview** tab is displayed. Now Assist collects and analyzes log data. An AI icon indicates that Now Assist auto-maps log data to service instances and components for contextual alert generation.
        -   **Activate** activates the integration without AI-powered mapping. The integration is activated and the **Overview** tab is displayed.
    -   If you didn't complete all the prior requirements, select **Save draft**.

        The system saves the integration as a draft in the Integrations Launchpad. It appears in the **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the integration later. For more information, see [Activate a draft integration in Health Log Analytics](il-connector-hla-activate-draft.md).


## What to do next

On the **Overview** tab, do the following:

-   Use the displayed information to refine how Health Log Analytics reads the log data. For more information, see [Review log streaming data and adjust integration settings in Health Log Analytics](il-connector-overview-tab.md).
-   Use the More options menu \(![More options menu icon.](../image/more-options.png)\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**. Use the **Log Viewer** to review raw log messages ingested by the integration. For more information, see:
    -   [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)
    -   [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md)
    -   [Review logs on the Log Viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept-sow.md)

If you activated the integration with AI, verify that AI correctly auto-mapped log data to service instances and components. To do this, select **View mapping** under **Log context mapping**. You can override the AI mapping by selecting a different log field from each list. For more information, see [Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics](il-connector-hla-map-business-context.md).

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

