---
title: Combined ITOM AIOps release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for ITOM AIOps from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-itomaiops-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined ITOM AIOps release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for ITOM AIOps from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM AIOps release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM AIOps to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ITOM AIOps.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

