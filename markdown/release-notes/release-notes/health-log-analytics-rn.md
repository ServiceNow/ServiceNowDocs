---
title: Health Log Analytics release notes
description: The ServiceNow Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [HLA release notes]
---

# Health Log Analytics release notes

The ServiceNow® Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Zurich release.

## Health Log Analytics highlights for the Zurich release

-   Use the Cribl integration to streamline Health Log Analytics data ingestion with Cribl.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** [Health Log Analytics](health-log-analytics-rn.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.


-   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 37.0.15, take advantage of extra information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.


-   **[Export source types to an update set by log source](https://www.servicenow.com/docs/access?context=hla-export-sourcetypes-by-source&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, export all source types related to one or more selected log sources to an update set together. You can then import the update set to the target environment.


-   **[Map log data to service instances and components for alerts in context](https://www.servicenow.com/docs/access?context=il-connector-hla-map-business-context&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Display Integrations Launchpad from the ITOM AIOps configuration center](https://www.servicenow.com/docs/access?context=itom-aiops-conf-center&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, open the Integrations Launchpad from ITOM AIOps configuration center. The ITOM AIOps configuration center is a centralized workspace that enables you to configure and manage AIOps features from a single place.


-   **[Set up a GCP PubSub integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-gcp-pubsub&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, set up an integration from the Integrations Launchpad for receiving log messages that were published to a Google Cloud Platform \(GCP\) Pub/Sub topic and streaming them to your ServiceNow instance.


-   **[Set up a Microsoft Azure Event Hubs integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-event-hubs&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, set up an integration from the Integrations Launchpad for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance.


-   **[Set up an Edge Delta TCP or REST integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-edgedelta-tcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, set up an integration from the Integrations Launchpad to enable Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance over the TCP transport protocol or via REST.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://www.servicenow.com/docs/access?context=hla-data-input-log-export&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The Event Management application uses events generated by Health Log Analytics. When Health Log Analytics detects an anomaly in your log data, it sends an event to Event Management. Event Management receives the event and generates an alert based on event and alert management rules.

-   **[Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Agent data inputs beginning in Health Log Analytics Version 21.0.1 - September 2021 use Agent Client Collector to stream logs to your ServiceNow instance.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Health Log Analytics uses the ServiceNow® MID Server product to stream logs to your ServiceNow instance.

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Health Log Analytics generates alerts in the ServiceNow Service Operations Workspace, a configurable workspace that provides a unified experience for multiple IT Operations Management workflows.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)

