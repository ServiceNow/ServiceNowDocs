---
title: Combined Health Log Analytics release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Health Log Analytics from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-healthloganalytics-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Health Log Analytics release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Health Log Analytics from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Health Log Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Health Log Analytics to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Health Log Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Enjoy a significantly faster log streaming rate with the Lighting gRPC client for MID Server communication with the ServiceNow instance](https://www.servicenow.com/docs/access?context=hla-configuration-preferences&family=xanadu&ft:locale=en-US)**

Increase log streaming speeds to Health Log Analytics by up to six times through the Lightning gRPC client, which enhances MID Server communication with your ServiceNow instance. Note that the Lightning gRPC client requires manual configuration to activate.

-   **[Stream system logs from Glide to Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&family=xanadu&ft:locale=en-US)**

Use the Glide Syslog data input to stream log messages from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\).

**Note:** Only a single Glide Syslog data input can exist in the system. This data input doesn't run on a MID Server.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&family=yokohama&ft:locale=en-US)**

Make your data workflows more consistent and productive by fetching data consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side means you need minimal additional stakeholder involvement, which enables swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest preprocessed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&family=yokohama&ft:locale=en-US)**

Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.


 -   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of extra information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Sustained Alert feedback](https://www.servicenow.com/docs/access?context=hla-sustained-alert-apply&family=brazil&ft:locale=en-US)**

Suppress alerts on short-lived anomaly spikes and receive notifications only when an issue persists continuously. Apply Sustained Alert feedback per metric from the Alert Card or Express List \(single or bulk\), setting a fixed duration threshold to define what counts as sustained.

-   **[Smart Parser Gen AI enhancements](https://www.servicenow.com/docs/access?context=hla-source-type-structure-adjustment&family=brazil&ft:locale=en-US)**

Increase confidence in Smart Parser Gen AI alerts by viewing the full parsing and alert generation flow, now backed by expanded automated testing.

-   **[MID-less integration setup through an MCP Client](https://www.servicenow.com/docs/access?context=hla-mid-less-integrations-concept&family=brazil&ft:locale=en-US)**

Admins with access to the ITOM MCP Server Console can use an AI-enabled MCP Client to set up MID-less integrations. You can use any MCP Client, such as AWS Claude, to create MID-less integrations through natural-language prompts, without navigating to the Integrations Launchpad.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Health Log Analytics features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Component-based alert grouping is deprecated](https://www.servicenow.com/docs/access?context=hla-op-log-analytics-alert-types&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, the adoption of a streamlined two-tier alert model, Log Analytics Group to Single Alert, has replaced component-based alert groups, which have been removed. This model aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **ServiceNow Otto®**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Health Log Analytics. Your product entitlements remain unchanged. Check your entitlements to determine whether you have access to specific features.

-   **Health Log Analytics migration to LogDB for log storage**

Health Log Analytics stores short-term troubleshooting logs in LogDB instead of Elasticsearch for significantly better compression and faster ingestion. No action is required from your organization. Alerts generated before the transition still appear, but their surrounding logs aren't available because existing log data remains in Elasticsearch. New logs generated after the switch populate normally. If you notice anything unexpected, contact ServiceNow support.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Health Log Analytics features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Health Log Analytics features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Localization information**

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


</td></tr><tr><td>

Zurich

</td><td>

-   **Localization information**

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Localization information**

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Health Log Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Enjoy a significantly faster log streaming rate with the Lighting gRPC client for MID Server communication with the ServiceNow instance.
-   Stream system logs from Glide to Health Log Analytics.

 See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use the enhanced Splunk data input to ingest data from Splunk in a preprocessed structured format. You can also pull data from Splunk regularly using the new Splunk Polling data input.
-   Take advantage of a unified interface for convenient data input integration by setting up integrations from the Integrations Launchpad.
-   Streamline HLA data ingestion with tools for handling large log volumes by using dedicated Cribl and Edge Delta data inputs.
-   Configure log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, REST API, and Amazon Data Firehose conveniently from the Integrations Launchpad.
-   Generate a description of Health Log Analytics alerts using Now Assist.

 See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use the Cribl integration to streamline Health Log Analytics data ingestion with Cribl.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

 See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   Stay ahead of issues with predictive alerts based on anomaly detection.
-   Detect anomalous behavior automatically with log analytics alert rules.
-   Reduce mean time to resolution by accelerating root cause analysis with contextual log data.
-   Simplify log ingestion by processing high-volume log data at scale.
-   Uncover patterns in log data using built-in AI and ML.

 See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

