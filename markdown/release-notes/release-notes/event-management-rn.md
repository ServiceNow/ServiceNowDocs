---
title: Event Management release notes
description: The ServiceNow Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management provides alert aggregation for discovered services, application services, and automated alert groups. Event Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Event Management release notes

The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management provides alert aggregation for discovered services, application services, and automated alert groups. Event Management was enhanced and updated in the Yokohama release.

## Event Management highlights for the Yokohama release

-   Review network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times by focusing on critical connections and dependencies.
-   Starting in version 26.3.4, benefit from the new alert grouping based on network traffic correlations:
    -   Investigate network traffic-based alert groups by using Express List®.
    -   Review alert group analysis by Now Assist
    -   View connections between network traffic-based alerts in **Link View**.
-   Enable team-level operators to create and manage their own integrations, set up their own alert automations, and enhancing control over alert management for their teams by assigning the new team\_operator role.
-   Review relevant information in the Now Assist panel based on records selected in the Express List®.
-   Starting in version 2.15.1, you can configure metric connector instances for the Nagios, SolarWinds, and Zabbix monitoring tools to receive metrics directly from these monitoring tools. This enhancement provides the following benefits:
    -   Seamlessly integrate monitoring data from multiple sources into Metric Intelligence.
    -   Improve anomaly detection and alerting with real-time metric ingestion.

See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Group alerts using network traffic-based grouping](https://www.servicenow.com/docs/access?context=network-traffic-correlation-grouping&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Group alerts efficiently with network traffic-based alert grouping, which uses discovered TCP connections with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them.

-   **[View links between alerts in network traffic-based alert groups](https://www.servicenow.com/docs/access?context=el-network-traffic-based-link-view&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Once a network traffic correlation is enabled, investigate network traffic alert group details and visualize connections through Link View in Express List®.

-   **[New role for team level operators](https://www.servicenow.com/docs/access?context=r_InstalledWithEventManagement&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Enhance team-level control over alert management with the evt\_team\_operator role. This role enables operators to manage Event Management operations within their assigned team, including reading and writing alerts, making configuration changes,updating Alert Automation, and setting up new integrations in the Integrations Launchpad.

-   ****

    Starting in version 26.7.0, execute response subflows automatically, manually, or both for alerts that match specific conditions through the Run Other Response Actions option of Respond Automatic. This enhancement offers better control over automated responses with configurable execution limits and multiple response actions.

-   ****

    Starting in version 26.7.0, link a CI to an alert for more accurate IT component mapping though the Improve Configuration Item \(CI identification option of Enrich Automation. This enhancement improves alert visibility, speeds up issue resolution, and ensures better correlation between alerts and infrastructure components.


## Changed in this release

-   **[Property name changes](https://www.servicenow.com/docs/access?context=enable-alert-grouping&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    **Enable CMDB Correlation for Alert Aggregation \( CMDB groups\)** \(**sa\_analytics.agg.query\_cmdb\_correlation\_enabled**\) has been renamed **Enable CMDB correlation**.

    **Enable alert aggregation for CI-based Automated groups** \(**sa\_analytics.specific\_patterns\_enabled**\) has been renamed **Enable ML based Automation correlation**.

    **Enable alert aggregation for Text-based groups** \(**sa\_analytics.text\_based\_group\_enabled**\) has been renamed **Enable Text based correlation**.

    **Use all CMDB relations for CMDB group correlation. This property impacts both CMDB group correlation and Alert Similarity on the Alert form** \(**evt\_mgmt.related\_cis\_get\_all\_relation\_types**\) has been renamed **Use all CMDB relations for CMDB group correlation**.

-   **[Pull connectors](https://www.servicenow.com/docs/access?context=t_EMConfigureConnectorInstance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Simplifying the setup for Out-of-the-Box \(OOTB\) event rules that come with the pull connectors that have not yet been activated, deactivated, or modified, the Apply additional matching rules option is now enabled by default. If a rule has been previously applied, you must set this option manually.


## Activation information

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://www.servicenow.com/docs/access?context=t_EMActivatePlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Metric Explorer](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    ServiceNow® Agent Workspace for [Metric Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) provides a central interface that enables you to view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds and aggregations for single score charts.


