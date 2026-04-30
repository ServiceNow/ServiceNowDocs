---
title: ITOM AIOps release notes
description: The ServiceNow ITOM AIOps product helps you to keep track and maintain the health of the services in your organization. ITOM AIOps was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# ITOM AIOps release notes

The ServiceNow® ITOM AIOps product helps you to keep track and maintain the health of the services in your organization. ITOM AIOps was enhanced and updated in the Yokohama release.

## ITOM AIOps highlights for the Yokohama release

Health Log Analytics highlights:

-   Pull data from Splunk consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk.
-   Use your Splunk data input to ingest data from Splunk in a pre-processed, structured format.
-   Integrate with log data connectors from the Integrations Launchpad
-   Use dedicated Cribl, Edge Delta and Vector Agent data inputs to streamline HLA data ingestion with tools handling large log volumes.
-   Generate a description of Health Log Analytics alerts using Now Assist.

Event Management highlights:

-   Focus on critical connections and dependencies by reviewing network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times.

[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

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

See [ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** [Agent Client Collector](agent-client-collector-rn.md), [Health Log Analytics](health-log-analytics-rn.md), and [Install ServiceNow Operations Workspace \(ITOM\)](https://www.servicenow.com/docs/access?context=install-sow-itom-apps&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Fetch data consistently over time by using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side, you need minimal additional stakeholder involvement, enabling swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest pre-processed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input for streaming log messages to Health Log Analytics with a heavy forwarder.

-   **[Create Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    View key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression, to help track and optimize alert grouping efficiency. Simulate other group types, such as CMDB, ML, and text-based grouping. The simulation processes only alerts that match the condition filter.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Set up your log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. The Integrations Launchpad provides a unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

    Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://www.servicenow.com/docs/access?context=il-connector-hla-firehose&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.

-   **[View links between alerts in Network Traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Once network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.


## UI changes

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The **Compose** action has been renamed **Copy or compose fields**.

-   **[Integrations Launchpad enhancements](https://www.servicenow.com/docs/access?context=review-integration-config-health&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The **Related events** tab has been renamed **Events**.

    The **Health state** tab has been renamed **Integration Stats**.

    The **Alert compression rate** section has been renamed **Grouping ratio**.

-   **[Respond automation](https://www.servicenow.com/docs/access?context=esc-notify-alert-sow-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The **Active** toggle switch has been replaced with a check box.

-   **[ServiceNow System Logs data input](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Glide Syslog data input has been renamed ServiceNow System Logs data input.


## Changed in this release

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Introduced a new section **And finally** that contains two radio buttons that replace the previous **Continue running automations of this type** toggle switch.

    -   **Run other enrich alert automations** continues running automations with the same filter conditions.
    -   **Don't run other enrich alert automations** halts additional automations after execution, except those owned by other assignment groups.
-   **[Investigate alerts using Now Assist](https://www.servicenow.com/docs/access?context=nai-past-incidents&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Investigate alerts using Now Assist, which now uses the Retrieval-Augmented Generation \(RAG\) process to enhance alert investigation. This enhancement enables the retrieval of highly relevant past incidents, providing accurate context and actionable insights. Now Assist also notifies users of those involved in past or present efforts to resolve similar issues, promoting collaboration and reducing duplicated efforts.

-   **[Component-based alert grouping is deprecated](https://www.servicenow.com/docs/access?context=hla-op-log-analytics-alert-types&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 36.0.19, component-based alert groups are removed as Health Log Analytics adopts a streamlined, two-tier alert model: Log Analytics Group to Single Alert. It aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


## Activation information

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).
-   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Support for reflow**

    The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for details.


## Localization information

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

## Related ServiceNow applications and features

-   **[ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The ITOM Visibility application consists of [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), Certificate Inventory and Management, Service Graph Connectors, CMDB 360, and Firewall Audits and Reporting. Discovery and Service Mapping provide a unified, connected view of your entire IT network and the services that it supports.

-   **[ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    ITOM Optimization contains the [Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) feature. By using this feature, you can provision a private and public cloud infrastructure and services to achieve consistent management and cost visibility.

-   **[Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Service Operations Workspace ITSM and ITOM are integrated to streamline incident and operations management. ITSM focuses on managing service incidents, requests, and changes, while ITOM is responsible for operational tasks like monitoring infrastructure, handling alerts, and maintaining system health. Together, they provide a unified workspace that enables seamless collaboration between service management and operations teams, improving efficiency in resolving issues and maintaining service performance.


