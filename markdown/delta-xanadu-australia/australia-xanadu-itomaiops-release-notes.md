---
title: Combined ITOM AIOps release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ITOM AIOps from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-itomaiops-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 13
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

No updates for this release.

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

-   **Activation information**
    -   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=yokohama&ft:locale=en-US).
    -   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).
    -   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**
    -   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&family=zurich&ft:locale=en-US).
    -   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).
    -   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

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

-   **Accessibility information**
    -   **Support for reflow**

The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Support for reflow**

The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [\[Placeholder link text to key bundle-platux.auto-reflow\]](https://www.servicenow.com/docs/access?context=auto-reflow&family=zurich&ft:locale=en-US) for details.

    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

 -   Focus on critical connections and dependencies by reviewing network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times.

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

 -   Create tasks to address Agent Client Collector errors.
-   Discover java installation information using file-based discovery.
-   Upgrade many agents at once using high-volume upgrade of Agent Client Collector.
-   Conserve the MID Server resources for more persistent features by using MID-less installation.

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
    -   [Service Operations Workspace \(SOW\) for ITOM](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-ops-workspace-itom-apps.html)
    -   [Synthetic Monitoring](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-sow-synthetic-monitoring.html)

 See [ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

