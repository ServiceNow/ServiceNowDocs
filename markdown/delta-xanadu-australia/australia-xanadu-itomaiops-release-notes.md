---
title: Combined ITOM AIOps release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ITOM AIOps from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-itomaiops-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined ITOM AIOps release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ITOM AIOps from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM AIOps release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM AIOps to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ITOM AIOps.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Load the allow list only from the configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&family=xanadu&ft:locale=en-US)**

Enhance your security by loading the allow list from the configuration file and ignoring the allow-list parameters.

-   **[Configure the agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&family=xanadu&ft:locale=en-US)**

Configure the agent log level directly from the ServiceNow® instance without needing to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&family=xanadu&ft:locale=en-US)**

Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore. Adding a certificate to the truststore verifies that the certificate is authentic.

-   **[Use the new application Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&family=xanadu&ft:locale=en-US)**

Use the Service Reliability Management application to respond, collaborate, track, and self-remediate when working on alerts and incidents.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation. You can use the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Stream log data from the System Log table in Glide to the Health Log Analytics AI engine](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&family=xanadu&ft:locale=en-US)**

Use the Glide Syslog data input to stream log messages from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\).

**Note:** Only a single Glide Syslog data input can exist in the system. This data input doesn't run on a MID Server.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=xanadu&ft:locale=en-US)**

Map current alert fields values to specified new values through the **Change alert values** option, in the "If these conditions are met, don't add an alert in ServiceNow" section.

-   **[Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&family=xanadu&ft:locale=en-US)**

Track and optimize alert grouping efficiency through a new header displaying key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&family=xanadu&ft:locale=en-US)**

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&family=xanadu&ft:locale=en-US)**

Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents related to the current alert. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&family=xanadu&ft:locale=en-US)**

Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&family=xanadu&ft:locale=en-US)**

Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&family=yokohama&ft:locale=en-US)**

Fetch data consistently over time by using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side, you need minimal additional stakeholder involvement, enabling swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest pre-processed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&family=yokohama&ft:locale=en-US)**

Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input for streaming log messages to Health Log Analytics with a heavy forwarder.

-   **[Create Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&family=yokohama&ft:locale=en-US)**

View key details from the Test Automation section, including total alerts, alert groups, ungrouped alerts, and compression, to help track and optimize alert grouping efficiency. Simulate other group types, such as CMDB, ML, and text-based grouping. The simulation processes only alerts that match the condition filter.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&family=yokohama&ft:locale=en-US)**

Set up your log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. The Integrations Launchpad provides a unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://www.servicenow.com/docs/access?context=il-connector-hla-firehose&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.

-   **[View links between alerts in Network Traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&family=yokohama&ft:locale=en-US)**

Once network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.

-   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of additional information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.

-   **[Benefit from enhanced Log Analytics alert group and mixed alert group functionality in the Express List](https://www.servicenow.com/docs/access?context=el-link-view&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, identify connected Log Analytics alerts and mixed alert group correlations faster using the Link View functionality. Utilize enhanced Now Assist Alert Analysis with additional context for Log Analytics alerts.

-   **[View visualizations of anomaly information for Log Analytics-based alerts and metric intelligence alerts in Express List®](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, review anomaly charts for Log Analytics alerts and Metric Intelligence alerts in the preview panel in Express List®.

-   **[Configure automatic resume for live updates when the live alert list is paused, and configure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, enable admins to configure the amount of time until the active display resumes after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®.


-   **[Map log data to service instances and components for alerts in context](https://www.servicenow.com/docs/access?context=il-connector-hla-map-business-context&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://www.servicenow.com/docs/access?context=hla-data-input-log-export&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


-   **[Live updates functionality has been updated in the Service Operation Workspace Lists.](https://www.servicenow.com/docs/access?context=configure-alert-list-autofresh-settings&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, a new toggle switch allows users to enable or disable live updates. When the toggle is set to on, alerts are updated automatically. When the toggle is set to off, a badge displays the number of available updates until the page is refreshed manually. The setting is saved for future logins by the same user.

-   **[Explore the new Dependency view for an alert](https://www.servicenow.com/docs/access?context=dependency-maps&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, explore the new Dependency view for an alert. Access maps from the following locations:

    -   in the preview panel, in the Configuration item section for the CI topology
    -   in the Utilities panel of the alert record
    -   in the action drop-down menu
    -   in the Core UI alert form
-   **[Respond to multiple alerts in Express List](https://www.servicenow.com/docs/access?context=bulk-alert-response-express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, run response actions on multiple alerts at the same time in Express List.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ITOM AIOps features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Alert automation enhancements](https://www.servicenow.com/docs/access?context=sow-itom-alert-automation&family=xanadu&ft:locale=en-US)**

In Group automation, in the Simulation section, **Re-run test** has been renamed **Re-run simulation**.

The **Active** toggle switch has been replaced with a check box.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=xanadu&ft:locale=en-US)**

A new section, **And finally**, featured two radio buttons, **Run other enrich alert automations** and **Don't run other enrich alert automations**, which replace the previous **Continue running automations of this type** toggle switch. Although this section is new, the functionality is unchanged. Selecting **Run other enrich alert automations** continues running automations with the same filter conditions, while **Don't run other enrich alert automations** halts additional automations after execution except for those owned by other assignment groups.

-   **[Associate services to use in Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-add-service&family=xanadu&ft:locale=en-US)**

System admins can select any supported service and associate it to use in Service Reliability Management regardless of the owner or support group configurations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=yokohama&ft:locale=en-US)**

Introduced a new section **And finally** that contains two radio buttons that replace the previous **Continue running automations of this type** toggle switch.

    -   **Run other enrich alert automations** continues running automations with the same filter conditions.
    -   **Don't run other enrich alert automations** halts additional automations after execution, except those owned by other assignment groups.
-   **[Investigate alerts using Now Assist](https://www.servicenow.com/docs/access?context=nai-past-incidents&family=yokohama&ft:locale=en-US)**

Investigate alerts using Now Assist, which now uses the Retrieval-Augmented Generation \(RAG\) process to enhance alert investigation. This enhancement enables the retrieval of highly relevant past incidents, providing accurate context and actionable insights. Now Assist also notifies users of those involved in past or present efforts to resolve similar issues, promoting collaboration and reducing duplicated efforts.

-   **[Component-based alert grouping is deprecated](https://www.servicenow.com/docs/access?context=hla-op-log-analytics-alert-types&family=yokohama&ft:locale=en-US)**

Starting in version 36.0.19, component-based alert groups are removed as Health Log Analytics adopts a streamlined, two-tier alert model: Log Analytics Group to Single Alert. It aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ITOM AIOps features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ITOM AIOps features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The following dashboards have been deprecated:

-   Event Management scorecards
-   Event Management insights
-   Event Management overview
-   Health Log Analytics Overview

Service Management Dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM AIOps.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). To work with Health Log Analytics, you must purchase ITOM Predictive AIOps, a more comprehensive ITOM AIOps package. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=xanadu&ft:locale=en-US).

 Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=yokohama&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).
-   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=zurich&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. 
-   Install Health Log Analytics by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install ITOM AIOps apps by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=australia&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM AIOps we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ITOM AIOps we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ITOM AIOps, such as specific requirements or compliance levels.

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

-   **Support for reflow**

The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

-   **Support for reflow**

The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [\[Placeholder link text to key bundle-platux.auto-reflow\]](https://www.servicenow.com/docs/access?context=auto-reflow&family=zurich&ft:locale=en-US) for details.


 -   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ITOM AIOps we have noted them here.

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

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr><tr><td>

Zurich

</td><td>

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ITOM AIOps we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Agent Client Collector](https://www.servicenow.com/docs/access?context=agent-client-collector-rn&family=xanadu&ft:locale=en-US) highlights:

-   Configure the agent log level from the instance without needing to access the `acc.yml` configuration file.
-   Ensure secure agent connections by adding a self-signed certificate.
-   Gather expanded information on your Linux and Windows servers by using expanded Linux and Windows checks.

 [Health Log Analytics](https://www.servicenow.com/docs/access?context=health-log-analytics-rn&family=xanadu&ft:locale=en-US) highlights:

-   Enhance your system with the latest updates: Security fixes; Filebeat, Elasticsearch, and Microsoft Azure Event Hubs data input updates; Java JDK 17 update and support, and dependency upgrades.
-   Stream system logs from Glide to Health Log Analytics using the Glide Syslog data input.

 [Event Management release notes](https://www.servicenow.com/docs/access?context=event-management-rn&family=xanadu&ft:locale=en-US) highlights:

-   View configuration item \(CI\) information on the preview panel in Express List.
-   Optimize alert resolution with Now Assist AI-driven investigation of past related incidents.
-   Generate an alert group description in Express List using Now Assist.
-   Launch an alert analysis from the Now Assist panel.

</td></tr><tr><td>

Yokohama

</td><td>

Health Log Analytics highlights:

-   Pull data from Splunk consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk.
-   Use your Splunk data input to ingest data from Splunk in a pre-processed, structured format.
-   Integrate with log data connectors from the Integrations Launchpad
-   Use dedicated Cribl, Edge Delta and Vector Agent data inputs to streamline HLA data ingestion with tools handling large log volumes.
-   Generate a description of Health Log Analytics alerts using Now Assist.

 Event Management highlights:

 [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&family=yokohama&ft:locale=en-US)

-   Starting with version 26.3.1, benefit from the new alert grouping based on network traffic correlation:
    -   Use Express List® to investigate network traffic-based alert groups
    -   View connections between network traffic-based alerts in Link View.
    -   Starting with version 2.5.3, review alert group analysis by Now Assist
-   Review relevant information in the Now Assist panel based on records selected in Express List®.
-   Enable team-level operators to create and manage new alert automations by assigning the new team\_operator role.
-   Map current alert field values to new specified values through the new **Change alert values** option in the Enrich automation section.
-   Track and optimize grouping efficiency by viewing key details such as total alerts, alert groups, ungrouped alerts, and compression in Group Automation. Simulate other group types, such as CMDB, ML, and text-based grouping.

 Agent Client Collector highlights:

 See [ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

Health Log Analytics highlights:

-   Streamline Health Log Analytics data ingestion with Cribl by using the Cribl integration.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

 [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&family=zurich&ft:locale=en-US) highlights:

-   Control how alerts are grouped, which ones are included, and the order of grouping methods through Mixed Alert Grouping, which combines CMDB-based and tag-based strategies.
-   Starting in version 26.9.0, investigate mixed alert groups and Log Analytics-based alert groups by using Express List®.
-   Starting in version 26.9.0, view connections between alerts in Link View for mixed alert groups and Log Analytics-based alert groups.

 See [ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow Store updates for ITOM AIOps](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-ops-landing.html)**

The majority of ITOM AIOps apps are updated monthly or quarterly via the ServiceNow Store. The latest updates are available in the ServiceNow Store. For cumulative release notes and compatibility information, see the ServiceNow Store version details:

    -   [Service Reliability Management \(SRM\)](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-reliability-mgmt.html)
    -   [Service Level Objective Management](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-level-objective-mgmt-sow.html)
    -   [Service Observability](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-observability.html)
    -   [Event Management](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-event-management-core.html)
    -   [Health Log Analytics](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-health-log-analytics.html)
    -   [AIOps Dashboards](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-dashboards.html)
    -   [Agent Client Collector Log Analytics \(ACC-L\)](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-log-analytics.html)
    -   [Integrations Launchpad](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-ws-integrations-launchpad.html)
    -   [Express List](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-ws-express-list.html)
    -   [Metric Intelligence](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-metric-intelligence.html)
    -   Alert Automation
    -   [Learning Enhanced Automation Playbook \(LEAP\)](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-leap.html)
    -   [Service Operations Workspace \(SOW\) for ITOM](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-workspace-itom-apps.html)
    -   [Synthetic Monitoring](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-sow-synthetic-monitoring.html)

 See [ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

