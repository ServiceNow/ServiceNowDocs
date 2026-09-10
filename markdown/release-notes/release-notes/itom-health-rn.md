---
title: ITOM Health release notes
description: The ServiceNow ITOM Health product helps you to keep track and maintain the health of the services in your organization. ITOM Health was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ITOM Health release notes

The ServiceNow® ITOM Health product helps you to keep track and maintain the health of the services in your organization. ITOM Health was enhanced and updated in the Yokohama release.

## About ITOM Health

Health Log Analytics highlights:

-   Pull data from Splunk consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk.
-   Use your Splunk data input to ingest data from Splunk in a pre-processed, structured format.
-   Integrate with log data connectors from the Integrations Launchpad
-   Use dedicated Cribl, Edge Delta and Vector Agent data inputs to streamline HLA data ingestion with tools handling large log volumes.
-   Generate a description of Health Log Analytics alerts using Now Assist.

Event Management highlights:

-   Focus on critical connections and dependencies by reviewing network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times.

[Service Operations Workspace for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/sow-landing-page-itom.md)

-   Starting with version 26.3.1, benefit from the new alert grouping based on network traffic correlation:
    -   Use Express List® to investigate network traffic-based alert groups
    -   View connections between network traffic-based alerts in Link View.
    -   Starting with version 2.5.3, review alert group analysis by Now Assist
-   Review relevant information in the Now Assist panel based on records selected in Express List®.
-   Enable team-level operators to create and manage new alert automations by assigning the new team\_operator role.
-   Map current alert field values to new specified values through the new **Change alert values** option in the Enrich automation section.
-   Track and optimize grouping efficiency by viewing key details such as total alerts, alert groups, ungrouped alerts, and compression in Group Automation. Simulate other group types, such as CMDB, ML, and text-based grouping.

Agent Client Collector highlights:

-   Create tasks to address Agent Client Collector errors.
-   Discover java installation information using file-based discovery.
-   Upgrade many agents at once using high-volume upgrade of Agent Client Collector.
-   Conserve the MID Server resources for more persistent features by using MID-less installation.

See [ITOM Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-health-landing-page.md) for more information.

## Activation and other requirements

**Important:** [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/agent-client-collector-rn.md), [Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/health-log-analytics-rn.md), and [Install ServiceNow Operations Workspace \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/install-sow-itom-apps.md) are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**
    -   ITOM Health is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM Health package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/c_EMConfiguration.md).
    -   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).
    -   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Accessibility and localization

-   **Accessibility information**
    -   **Support for reflow**

        The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

        This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/auto-reflow.md) for details.

-   **Localization information**

    The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


