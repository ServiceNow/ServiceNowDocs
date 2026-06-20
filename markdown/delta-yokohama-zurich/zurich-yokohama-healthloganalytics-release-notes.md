---
title: Combined Health Log Analytics release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Health Log Analytics from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-healthloganalytics-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Health Log Analytics release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Health Log Analytics from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Health Log Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Health Log Analytics to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Health Log Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-splunk-polling&family=yokohama&ft:locale=en-US)**

Make your data workflows more consistent and productive by fetching data consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side means you need minimal additional stakeholder involvement, which enables swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest preprocessed data from Splunk](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-splunk&family=yokohama&ft:locale=en-US)**

Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-setup-integrations&family=yokohama&ft:locale=en-US)**

Take advantage of the Integrations Launchpad's unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. You set up log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

-   **[Use Cribl and Edge Delta data inputs to streamline HLA data ingestion with tools handling large log volumes](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-setup-manual&family=yokohama&ft:locale=en-US)**

Use dedicated data inputs to facilitate data ingestion from Cribl or Edge Delta when using these tools to handle large volumes of log data from multiple sources before sending it to HLA.

-   **[Configure log data integrations from the Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-setup-integrations&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-firehose&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-cribl&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.


-   **[Leverage additional information available on the integration's Overview screen](https://servicenow-staging.fluidtopics.net/access?context=il-connector-overview-tab&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of extra information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.


-   **[Export source types to an update set by log source](https://servicenow-staging.fluidtopics.net/access?context=hla-export-sourcetypes-by-source&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, export all source types related to one or more selected log sources to an update set together. You can then import the update set to the target environment.


-   **[Map log data to service instances and components for alerts in context](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-map-business-context&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Display Integrations Launchpad from the ITOM AIOps configuration center](https://servicenow-staging.fluidtopics.net/access?context=itom-aiops-conf-center&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, open the Integrations Launchpad from ITOM AIOps configuration center. The ITOM AIOps configuration center is a centralized workspace that enables you to configure and manage AIOps features from a single place.


-   **[Set up a GCP PubSub integration from the Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-gcp-pubsub&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad for receiving log messages that were published to a Google Cloud Platform \(GCP\) Pub/Sub topic and streaming them to your ServiceNow instance.


-   **[Set up a Microsoft Azure Event Hubs integration from the Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-event-hubs&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance.


-   **[Set up an Edge Delta TCP or REST integration from the Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-edgedelta-tcp&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad to enable Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance over the TCP transport protocol or via REST.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-log-export&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Health Log Analytics features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Component-based alert grouping is deprecated](https://servicenow-staging.fluidtopics.net/access?context=hla-op-log-analytics-alert-types&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, the adoption of a streamlined two-tier alert model, Log Analytics Group to Single Alert, has replaced component-based alert groups, which have been removed. This model aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Health Log Analytics features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Health Log Analytics features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Health Log Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Health Log Analytics by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Health Log Analytics, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr><tr><td>

Zurich

</td><td>

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Use the enhanced Splunk data input to ingest data from Splunk in a preprocessed structured format. You can also pull data from Splunk regularly using the new Splunk Polling data input.
-   Take advantage of a unified interface for convenient data input integration by setting up integrations from the Integrations Launchpad.
-   Streamline HLA data ingestion with tools for handling large log volumes by using dedicated Cribl and Edge Delta data inputs.
-   Configure log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, REST API, and Amazon Data Firehose conveniently from the Integrations Launchpad.
-   Generate a description of Health Log Analytics alerts using Now Assist.

 See [Health Log Analytics](https://servicenow-staging.fluidtopics.net/access?context=hla-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use the Cribl integration to streamline Health Log Analytics data ingestion with Cribl.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

 See [Health Log Analytics](https://servicenow-staging.fluidtopics.net/access?context=hla-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

