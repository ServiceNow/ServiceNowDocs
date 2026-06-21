---
title: Combined Event Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Event Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-eventmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Event Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Event Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Event Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Event Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Australia, new features were introduced for Event Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Customize the default order of the alert correlation algorithm](https://www.servicenow.com/docs/access?context=Alert-Groups&family=xanadu&ft:locale=en-US)**

Configure the alert correlation algorithm sequence by customizing it according to your needs.

-   **[Create team-based alert management rules](https://www.servicenow.com/docs/access?context=alert-management-rule&family=xanadu&ft:locale=en-US)**

Assign alert management rules to specific assignment groups so that only those alerts that are assigned to the specified group are executed.

-   **[Create tag based alert clustering definitions by teams](https://www.servicenow.com/docs/access?context=alert-clustering-definitions&family=xanadu&ft:locale=en-US)**

Create tag clusters only for alerts that are assigned to an alert group by assigning tag-based alert clusters to specific groups.

-   **[Restrict alert groups across alert assignment groups](https://www.servicenow.com/docs/access?context=alert-filtering&family=xanadu&ft:locale=en-US)**

Improve the accuracy and relevance of the alert correlation by grouping alerts according to a diverse set of requirements.

-   **[Scale out for alert group creation](https://www.servicenow.com/docs/access?context=Alert-Groups&family=xanadu&ft:locale=en-US)**

Ensure efficiency when running a job during high-alert traffic by scaling out the alert grouping job.

-   **[View unified service map and the impact paths in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-impact-tree&family=xanadu&ft:locale=en-US)**

Explore the updated service map in the Service Operations Workspace, designed to focus on the path that was affected by an alert to help you quickly assess its impact on a service. The map displays all configuration items \(CIs\) for services with up to 60 CIs, regardless of alert status. For services with over 60 CIs that have alerts, it shows the path of the most severe, most recent alert. You can also investigate an even broader view of the service topology. Access the service map directly from Service Operations Workspace, or through the preview panel or an impacted service in Express List.

-   **[Perform bulk actions on alerts in Express List](https://www.servicenow.com/docs/access?context=acknowledge-alerts&family=xanadu&ft:locale=en-US)**

Perform an action on up to 1,000 alerts in the Active alerts list simultaneously.

-   **[Remove alerts from an alerts group in Express List](https://www.servicenow.com/docs/access?context=el-remove-alerts-from-group&family=xanadu&ft:locale=en-US)**

Remove secondary alerts from an alert group directly from the Express List pane or from the preview panel.

-   **[Hide closed alerts on the preview panel and in Link View in Express List](https://www.servicenow.com/docs/access?context=el-hide-closed-alerts&family=xanadu&ft:locale=en-US)**

View only the open alerts on the preview panel and in Link View in Express List by toggling to hide the closed alerts.

-   **[View data on impacted services on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-impacted-services-data&family=xanadu&ft:locale=en-US)**

View information about Impacted Services on the preview panel and in Link View in Express List and open the Service Map and Metric Explorer directly from the panel.

-   **[Create an incident with Now Assist in Express List](https://www.servicenow.com/docs/access?context=el-create-incident-now-assist&family=xanadu&ft:locale=en-US)**

Generate incidents from alerts in Express List with a summary created by genAI that includes details on configuration items and impacted services.

-   **[View data on configuration items on the preview panel in Express List](https://www.servicenow.com/docs/access?context=el-ci-data&family=xanadu&ft:locale=en-US)**

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

-   **[Speed up alert resolution with a Now Assist analysis of past related incidents](https://www.servicenow.com/docs/access?context=nai-past-incidents&family=xanadu&ft:locale=en-US)**

Enhance efficiency and reduce downtime with a Now Assist analysis of past incidents on the same or related CIs. Now Assist investigates historical data to identify past incidents related to the current alert and reports their frequency and criticality levels. It also provides a summary of effective strategies used to resolve them. In addition, Now Assist offers contact information for individuals or teams who have resolved similar incidents in the past and could assist when needed.

-   **[Generate an alert group description in Express List using Now Assist](https://www.servicenow.com/docs/access?context=alert-group-descr-generate-el&family=xanadu&ft:locale=en-US)**

Use Now Assist to generate a description of an alert group in Express List that encompasses all the alerts within the group. The generated description replaces the original description of the group.

-   **[Launch an alert analysis from the Now Assist panel](https://www.servicenow.com/docs/access?context=alert-analysis-now-assist-panel&family=xanadu&ft:locale=en-US)**

Analyze an alert from the Now Assist panel. The alert analysis displays directly in the Now Assist panel for convenient review.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Group alerts using network traffic-based grouping](https://www.servicenow.com/docs/access?context=network-traffic-correlation-grouping&family=yokohama&ft:locale=en-US)**

Group alerts efficiently with network traffic-based alert grouping, which uses discovered TCP connections with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them.

-   **[View links between alerts in network traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&family=yokohama&ft:locale=en-US)**

Once a network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.

-   **[New role for team level operators](https://www.servicenow.com/docs/access?context=r_InstalledWithEventManagement&family=yokohama&ft:locale=en-US)**

Enhance team-level control over alert management with the evt\_team\_operator role. This role enables operators to manage Event Management operations within their assigned team, including reading and writing alerts, making configuration changes,updating Alert Automation, and setting up new integrations in the Integrations Launchpad.

-   **[\[Placeholder link text to key esc-notify-alert-sow-itom\]](https://www.servicenow.com/docs/access?context=esc-notify-alert-sow-itom&family=yokohama&ft:locale=en-US)**

Starting in version 26.7.0, execute response subflows automatically, manually, or both for alerts that match specific conditions through the Run Other Response Actions option of Respond Automatic. This enhancement offers better control over automated responses with configurable execution limits and multiple response actions.

-   **[\[Placeholder link text to key enrich-alert-sow-itom\]](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=yokohama&ft:locale=en-US)**

Starting in version 26.7.0, link a CI to an alert for more accurate IT component mapping though the Improve Configuration Item \(CI identification option of Enrich Automation. This enhancement improves alert visibility, speeds up issue resolution, and ensures better correlation between alerts and infrastructure components.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Mixed alert grouping](https://www.servicenow.com/docs/access?context=alert-group-use-cases&family=zurich&ft:locale=en-US)**

Combine CMDB-based and tag-based alert grouping strategies into cohesive groups that reduce noise, enabling faster and more effective response.

-   **[AIOps 360 overview dashboard](https://www.servicenow.com/docs/access?context=aiops-360-overview-dashboard&family=zurich&ft:locale=en-US)**

Gain actionable insights with a 360-degree dashboard that showcases product value, tracks operational efficiency, and highlights automation impact. Monitor alert handling, service health, and AIOps outcomes to drive smarter, faster decisions across IT operations.

-   **[Mixed alert grouping in Service Operations Workspace](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&family=zurich&ft:locale=en-US)**

Choose how you want to group alerts from the **Criteria Type** field. Use the **Related CIs** option to combine CMDB-based and tag-based alert grouping.

-   **[Application services for impact calculation](https://www.servicenow.com/docs/access?context=c_EMImpactCalculation&family=zurich&ft:locale=en-US)**

Filter the application services to be considered in impact calculation for focused and accurate results.

-   **[Metric connector in Integrations Launchpad](https://www.servicenow.com/docs/access?context=configure-metric-pull-connector&family=zurich&ft:locale=en-US)**

Configure metric pull connectors to automate data retrieval and seamlessly integrate external metrics for efficient monitoring.

-   **[View links between alerts in new alert groups in Express List®](https://www.servicenow.com/docs/access?context=el-link-view&family=zurich&ft:locale=en-US).**

Starting in version 26.9.0, investigate alert group details and visualize connections through Link View in Express List®, now available for log analytics-based alert groups and mixed alert groups.

-   **[Anomaly information for log analytic based alerts and metric intelligence alerts in preview panel in Express List®.](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, review visualizations for anomaly information in log analytic-based alerts and metric intelligence alerts in the preview panel in Express List\[var.express-reg-tm\].

-   **[Configure new property for automatic resume of the live list updates following a pause, and conﬁgure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&family=zurich&ft:locale=en-US)**

Starting in version 26.9.0, admins gain the ability to conﬁgure the amount of time until the live list updates resume, after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®, such as the default time range.

-   **[Centralized management with the ITOM AIOps configuration center](https://www.servicenow.com/docs/access?context=itom-aiops-conf-center&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, the ITOM AIOps configuration center provides a centralized hub to manage AIOps settings, helping you integrate monitoring tools, optimize alerts, metrics, and logs, and manage services, dashboards, teams, and authorizations for improved visibility and operational efficiency.

-   **[Added Recommended category for AIOps 360 Overview dashboards](https://www.servicenow.com/docs/access?context=aiops-360-overview-dashboard&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, added a Recommended category to all officially released dashboards, such as the AIOps 360 Overview dashboard and the AIOps Value Realization dashboard. The category helps you easily identify and access ITOM-approved dashboards.

-   **[Add a delay for incident creation from alerts](https://www.servicenow.com/docs/access?context=esc-notify-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, you can add a delay in Respond Automation before incidents are created from alerts. This enables alerts to auto-close if resolved, and it helps to reduce unnecessary incident creation.

-   **[Added support for multiple subscriptions of AWS account](https://www.servicenow.com/docs/access?context=aws-events-transform-script&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, added support to enable multiple member accounts to forward CloudWatch/EventBridge events to a centralized account, where a single SNS topic delivers them to the ServiceNow Event Ingestion endpoint. This reduces manual setup from multiple configurations to one and cuts onboarding effort by up to 90%.

-   **[Configure Dynatrace metric connector from Integrations Launchpad](https://www.servicenow.com/docs/access?context=configure-dynatrace-metric-pull-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the Dynatrace metric connector from the Integrations Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence for visualization, enrichment, dynamic thresholds, and anomaly detection.

-   **[\[Placeholder link text to key configure-datadog-connector\]](https://www.servicenow.com/docs/access?context=configure-datadog-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.

-   **[\[Placeholder link text to key configure-kafka-metrics-connector\]](https://www.servicenow.com/docs/access?context=configure-kafka-metrics-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use the new Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.

-   **ITOM [\[Placeholder link text to key c\_EM\]](https://www.servicenow.com/docs/access?context=c_EM&family=zurich&ft:locale=en-US) guided setup**

Starting in 27.2.1, introduced ITOM Event Management guided setup, providing a sequence of tasks that help you install and get started with Event Management efficiently.

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

-   **[Unified alert grouping across Event Management and HLA](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&family=australia&ft:locale=en-US)**

Improve alert quality, reduce noise, and achieve higher compression to act faster on issues by grouping Health Log Analytics and Event Management alerts.

-   **[Explicit node-based control for CI binding](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=australia&ft:locale=en-US)**

Increase binding accuracy and reliability and improve alert-to-CI binding with explicit node-based control, configurable node-field usage, enhanced mapping logic, and backward-compatible updates.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Event Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Alert page performance enhancements](https://www.servicenow.com/docs/access?context=c_EMAlert&family=xanadu&ft:locale=en-US)**

Benefit from the enhanced load time of the alert forms and service dashboard.

-   **[Calculate impact during loop dependency](https://www.servicenow.com/docs/access?context=cross-business-service-impact&family=xanadu&ft:locale=en-US)**

Support for circular \(loop\) dependency between configuration items in the impact tree is enabled.

-   **[Automated alert groups perform tag-based alert clustering](https://www.servicenow.com/docs/access?context=c_SACorrelatedAlertGroups&family=xanadu&ft:locale=en-US)**

Tag-based alert group correlation is performed as part of automated alert groups.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Property name changes](https://www.servicenow.com/docs/access?context=enable-alert-grouping&family=yokohama&ft:locale=en-US)**

**Enable CMDB Correlation for Alert Aggregation \( CMDB groups\)** \(**sa\_analytics.agg.query\_cmdb\_correlation\_enabled**\) has been renamed **Enable CMDB correlation**.

**Enable alert aggregation for CI-based Automated groups** \(**sa\_analytics.specific\_patterns\_enabled**\) has been renamed **Enable ML based Automation correlation**.

**Enable alert aggregation for Text-based groups** \(**sa\_analytics.text\_based\_group\_enabled**\) has been renamed **Enable Text based correlation**.

**Use all CMDB relations for CMDB group correlation. This property impacts both CMDB group correlation and Alert Similarity on the Alert form** \(**evt\_mgmt.related\_cis\_get\_all\_relation\_types**\) has been renamed **Use all CMDB relations for CMDB group correlation**.

-   **[Pull connectors](https://www.servicenow.com/docs/access?context=t_EMConfigureConnectorInstance&family=yokohama&ft:locale=en-US)**

Simplifying the setup for Out-of-the-Box \(OOTB\) event rules that come with the pull connectors that have not yet been activated, deactivated, or modified, the Apply additional matching rules option is now enabled by default. If a rule has been previously applied, you must set this option manually.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Automated regex generation](https://www.servicenow.com/docs/access?context=esc-notify-alert-sow-itom&family=zurich&ft:locale=en-US)**

Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.

-   **[Support for OAuth authentication method in Kafka connector](https://www.servicenow.com/docs/access?context=configure-kafka-consumer-connector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, enabling you to securely connect and manage access without storing or sharing static credentials.

-   **[Support for SCOM 2025 version](https://www.servicenow.com/docs/access?context=t_EMConfigureSCOMConnector&family=zurich&ft:locale=en-US)**

Starting in version 2.17.1, you can now check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.

-   **[Group automation enhancements](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, group automation now supports grouping by impacted service instances and related log properties, with enhanced test automation details for better visibility. These updates enable more effective analysis of alert correlations and more accurate validation of grouping logic.

The updated Test Automation section provides detailed insights into alert groups, including total alerts, description, grouping category, node, and time, with support for sorting by grouping type.

-   **[Validate CI identification in Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&family=zurich&ft:locale=en-US)**

Starting in version 26.11.0, you can ensure CI attributes are present in the **Additional info** field of the alert for accurate matching and test CI identification on sample events.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Event Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Event Management Mobile application is no longer available.

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

Between your current release family and Australia, some Event Management features or functionality were deprecated.

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

The Service Management dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article [\(KB0867184\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) in the Now Support knowledge base.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Event Management connector: Deprecate unused V1 connector definitions during Event Management connector upgrades.
-   vRealize connector: Enhance the vRealize event connector by replacing the deprecated XML API with a JSON-based API, ensuring compatibility with future versions.
-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr><tr><td>

Australia

</td><td>

-   Alert Clustering Definitions \(ACD\) have been deprecated and fully replaced by Alert Automation in Service Operations Workspace. All existing configurations remain supported with full feature parity.
-   Service Management Dashboard is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Event Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Event Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Event Management we have noted them here.

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

Review details on accessibility information for Event Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Event Management we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Event Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Visualize the chain of events that caused an issue by viewing an alert group timeline in Express List.
-   Understand the connection between the alerts by using Alert Assist's AI-driven technical analysis on alert groups.
-   Use the enhanced service map for alert impact visualization in Service Operations Workspace and Express List.

-   Select all alerts in Express List to perform bulk actions.
-   Remove alerts from an alerts group in Express List.
-   Hide closed alerts in Express List.
-   View data on Impacted Services in the preview panel in Express List.
-   Create an incident with an AI-generated summary from alerts in Express List.
-   View data on configuration items \(CIs\) on the preview panel in Express List.
-   Optimize alert resolution with AI-driven investigation of past related incidents by Now Assist.
-   Generate an alert group description in Express List using Now Assist.
-   Launch an alert analysis from the Now Assist panel.

 See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Review network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times by focusing on critical connections and dependencies.
-   Starting in version 26.3.4, benefit from the new alert grouping based on network traffic correlations:
    -   Investigate network traffic-based alert groups by using Express List®.
    -   Review alert group analysis by Now Assist
    -   View connections between network traffic-based alerts in **Link View**.
-   Enable team-level operators to create and manage their own integrations, set up their own alert automations, and enhancing control over alert management for their teams by assigning the new team\_operator role.
-   Review relevant information in the Now Assist panel based on records selected in the Express List®.
-   Starting in version 2.15.1, you can configure metric connector instances for the [Nagios](https://www.servicenow.com/docs/access?context=configure-nagios-metrics-connector&family=yokohama&ft:locale=en-US), [SolarWinds](https://www.servicenow.com/docs/access?context=configure-solarwinds-connector&family=yokohama&ft:locale=en-US), and [Zabbix](https://www.servicenow.com/docs/access?context=configure-zabbix-metrics-connector&family=yokohama&ft:locale=en-US) monitoring tools to receive metrics directly from these monitoring tools. This enhancement provides the following benefits:
    -   Seamlessly integrate monitoring data from multiple sources into Metric Intelligence.
    -   Improve anomaly detection and alerting with real-time metric ingestion.

 See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Combine the strengths of CMDB-based and tag-based strategies to create mixed alert groups that reduce noise and reveal clearer, actionable insights.
-   Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.
-   Gain actionable insights with AIOps 360-degree overview dashboard to showcase product value.
-   Accelerate integration setup with seamless installation via the Unified Launchpad store app, guided support for creating integrations, and enhanced observability with the new Service Observability filter.

 See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&family=zurich&ft:locale=en-US) or [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Streamline Event Management setup with the new AI-guided Implementation Planner, helping admins configure ITOM AIOps faster and more accurately.
-   Enable smarter alert grouping based on CMDB service relationships, with thresholds and seed prerequisites to reduce noise and improve operational efficiency.
-   Enhance alert grouping by unifying Health Log Analytics and Event Management alerts, helping you reduce noise and act on alerts with greater confidence.
-   Support OpenTelemetry \(OTel\) metrics through the MID Server API to simplify metric ingestion and enhance anomaly detection capabilities.

 -   **[ServiceNow Store updates for Event Management and Service Operations Workspace](https://store.servicenow.com/store/apps?q=ITOM)**

Some apps are updated monthly or quarterly via the ServiceNow Store. For information about cumulative release notes and compatibility information, see the ServiceNow Store version details:

    -   [Event Management](https://store.servicenow.com/store/app/e1a9af221b246a50a85b16db234bcbcb#releaseNotes)
    -   [Integrations Launchpad](https://store.servicenow.com/store/app/a21ae3e21b246a50a85b16db234bcb4d#releaseNotes)
    -   [Express List](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)
    -   [Alert Automation](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)
    -   [Service Operations Workspace \(SOW\) for ITOM](https://store.servicenow.com/store/app/98e8672e1be06a50a85b16db234bcb52#releaseNotes)

 See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&family=australia&ft:locale=en-US) or [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

