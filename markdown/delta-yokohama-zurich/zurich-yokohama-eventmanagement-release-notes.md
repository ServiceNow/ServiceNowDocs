---
title: Combined Event Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Event Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-eventmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Event Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Event Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Event Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Event Management to Zurich

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

Between your current release family and Zurich, new features were introduced for Event Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Group alerts using network traffic-based grouping](https://servicenow-staging.fluidtopics.net/access?context=network-traffic-correlation-grouping&family=yokohama&ft:locale=en-US)**

Group alerts efficiently with network traffic-based alert grouping, which uses discovered TCP connections with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them.

-   **[View links between alerts in network traffic-based alert groups](https://servicenow-staging.fluidtopics.net/access?context=el-network-traffic-based-link-view&family=yokohama&ft:locale=en-US)**

Once a network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.

-   **[New role for team level operators](https://servicenow-staging.fluidtopics.net/access?context=r_InstalledWithEventManagement&family=yokohama&ft:locale=en-US)**

Enhance team-level control over alert management with the evt\_team\_operator role. This role enables operators to manage Event Management operations within their assigned team, including reading and writing alerts, making configuration changes,updating Alert Automation, and setting up new integrations in the Integrations Launchpad.

-   **[\[Placeholder link text to key esc-notify-alert-sow-itom\]](https://servicenow-staging.fluidtopics.net/access?context=esc-notify-alert-sow-itom&family=yokohama&ft:locale=en-US)**

Starting in version 26.7.0, execute response subflows automatically, manually, or both for alerts that match specific conditions through the Run Other Response Actions option of Respond Automatic. This enhancement offers better control over automated responses with configurable execution limits and multiple response actions.

-   **[\[Placeholder link text to key enrich-alert-sow-itom\]](https://servicenow-staging.fluidtopics.net/access?context=enrich-alert-sow-itom&family=yokohama&ft:locale=en-US)**

Starting in version 26.7.0, link a CI to an alert for more accurate IT component mapping though the Improve Configuration Item \(CI identification option of Enrich Automation. This enhancement improves alert visibility, speeds up issue resolution, and ensures better correlation between alerts and infrastructure components.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Mixed alert grouping](https://servicenow-staging.fluidtopics.net/access?context=alert-group-use-cases&family=zurich&ft:locale=en-US)**

Combine CMDB-based and tag-based alert grouping strategies into cohesive groups that reduce noise, enabling faster and more effective response.

-   **[AIOps 360 overview dashboard](https://servicenow-staging.fluidtopics.net/access?context=aiops-360-overview-dashboard&family=zurich&ft:locale=en-US)**

Gain actionable insights with a 360-degree dashboard that showcases product value, tracks operational efficiency, and highlights automation impact. Monitor alert handling, service health, and AIOps outcomes to drive smarter, faster decisions across IT operations.

-   **[Mixed alert grouping in Service Operations Workspace](https://servicenow-staging.fluidtopics.net/access?context=group-alert-sow-itom&family=zurich&ft:locale=en-US)**

Choose how you want to group alerts from the **Criteria Type** field. Use the **Related CIs** option to combine CMDB-based and tag-based alert grouping.

-   **[Application services for impact calculation](https://servicenow-staging.fluidtopics.net/access?context=c_EMImpactCalculation&family=zurich&ft:locale=en-US)**

Filter the application services to be considered in impact calculation for focused and accurate results.

-   **[Metric connector in Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=configure-metric-pull-connector&family=zurich&ft:locale=en-US)**

Configure metric pull connectors to automate data retrieval and seamlessly integrate external metrics for efficient monitoring.

-   **[View links between alerts in new alert groups in Express List®](https://servicenow-staging.fluidtopics.net/access?context=el-link-view&family=zurich&ft:locale=en-US).**

Starting in version 26.9.0, investigate alert group details and visualize connections through Link View in Express List®, now available for log analytics-based alert groups and mixed alert groups.

-   **[Anomaly information for log analytic based alerts and metric intelligence alerts in preview panel in Express List®.](https://servicenow-staging.fluidtopics.net/access?context=view-anomaly-alert-display&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, review visualizations for anomaly information in log analytic-based alerts and metric intelligence alerts in the preview panel in Express List\[var.express-reg-tm\].

-   **[Configure new property for automatic resume of the live list updates following a pause, and conﬁgure time ranges in Express List®](https://servicenow-staging.fluidtopics.net/access?context=express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, admins gain the ability to conﬁgure the amount of time until the live list updates resume, after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®, such as the default time range.

-   **[Centralized management with the ITOM AIOps configuration center](https://servicenow-staging.fluidtopics.net/access?context=itom-aiops-conf-center&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, the ITOM AIOps configuration center provides a centralized hub to manage AIOps settings, helping you integrate monitoring tools, optimize alerts, metrics, and logs, and manage services, dashboards, teams, and authorizations for improved visibility and operational efficiency.

-   **[Added Recommended category for AIOps 360 Overview dashboards](https://servicenow-staging.fluidtopics.net/access?context=aiops-360-overview-dashboard&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, added a **Recommended** category to all officially released dashboards such as AIOps 360 Overview dashboard, AIOps Value Realization dashboard, to help you easily identify and access ITOM-approved dashboards.

-   **[Add a delay for incident creation from alerts](https://servicenow-staging.fluidtopics.net/access?context=esc-notify-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, you can add a delay in Respond Automation before incidents are created from alerts, allowing alerts to auto-close if resolved and helping reduce unnecessary incident creation.

-   **[Added support for multiple subscriptions of AWS account](https://servicenow-staging.fluidtopics.net/access?context=aws-events-transform-script&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, added support to enable multiple member accounts to forward CloudWatch/EventBridge events to a centralized account, where a single SNS topic delivers them to the ServiceNow Event Ingestion endpoint, reducing manual setup from multiple configurations to one and cutting onboarding effort by up to 90%.

-   **[Configure Dynatrace metric connector from Integrations Launchpad](https://servicenow-staging.fluidtopics.net/access?context=configure-dynatrace-metric-pull-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the Dynatrace metric connector from the Integrations Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence for visualization, enrichment, dynamic thresholds, and anomaly detection.

-   **[\[Placeholder link text to key configure-datadog-connector\]](https://servicenow-staging.fluidtopics.net/access?context=configure-datadog-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.

-   **[\[Placeholder link text to key configure-kafka-metrics-connector\]](https://servicenow-staging.fluidtopics.net/access?context=configure-kafka-metrics-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the new Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.

-   **ITOM [\[Placeholder link text to key c\_EM\]](https://servicenow-staging.fluidtopics.net/access?context=c_EM&family=zurich&ft:locale=en-US) guided setup**

Starting in 27.2.1, introduced ITOM Event Management guided setup, providing a sequence of tasks that help you install and get started with Event Management efficiently.

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

Between your current release family and Zurich, some changes were made to existing Event Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Property name changes](https://servicenow-staging.fluidtopics.net/access?context=enable-alert-grouping&family=yokohama&ft:locale=en-US)**

**Enable CMDB Correlation for Alert Aggregation \( CMDB groups\)** \(**sa\_analytics.agg.query\_cmdb\_correlation\_enabled**\) has been renamed **Enable CMDB correlation**.

**Enable alert aggregation for CI-based Automated groups** \(**sa\_analytics.specific\_patterns\_enabled**\) has been renamed **Enable ML based Automation correlation**.

**Enable alert aggregation for Text-based groups** \(**sa\_analytics.text\_based\_group\_enabled**\) has been renamed **Enable Text based correlation**.

**Use all CMDB relations for CMDB group correlation. This property impacts both CMDB group correlation and Alert Similarity on the Alert form** \(**evt\_mgmt.related\_cis\_get\_all\_relation\_types**\) has been renamed **Use all CMDB relations for CMDB group correlation**.

-   **[Pull connectors](https://servicenow-staging.fluidtopics.net/access?context=t_EMConfigureConnectorInstance&family=yokohama&ft:locale=en-US)**

Simplifying the setup for Out-of-the-Box \(OOTB\) event rules that come with the pull connectors that have not yet been activated, deactivated, or modified, the Apply additional matching rules option is now enabled by default. If a rule has been previously applied, you must set this option manually.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Automated regex generation](https://servicenow-staging.fluidtopics.net/access?context=esc-notify-alert-sow-itom&family=zurich&ft:locale=en-US)**

Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.

-   **[Support for OAuth authentication method in Kafka connector](https://servicenow-staging.fluidtopics.net/access?context=configure-kafka-consumer-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, allowing you to securely connect and manage access without storing or sharing static credentials.

-   **[Support for SCOM 2025 version](https://servicenow-staging.fluidtopics.net/access?context=t_EMConfigureSCOMConnector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can now check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.

-   **[Group automation enhancements](https://servicenow-staging.fluidtopics.net/access?context=group-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, group automation now supports grouping by impacted service instances and related log properties, with enhanced test automation details for better visibility. These updates enable more effective analysis of alert correlations and more accurate validation of grouping logic.

The updated Test Automation section provides detailed insights into alert groups, including total alerts, description, grouping category, node, and time, with support for sorting by grouping type.

-   **[Validate CI identification in Enrich automation](https://servicenow-staging.fluidtopics.net/access?context=enrich-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, you can ensure CI attributes are present in the **Additional info** field of the alert for accurate matching and test CI identification on sample events.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Event Management features or functionality were removed.

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

Between your current release family and Zurich, some Event Management features or functionality were deprecated.

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

-   Event Management connector: Deprecate unused V1 connector definitions during Event Management connector upgrades.
-   vRealize connector: Enhance the vRealize event connector by replacing the deprecated XML API with a JSON-based API, ensuring compatibility with future versions.
-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Event Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://servicenow-staging.fluidtopics.net/access?context=t_EMActivatePlugin&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://servicenow-staging.fluidtopics.net/access?context=t_EMActivatePlugin&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Event Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Event Management we have noted them here.

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

Review details on accessibility information for Event Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Event Management we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Event Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Review network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times by focusing on critical connections and dependencies.
-   Starting in version 26.3.4, benefit from the new alert grouping based on network traffic correlations:
    -   Investigate network traffic-based alert groups by using Express List®.
    -   Review alert group analysis by Now Assist
    -   View connections between network traffic-based alerts in **Link View**.
-   Enable team-level operators to create and manage their own integrations, set up their own alert automations, and enhancing control over alert management for their teams by assigning the new team\_operator role.
-   Review relevant information in the Now Assist panel based on records selected in the Express List®.
-   Starting in version 2.15.1, you can configure metric connector instances for the [Nagios](https://servicenow-staging.fluidtopics.net/access?context=configure-nagios-metrics-connector&family=yokohama&ft:locale=en-US), [SolarWinds](https://servicenow-staging.fluidtopics.net/access?context=configure-solarwinds-connector&family=yokohama&ft:locale=en-US), and [Zabbix](https://servicenow-staging.fluidtopics.net/access?context=configure-zabbix-metrics-connector&family=yokohama&ft:locale=en-US) monitoring tools to receive metrics directly from these monitoring tools. This enhancement provides the following benefits:
    -   Seamlessly integrate monitoring data from multiple sources into Metric Intelligence.
    -   Improve anomaly detection and alerting with real-time metric ingestion.

 See [Event Management](https://servicenow-staging.fluidtopics.net/access?context=c_EM&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Combine the strengths of CMDB-based and tag-based strategies to create mixed alert groups that reduce noise and reveal clearer, actionable insights.
-   Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.
-   Gain actionable insights with AIOps 360-degree overview dashboard to showcase product value.
-   Accelerate integration setup with seamless installation via the Unified Launchpad store app, guided support for creating integrations, and enhanced observability with the new Service Observability filter.

 See [Event Management](https://servicenow-staging.fluidtopics.net/access?context=c_EM&family=zurich&ft:locale=en-US) or [Service Operations Workspace for ITOM](https://servicenow-staging.fluidtopics.net/access?context=sow-landing-page-itom&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

