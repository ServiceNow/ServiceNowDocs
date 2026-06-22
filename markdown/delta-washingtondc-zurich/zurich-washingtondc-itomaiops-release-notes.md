---
title: Combined ITOM AIOps release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for ITOM AIOps from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-itomaiops-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined ITOM AIOps release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for ITOM AIOps from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM AIOps release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM AIOps to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ITOM AIOps.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Address alerts more effectively with alert simplifications created by Now Assist using generative AI](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itom-use&family=washingtondc&ft:locale=en-US)**

Use alert simplifications in Service Operations Workspace and Express List to help triage and investigate alerts more effectively, which can lead to reduced resolution time.

-   **[Save time by using preconfigured alert clustering tags and definitions](https://servicenow-staging.fluidtopics.net/access?context=alert-clustering-tag-definitions-concept&family=washingtondc&ft:locale=en-US)**

Get started faster with alert clustering in Event Management by using predefined tags mapped from alerts and based on the information contained in tag sources. You can attach one or more tags to an alert clustering definition. Either create your own definition or select a predefined definition provided with the application.

-   **[Create a predefined Express List view for users and user groups](https://servicenow-staging.fluidtopics.net/access?context=manage-views-express-list&family=washingtondc&ft:locale=en-US)**

Configure an Express List view for users to make sure that they focus on specific services, priorities, or alerts. You can set the filters, column order, and filter attributes for this view in Event Management and assign it to individual users or user groups.

-   **[Enhanced system properties](https://servicenow-staging.fluidtopics.net/access?context=acc-policy-collection-properties&family=washingtondc&ft:locale=en-US)**

Monitor the behavior of the Agent Client Collector with enhanced Policy Calculation and Framework Configuration system properties, including enhancements to agent Discovery, automatic MID Server selection, and error message logging.

-   **[Configuration data files added to checks](https://servicenow-staging.fluidtopics.net/access?context=acc-config-data-files&family=washingtondc&ft:locale=en-US)**

Provide enhanced data collection in the Agent Client Collector by communicating the instance data with the agent. The configuration data files are also sent to the agent’s associated MID Server.

-   **[Continuously discovering resources in your Kubernetes clusters](https://servicenow-staging.fluidtopics.net/access?context=cnov-exploring&family=washingtondc&ft:locale=en-US)**

Continuously discover the resources in the Kubernetes clusters deployed in on-premises and cloud environments in near real-time without the need to enter any credentials in your ServiceNow instance. You can ensure that the changes in the resources are promptly reported to the instance and updated in the Configuration Management Database \(CMDB\).

-   **[Scaling Health Log Analytics to support increased log ingestion](https://servicenow-staging.fluidtopics.net/access?context=hla-scale-request&family=washingtondc&ft:locale=en-US)**

Stream log data in a scalable, more stable way by using the advanced ServiceNow infrastructure. The Health Log Analytics AI engine has been enhanced to scale dynamically in response to increased log ingestion by your organization.


</td></tr><tr><td>

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

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-cribl&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.

-   **[Leverage additional information available on the integration's Overview screen](https://servicenow-staging.fluidtopics.net/access?context=il-connector-overview-tab&family=zurich&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of additional information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.

-   **[Benefit from enhanced Log Analytics alert group and mixed alert group functionality in the Express List](https://servicenow-staging.fluidtopics.net/access?context=el-link-view&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, identify connected Log Analytics alerts and mixed alert group correlations faster using the Link View functionality. Utilize enhanced Now Assist Alert Analysis with additional context for Log Analytics alerts.

-   **[View visualizations of anomaly information for Log Analytics-based alerts and metric intelligence alerts in Express List®](https://servicenow-staging.fluidtopics.net/access?context=view-anomaly-alert-display&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, review anomaly charts for Log Analytics alerts and Metric Intelligence alerts in the preview panel in Express List®.

-   **[Configure automatic resume for live updates when the live alert list is paused, and configure time ranges in Express List®](https://servicenow-staging.fluidtopics.net/access?context=express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, enable admins to configure the amount of time until the active display resumes after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®.


-   **[Map log data to service instances and components for alerts in context](https://servicenow-staging.fluidtopics.net/access?context=il-connector-hla-map-business-context&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://servicenow-staging.fluidtopics.net/access?context=hla-data-input-log-export&family=zurich&ft:locale=en-US)**

Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


-   **[Live updates functionality has been updated in the Service Operation Workspace Lists.](https://servicenow-staging.fluidtopics.net/access?context=configure-alert-list-autofresh-settings&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, a new toggle switch allows users to enable or disable live updates. When the toggle is set to on, alerts are updated automatically. When the toggle is set to off, a badge displays the number of available updates until the page is refreshed manually. The setting is saved for future logins by the same user.

-   **[Explore the new Dependency view for an alert](https://servicenow-staging.fluidtopics.net/access?context=dependency-maps&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, explore the new Dependency view for an alert. Access maps from the following locations:

    -   in the preview panel, in the Configuration item section for the CI topology
    -   in the Utilities panel of the alert record
    -   in the action drop-down menu
    -   in the Core UI alert form
-   **[Respond to multiple alerts in Express List](https://servicenow-staging.fluidtopics.net/access?context=bulk-alert-response-express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, run response actions on multiple alerts at the same time in Express List.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing ITOM AIOps features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Retrieve metrics for cloud resources](https://servicenow-staging.fluidtopics.net/access?context=azure-checks-policies&family=washingtondc&ft:locale=en-US)**

Use Azure policies to retrieve high-performance metrics for virtual resources in the cloud.

-   **[Automatic MID Server selection](https://servicenow-staging.fluidtopics.net/access?context=acc-auto-mid-selection&family=washingtondc&ft:locale=en-US)**
    -   Receive additional MID Server information to be used as alternative points of communication during automatic MID Server selection.
    -   Automatic MID Server selection is off by default.
-   **[ITOM Licensing](https://servicenow-staging.fluidtopics.net/access?context=itom-su-licensing-landing-page&family=washingtondc&ft:locale=en-US)**

ITOM SU Licensing has been rebranded as ITOM/OT SU Licensing. ITOM/OT SU Licensing calculates and displays the usage of ITOM subscriptions based on subscription units. It enables you to access a comprehensive overview of the total number of licenses allocated to applications and configuration items \(CIs\), while offering an advanced feature set that provides visibility into the specific CIs covered by your licenses. You can view the subscription breakdown for ITOM AIOps, ITOM Visibility, ITOM Optimization, and ITOM Cloud Accelerate. For more details, see [View which CIs have an ITOM license](https://servicenow-staging.fluidtopics.net/access?context=itom-licensing-count&family=washingtondc&ft:locale=en-US).


</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some ITOM AIOps features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some ITOM AIOps features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM AIOps.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://servicenow-staging.fluidtopics.net/access?context=c_EMConfiguration&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

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

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://servicenow-staging.fluidtopics.net/access?context=c_EMConfiguration&family=zurich&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. 
-   Install Health Log Analytics by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM AIOps we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ITOM AIOps we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ITOM AIOps, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **Support for reflow**

The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [\[Placeholder link text to key bundle-platux.auto-reflow\]](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=zurich&ft:locale=en-US) for details.


 -   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ITOM AIOps we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ITOM AIOps we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

[Event Management](https://servicenow-staging.fluidtopics.net/access?context=event-management-rn&family=washingtondc&ft:locale=en-US) highlights:

-   Investigate alerts more effectively in Service Operations Workspace and Express List with alert simplifications created by Now Assist using generative AI. Utilize brief alert descriptions and actionable alert data to enable quick alert triaging and effective analysis, which can lead to reduced resolution time.
-   Get started faster with alert clustering in Event Management by using predefined tags mapped from alerts and based on information contained in tag sources.
-   Configure an Express List view and assign it to users and user groups to ensure that they focus on specific services, priorities, or alerts.
-   Streamline the triage process and perform more effective root cause analysis by viewing data on repeated alerts, similar alerts, and incidents over the last 30 days in the Express List Alert Preview pane. These alert trends enable you to gain a deeper understanding of alert patterns and distinguish between noise and emerging issues.
-   Ensure that the connector's ownership and execution of rules is on a team level. This way, you can maintain consistency and hierarchy while offering flexibility and customization options for your teams.
-   Shorten your testing cycle by creating a stream of events from your production environment to your non-production environment where you can enable direct testing and evaluation of event rules, event field mappings, alert management rules, and alert correlation, without having to change your production environment.

 [Agent Client Collector](https://servicenow-staging.fluidtopics.net/access?context=agent-client-collector-rn&family=washingtondc&ft:locale=en-US) highlights:

-   Use your configuration data files to provide the instance data directly to an agent.
-   Continuously discover the resources in the Kubernetes clusters and ensure that changes in the resources are updated in the Configuration Management Database \(CMDB\).

 [Health Log Analytics](https://servicenow-staging.fluidtopics.net/access?context=health-log-analytics-rn&family=washingtondc&ft:locale=en-US) highlights:

-   Request Health Log Analytics scaling through the Now Support catalog.
-   Stream logs in a scalable, more stable way with Health Log Analytics by using the new ServiceNow infrastructure.

</td></tr><tr><td>

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

Health Log Analytics highlights:

-   Streamline Health Log Analytics data ingestion with Cribl by using the Cribl integration.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

 [Service Operations Workspace for ITOM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page-itom&family=zurich&ft:locale=en-US) highlights:

-   Control how alerts are grouped, which ones are included, and the order of grouping methods through Mixed Alert Grouping, which combines CMDB-based and tag-based strategies.
-   Starting in version 26.9.0, investigate mixed alert groups and Log Analytics-based alert groups by using Express List®.
-   Starting in version 26.9.0, view connections between alerts in Link View for mixed alert groups and Log Analytics-based alert groups.

 See [ITOM Health](https://servicenow-staging.fluidtopics.net/access?context=itom-health-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

