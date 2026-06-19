---
title: Set up a Splunk OpenTelemetry Collector \(MID-less\) integration for Health Log Analytics
description: Set up a Splunk OpenTelemetry Collector integration to stream Splunk log data directly to your ServiceNow instance using the OpenTelemetry \(OTLP\) protocol, without a MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/il-connector-hla-splunk-otel.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 5
keywords: [Health Log Analytics, HLA, Splunk, OpenTelemetry, OTel, integration, data input, MID-less log streaming, ITOM Gateway, JSON Web Token \(JWT\)]
breadcrumb: [MID-less integrations, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up a Splunk OpenTelemetry Collector \(MID-less\) integration for Health Log Analytics

Set up a Splunk OpenTelemetry Collector integration to stream Splunk log data directly to your ServiceNow instance using the OpenTelemetry \(OTLP\) protocol, without a MID Server.

## Before you begin

Set up MID-less log streaming via ITOM Gateway. Choose the deployment method based on your expected log volume. For more information, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).

Role required: evt\_mgmt\_admin

## About this task

Set up an integration from the Integrations Launchpad in Service Operations Workspace, which you access from the ITOM AIOps configuration center. The AIOps configuration center is a centralized workspace for configuring and managing AIOps features from a single place. The integrations setup process reduces implementation time compared to manual data input setup in the classic interface in Health Log Analytics. For more information, see [Integrations Launchpad in Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/integrations-launchpad.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the Integrate section, under Integrations, select **Add integration**.

    The Integrations Launchpad appears.

3.  In the **Browse integrations** tab, search for the Splunk OpenTelemetry \(MID-less\) integration and select its tile.

    **Note:** If you start an integration setup before meeting all prerequisites, a message appears. You can cancel the setup and complete the prior requirements first. Alternatively, you can continue in draft mode and complete the requirements later. Note that you can't activate the integration until you have completed all the prerequisites.

4.  On the **Provide details** form, fill in the fields and then select **Next**.

5.  On the **Set-up instruction** screen, follow the provided procedure to enable sending Splunk log data to ServiceNow using OpenTelemetry.

    1.  Copy the provided access token, endpoint, and integration ID to the clipboard.

        These credentials enable Cribl to securely send logs to the ServiceNow ITOM Gateway.

        |Credential|Description|
        |----------|-----------|
        |Access Token|The JWT credential passed with every request.|
        |Endpoint|The address to which the data is sent: the ITOM Gateway.|
        |Integration ID|The ID with which the integration identifies to ServiceNow.|

    2.  In your OpenTelemetry Collector configuration file, exporters section, add an OTLP exporter to forward telemetry data to ServiceNow.

        Typically, the configuration file is `otel-collector-config.yaml`.

        ```
        exporters:
          otlp/servicenow:
            endpoint: itomgw-prod-gateway-phxbwi.sncapps.service-now.com:443
            headers:
              # Reads the access token from the SERVICENOW_ACCESS_TOKEN env variable
              servicenow-access-token: ${SERVICENOW_ACCESS_TOKEN}
              servicenow-integration-id: 7b36df1387f00f10d696c845dabb351f
        ```

        This step tells the collector where to send the data and how to authenticate with your instance.

        For more detailed instructions, see the [Configure an OpenTelemetry Collector or 3rd Party agent to send data to HLA \[KB2117238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2117238) article in the Now Support knowledge base. For further assistance, contact your OpenTelemetry Collector administrator.

6.  On the Splunk OpenTelemetry Collector integration **Set-up instruction** screen, complete the integration setup by doing one of the following.

    |Option|Description|
    |------|-----------|
    |**Prerequisites complete — activate with AI**|Select **Activate with AI** to enable AI-powered automatic mapping of log data. When the integration is activated successfully, the **Overview** tab is displayed and Now Assist collects and analyzes log data. An AI icon indicates that Now Assist auto-maps log data to service instances and components for contextual alert generation.|
    |**Prerequisites complete — activate without AI**|Select **Activate** to activate the integration without AI-powered mapping. The integration is activated and the **Overview** tab is displayed.|
    |**Prerequisites not complete**|Select **Save draft**. The system saves the integration as a draft in the Integrations Launchpad **Installed integrations** tab, under **Waiting for your action**. You can complete the prerequisites and activate the integration later. For more information, see [Activate a draft integration in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-activate-draft.md).|


## What to do next

On the **Overview** tab, do the following:

-   Use the displayed information to refine how Health Log Analytics reads the log data. For more information, see [Review log streaming data and adjust integration settings in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-overview-tab.md).
-   Use the More options menu \(\[Omitted image "more-options.png"\] Alt text: More options menu icon.\) to open the **Data Input Mapping**, **Source Type Structures**, or **Log Sources** pages with context from the integration. If your log data is not properly mapped, structured, or sourced, go back and adjust the configuration. If the Service Operations Workspace Log Analytics application is installed, the More options menu also provides direct access to the **Log Viewer**. Use the **Log Viewer** to review raw log messages ingested by the integration. For more information, see:
    -   [Log data auto-mapping and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-automapping.md)
    -   [Source type structure adjustment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-source-type-structure-adjustment.md)
    -   [Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-logs-log-viewer-concept-sow.md)

If you activated the integration with AI, verify that AI correctly auto-mapped log data to service instances and components. To do this, select **View mapping** under **Log context mapping**. You can override the AI mapping by selecting a different log field from each list. For more information, see [Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-map-business-context.md).

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

