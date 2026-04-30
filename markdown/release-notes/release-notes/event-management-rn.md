---
title: Event Management release notes
description: The ServiceNow Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Event Management release notes

The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management was enhanced and updated in the Zurich release.

## Event Management highlights for the Zurich release

-   Combine the strengths of CMDB-based and tag-based strategies to create mixed alert groups that reduce noise and reveal clearer, actionable insights.
-   Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.
-   Gain actionable insights with AIOps 360-degree overview dashboard to showcase product value.
-   Accelerate integration setup with seamless installation via the Unified Launchpad store app, guided support for creating integrations, and enhanced observability with the new Service Observability filter.

See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) or [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** Event Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Mixed alert grouping](https://www.servicenow.com/docs/access?context=alert-group-use-cases&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Combine CMDB-based and tag-based alert grouping strategies into cohesive groups that reduce noise, enabling faster and more effective response.

-   **[AIOps 360 overview dashboard](https://www.servicenow.com/docs/access?context=aiops-360-overview-dashboard&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Gain actionable insights with a 360-degree dashboard that showcases product value, tracks operational efficiency, and highlights automation impact. Monitor alert handling, service health, and AIOps outcomes to drive smarter, faster decisions across IT operations.

-   **[Mixed alert grouping in Service Operations Workspace](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Choose how you want to group alerts from the **Criteria Type** field. Use the **Related CIs** option to combine CMDB-based and tag-based alert grouping.

-   **[Application services for impact calculation](https://www.servicenow.com/docs/access?context=c_EMImpactCalculation&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Filter the application services to be considered in impact calculation for focused and accurate results.

-   **[Metric connector in Integrations Launchpad](https://www.servicenow.com/docs/access?context=configure-metric-pull-connector&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Configure metric pull connectors to automate data retrieval and seamlessly integrate external metrics for efficient monitoring.

-   **[View links between alerts in new alert groups in Express List®](https://www.servicenow.com/docs/access?context=el-link-view&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).**

    Starting in version 26.9.0, investigate alert group details and visualize connections through Link View in Express List®, now available for log analytics-based alert groups and mixed alert groups.

-   **[Anomaly information for log analytic based alerts and metric intelligence alerts in preview panel in Express List®.](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.9.0, review visualizations for anomaly information in log analytic-based alerts and metric intelligence alerts in the preview panel in Express List\[var.express-reg-tm\].

-   **[Configure new property for automatic resume of the live list updates following a pause, and conﬁgure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.9.0, admins gain the ability to conﬁgure the amount of time until the live list updates resume, after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®, such as the default time range.

-   **Centralized management with the ITOM AIOps configuration center**

    Starting in version 26.11.0, the ITOM AIOps configuration center provides a centralized hub to manage AIOps settings, helping you integrate monitoring tools, optimize alerts, metrics, and logs, and manage services, dashboards, teams, and authorizations for improved visibility and operational efficiency.

-   **Added Recommended category for AIOps 360 Overview dashboards**

    Starting in version 26.11.0, added a **Recommended** category to all officially released dashboards such as AIOps 360 Overview dashboard, AIOps Value Realization dashboard, to help you easily identify and access ITOM-approved dashboards.

-   **Add a delay for incident creation from alerts**

    Starting in version 26.11.0, you can add a delay in Respond Automation before incidents are created from alerts, allowing alerts to auto-close if resolved and helping reduce unnecessary incident creation.

-   **Added support for multiple subscriptions of AWS account**

    Starting in version 2.17.1, added support to enable multiple member accounts to forward CloudWatch/EventBridge events to a centralized account, where a single SNS topic delivers them to the ServiceNow Event Ingestion endpoint, reducing manual setup from multiple configurations to one and cutting onboarding effort by up to 90%.

-   **Configure Dynatrace metric connector from Integrations Launchpad**

    Starting in version 2.17.1, you can use the Dynatrace metric connector from the Integrations Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence for visualization, enrichment, dynamic thresholds, and anomaly detection.

-   ****

    Starting in version 2.17.1, you can use the out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.

-   ****

    Starting in version 2.17.1, you can use the new Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.

-   **ITOM  guided setup**

    Starting in 27.2.1, introduced ITOM Event Management guided setup, providing a sequence of tasks that help you install and get started with Event Management efficiently.

-   **[Live updates functionality has been updated in the Service Operation Workspace Lists.](https://www.servicenow.com/docs/access?context=configure-alert-list-autofresh-settings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.11.0, a new toggle switch allows users to enable or disable live updates. When the toggle is set to on, alerts are updated automatically. When the toggle is set to off, a badge displays the number of available updates until the page is refreshed manually. The setting is saved for future logins by the same user.

-   **[Explore the new Dependency view for an alert](https://www.servicenow.com/docs/access?context=dependency-maps&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.11.0, explore the new Dependency view for an alert. Access maps from the following locations:

    -   in the preview panel, in the Configuration item section for the CI topology
    -   in the Utilities panel of the alert record
    -   in the action drop-down menu
    -   in the Core UI alert form
-   **[Respond to multiple alerts in Express List](https://www.servicenow.com/docs/access?context=bulk-alert-response-express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.11.0, run response actions on multiple alerts at the same time in Express List.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Group automation](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Added the **Criteria Type** field, enabling you to choose how alerts are grouped.


## Changed in this release

-   **Automated regex generation**

    Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.

-   **Support for OAuth authentication method in Kafka connector**

    Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, allowing you to securely connect and manage access without storing or sharing static credentials.

-   **Support for SCOM 2025 version**

    Starting in version 2.17.1, you can now check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.

-   **Group automation enhancements**

    Starting in version 26.11.0, group automation now supports grouping by impacted service instances and related log properties, with enhanced test automation details for better visibility. These updates enable more effective analysis of alert correlations and more accurate validation of grouping logic.

    The updated Test Automation section provides detailed insights into alert groups, including total alerts, description, grouping category, node, and time, with support for sorting by grouping type.

-   **Validate CI identification in Enrich automation**

    Starting in version 26.11.0, you can ensure CI attributes are present in the **Additional info** field of the alert for accurate matching and test CI identification on sample events.


## Deprecations

-   Event Management connector: Deprecate unused V1 connector definitions during Event Management connector upgrades.
-   vRealize connector: Enhance the vRealize event connector by replacing the deprecated XML API with a JSON-based API, ensuring compatibility with future versions.
-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

## Activation information

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Metric Explorer](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    ServiceNow® Agent Workspace for [Metric Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) provides a central interface that enables you to view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds and aggregations for single score charts.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)

