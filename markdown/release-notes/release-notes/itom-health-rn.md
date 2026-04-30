---
title: ITOM AIOps release notes
description: The ServiceNow ITOM AIOps product helps you to keep track and maintain the health of the services in your organization. ITOM AIOps was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
keywords: [ITOM Health release notes]
---

# ITOM AIOps release notes

The ServiceNow® ITOM AIOps product helps you to keep track and maintain the health of the services in your organization. ITOM AIOps was enhanced and updated in the Zurich release.

## ITOM AIOps highlights for the Zurich release

Health Log Analytics highlights:

-   Streamline Health Log Analytics data ingestion with Cribl by using the Cribl integration.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) highlights:

-   Control how alerts are grouped, which ones are included, and the order of grouping methods through Mixed Alert Grouping, which combines CMDB-based and tag-based strategies.
-   Starting in version 26.9.0, investigate mixed alert groups and Log Analytics-based alert groups by using Express List®.
-   Starting in version 26.9.0, view connections between alerts in Link View for mixed alert groups and Log Analytics-based alert groups.

See [ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** [Agent Client Collector](agent-client-collector-rn.md) and [Health Log Analytics](health-log-analytics-rn.md) are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.

-   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 37.0.15, take advantage of additional information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.

-   **[Benefit from enhanced Log Analytics alert group and mixed alert group functionality in the Express List](https://www.servicenow.com/docs/access?context=el-link-view&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.9.0, identify connected Log Analytics alerts and mixed alert group correlations faster using the Link View functionality. Utilize enhanced Now Assist Alert Analysis with additional context for Log Analytics alerts.

-   **[View visualizations of anomaly information for Log Analytics-based alerts and metric intelligence alerts in Express List®](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.9.0, review anomaly charts for Log Analytics alerts and Metric Intelligence alerts in the preview panel in Express List®.

-   **[Configure automatic resume for live updates when the live alert list is paused, and configure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 26.9.0, enable admins to configure the amount of time until the active display resumes after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®.


-   **[Map log data to service instances and components for alerts in context](https://www.servicenow.com/docs/access?context=il-connector-hla-map-business-context&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://www.servicenow.com/docs/access?context=hla-data-input-log-export&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


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


## Deprecations

-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

## Activation information

-   ITOM AIOps is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). You must purchase a more comprehensive ITOM AIOps package, ITOM Predictive AIOps, to enable working with Health Log Analytics. For details, see [Event Management setup](https://www.servicenow.com/docs/access?context=c_EMConfiguration&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).
-   Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Support for reflow**

    The Service Dashboard and Log Viewer component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See  for details.


-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

## Related ServiceNow applications and features

-   **[ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The ITOM Visibility application consists of [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), Certificate Inventory and Management, Service Graph Connectors, CMDB 360, and Firewall Audits and Reporting. Discovery and Service Mapping provide a unified, connected view of your entire IT network and the services that it supports.

-   **[ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    ITOM Optimization contains the [Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) feature. By using this feature, you can provision a private and public cloud infrastructure and services to achieve consistent management and cost visibility.

-   **[Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Service Operations Workspace ITSM and ITOM are integrated to streamline incident and operations management. ITSM focuses on managing service incidents, requests, and changes, while ITOM is responsible for operational tasks like monitoring infrastructure, handling alerts, and maintaining system health. Together, they provide a unified workspace that enables seamless collaboration between service management and operations teams, improving efficiency in resolving issues and maintaining service performance.


-   **[Agent Client Collector release notes](agent-client-collector-rn.md)**  
The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. Agent Client Collector was enhanced and updated in the Zurich release.
-   **[Event Management release notes](event-management-rn.md)**  
The ServiceNow® Event Management application helps you to identify health issues across the datacenter on a single management console. Event Management was enhanced and updated in the Zurich release.
-   **[Health Log Analytics release notes](health-log-analytics-rn.md)**  
The ServiceNow® Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Zurich release.
-   **[Service Observability release notes](service-observability-rn.md)**  
The ServiceNow® Service Observability application helps operations teams triage and manage incidents in a complex and distributed production system. Service Observability combines telemetry and platform insights from multiple observability tools into a single workflow in the Service Operations Workspace \(SOW\). Service Observability was enhanced and updated in the Zurich release.
-   **[Service Reliability Management release notes](service-reliability-management-rn.md)**  
The ServiceNow® Service Reliability Management \(SRM\) application helps your organization respond, collaborate, track, and self-remediate when working on alerts and incidents. SRM was enhanced and updated in the Zurich release.
-   **[Synthetic monitoring release notes](synthetic-monitoring-rn.md)**  
The ServiceNow® synthetic monitoring application in the Service Operations Workspace \(SOW\) empowers organizations to proactively manage and enhance the performance and availability of critical service endpoints. By simulating user transactions on HTTP endpoints, this solution identifies performance bottlenecks, helps ensure up-time, and optimizes user experiences. Synthetic monitoring was enhanced and updated in the Zurich release.

**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

