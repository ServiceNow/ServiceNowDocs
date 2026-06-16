---
title: Health Log Analytics release notes
description: Version history for the Health Log Analytics application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-health-log-analytics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 13
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Health Log Analytics release notes

Version history for the Health Log Analytics application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 40.0.13 - June 2026**
    -   Stream log data with Agent Client Collector Log AnalyticsUse the new ACC-L integration in Integration Launchpad to stream log messages to your ServiceNow instance. This integration is designed for environments where agentless log collection is impractical due to security requirements or host accessibility constraints.
    -   Support Linux capabilities with updated ACC-L folder structureACC-L agents now includemanifest.cfg andmanifest.sig files to support Linux capabilities and improved log shipper error output. These changes reduce support issues and speed up troubleshooting.
    -   Query and review HLA metrics from a single locationThe new Metric Data table consolidates all metrics that Health Log Analytics collects and monitors, including pattern, custom, and raw metrics. Filter by log source, integration, source type, or metric type, and review anomaly detection statistics and baselines in one place.
-   **Version 39.0.16 - March 2026**
    -   New:
        -   AI Agent for Log Field Classification: A new Now Assist skill automatically classifies and labels log fields within Source Type Structures.
        -   AI Agent for Business Context Mapping: A new Now Assist skill automatically recommends Service Instance and Component mapping fields from log data stored in the sample reservoir.
        -   'What If?' Hypothesizer AI Skill for HLA Alerts: A new skill within the Autonomous IT Operator workflow that analyzes HLA alert context.
        -   HLA Implementation Score-per-data-input and per-log-source implementation scoring is now available.
        -   Smart Sampling for Business Context Mapping: A new intelligent sampling mechanism collects statistically significant log samples using a field-selection algorithm.
    -   Fixed:
        -   Security: Patched vulnerable libraries including protobuf-java and netty-handler.
        -   Log streaming via ITOM Gateway was failing in certain configurations.
        -   NewPatternRateHealthCheck stopped monitoring source types after a server restart due to metric counter reset.
        -   MID-less data inputs lacked the Service Instance field on the Integration Launchpad UI.
        -   Smart Parser continued executing even when the Auto Parser 'ignored' flag was set on a source type.
        -   Azure EventHubs data input was automatically and incorrectly appending servicebus.windows.net as the domain name.
        -   The total log source count shown in the UI was incorrectly displaying 1 source per data input instead of the actual total.
-   **Version 38.0.17 - December 2025**
    -   New:
        -   HLA is now available for On-Premise deployments
        -   New HLA Admin Experience \(Phase 1\): Map Log Context
            -   New UX for viewing data input mapping results
            -   Streamlined, simplified manual steps
            -   Clear visibility and explanations
    -   Changed:
        -   Enabled export of HLA setup configurations by Log Source, facilitating environment migration and cloning
        -   HLA administration and maintenance:
            -   Enhanced visibility into AI Engine status for better supportability.
            -   Failed HLA health checks are displayed in Integration Launchpad screens
            -   Improved user messages and warnings in HLA screens: Data Input Mapping, Source Type Structure
            -   Added new HLA health checks to ease the HLA setup process.
        -   Created Log Export Service \(LES\) integration for HLA to read glide-node and other logs exportable via LES
    -   Fixed:
        -   Resolved the issue where surrounding logs were not being created
        -   Fixed generic UX defects in log integrations in Integrations Launchpad
        -   Addressed general defects and bug fixes
-   **Version 37.0.15 - August 2025**
    -   New:
        -   Integrations Launchpad – New UX for Cribl Data Input \(push/pull\) including Setup Connection wizard.
        -   Integrations Launchpad – Overview screen enhancements: ITOM Gateway step for HLA Scale deployment, cache pre-loading, and last-log-time indicator.
        -   Improved Anomaly Card in Express List side panel – UI now highlights the anomaly window \(“red span”\) using backend span and additional baseline data.
    -   Changed:
        -   Integrations Launchpad Overview – Faster load times and continuous 1-minute auto-refresh \(continues even after errors\).
        -   Enhanced backend data structures powering dashboards and richer alert previews.
    -   Fixed:
        -   Overview screen reliability – Resolves occasional stale data after cache invalidation.
        -   Additional performance and stability fixes across HLA, HLA Core and Integrations Launchpad \(60+ defects\).
    -   Known Issues:
    -   Cribl Integration – “Credential Alias” field may show no options when the default alias is empty.
        -   Work-around: Select “Manage Credential Aliases” and add a credential record to the alias with Name "Cribl Credential Alias" and ID 'sn\_itom \_integ\_app.Cribl\_Credential\_Alias'.
-   **Version 36.1.11 - July 2025**

    Fixed: ServiceNow System Logs Retriever data input streaming stops working under certain circumstances

-   **Version 36.0.19 - May 2025**
    -   New:
        -   Log Properties Classification Recommendations - In the Source Type Structure, get recommendations on how to classify extracted properties to ensure optimal analysis by the HLA Engine.
        -   Quick-start HLA - Reduce setup time by applying default minimal parsing on the first ingestion into HLA, allowing further iterative setup and improved configuration as needed. Improvements to default system features, properties, and parsing algorithms to allow smoother and more reliable streaming.
        -   Added native support for logs formatted according to the OpenTelemetry logging standard, and improved support for the Elastic Common Schema \(ECS\).
        -   The MID Server data input was added to the Integration Launchpad to simplify setup.
        -   New MID-less ingest - Support MID-less integration to Amazon Data Firehose.
    -   Changed:
        -   ServiceNow System Logs Integration - Updates to OOTB settings, including automatic startup.
        -   Added health checks to configuration pages \(Data Input Mapping and Source Type Structure\) to ensure proper setup and system robustness.
        -   Deprecation of Component-based groups - Removed 3-leveled Log Analytics groups that included Read-Only alerts as children of Component-based alerts, which in turn were children of the Log Analytics alert \(a group of groups\). Following this change, each single alert coming from HLA will be bound to the appropriate Service Instance CI, with an option to view relevant host CIs when applicable. The Log Analytics group alert will be a group of single alerts from HLA. This grouping process still happens in the HLA Engine, using unsupervised learning.
    -   Fixed:
        -   Improved stability of the ServiceNow System Logs Retriever integration.
        -   Fixed missing All Components option in Log Viewer.
        -   Errors when starting the HLA Engine for the first time.
        -   Generic bugs.
    -   Removed: Deprecation of Component-based groups - Removed 3-leveled Log Analytics groups that included Read-Only alerts as children of Component-based alerts, which in turn were children of the Log Analytics alert \(a group of groups\). Following this change, each single alert coming from HLA will be bound to the appropriate Service Instance CI, with an option to view relevant host CIs when applicable. The Log Analytics group alert will be a group of single alerts from HLA. This grouping process still happens in the HLA Engine, using unsupervised learning.
-   **Version 35.0.26 - February 2025**
    -   New:
        -   Integrations Launchpad:  Integrations Launchpad supports four log integrations with a new, improved UI: System Logs retriever, Elasticsearch, TCP, and UDP. 
        -   The Overview page in Integrations Launchpad enables viewing and validating the integration status.
        -   Quickly debug and detect streaming issues if they occur 
        -   New data inputs enable connecting log data from Cribl, Datadog Vector Agents, and Edge Delta. 
    -   Changed:
        -   Improvements to System Logs retriever data input. 
        -   New data model for metric data extracted from logs, improving the analytical scale. 
        -   Improved system health checks and visibility. 
    -   Fixed:
        -   Log streaming performance bugs. 
        -   Security fixes. 
-   **Version 34.0.37 - December 2024**
    -   Rename Application Service fields label to Service Instance.
    -   Optimize Clotho dimensions when the Message key is unassigned, properties are re-classified, and log sources are deleted.
    -   Performance improvements to refresh samples UI action on Source Type Structure screen.
    -   Security improvements for communication between the AI engine and the time series database.
-   **Version 33.0.31 - December 2024**

    Bug fixes.

-   **Version 33.0.27 - August 2024**
    -   New:
        -   Ability to see all properties extracted from a source type and classification/labels in the same flow.
        -   Identify problematic raw metrics in runtime and fix them before Occultus crashes.
        -   Support monitoring ServiceNow instance Syslog with HLA.
        -   Ability to see all learned patterns from a source type.
        -   Support native OTel header detection.
        -   Collect usage metrics for HLA.
        -   Add many-to-many mapping in Glide between source types and log sources.
        -   Notify user of problematic configurations in the Source Type Structure.
        -   Align HLA to support Elasticsearch 8.
    -   Changed: Alert Notifications: Replaced deprecated Teams plugin.
-   **Version 32.0.6 - May 2024**
    -   New:
        -   New data input to send logs from Service Now Cloud Observability to Health Log Analytics for analysis. The data input is initiated from Cloud Observability and all relevant Health Log Analytics configurations needed to parse and analyze the data are created automatically. This allows quicker implementations of Health Log Analytics for applications monitored by Cloud Observability.
        -   Support Elasticsearch 8 - upgrading dependencies and supporting new features for Elasticsearch 8.
    -   Changed: Improve health checks and robustness of data streaming.
    -   Fixed:
        -   Package dependencies and security updates.
        -   Several defects fixed, including supporting new Elasticsearch 8, removing backwards compatibility for Smart Parsers, and fixing default KBs.
-   **Version 30.1.2 - March 2024**

    Slowlog fix to support upgrade to Elastic Search 8.

-   **Version 27.2.5 - March 2024**

    Slowlog fix to support upgrade to Elastic Search 8.

-   **Version 30.0.4 - February 2024**
    -   Timestamp parsing enhancements
    -   Bug fixes
-   **Version 29.0.11 - November 2023**
    -   The release contains:
        -   A scalable, more stable way to stream logs with ITOM Health Log Analytics using the new ServiceNow infrastructure, leveraging queueing technology based on Kafka as well as additional scalable services that are part of the ITOM Cloud Services, to allow authentication and ingestion management.
        -   Scalability for the internal core engine and database used by ITOM Health Log Analytics to allow processing, analyzing, anomaly detection, and storing of logs at scale.
        -   Support for up to 240K logs per second, under testing assumptions of average-size logs of 300 bytes.
        -   Note: Testing was done under lab conditions and results may change based on a particular use case and the specific nature of the logs, number of MIDs, HW and network resources, and the size of the ServiceNow Instance.
        -   Support for advanced source type parsers to allow scripts for multiple JSONs.
-   **Version 27.1.12 - August 2023**

    Bug fixes.

-   **Version 27.0.7 - June 2023**
    -   New:
        -   Support giving ML feedback to stop generating unimportant alerts for multiple components of the Application Service
        -   User notification displayed when AI engine is down
        -   Health check notifies admin when no HLA alerts were generated for a configurable time period
-   **Version 27.0.6 - May 2023**
    -   New:
        -   Support providing ML feedback to stop generating insignificant alerts, for multiple components
        -   User notification presented when the AI engine is down
        -   Health check that notifies the admins whenever no HLA alerts were generated for a certain \(configurable\) period
    -   Fixed: Bug fixes
-   **Version 26.0.17 - February 2023**
    -   New:
        -   MID Server Cluster: Health Log Analytics now supports MID Servers Cluster for all the pull log data inputs. Using MID Cluster for fail-over protection have a configured order used to determine which MID Server to use next if a failure occurs.
        -   Test Outcome Table: A table was added to the Data Input Mapping form. The table presents the outcome of the mapping between log samples to log sources and source types. The table updates after logs samples refresh and click on the test button.
    -   Changed: Improvements in the data input mapping form, number of the maximal log samples increased to 5000, and the responsiveness was improved.
    -   Fixed: Several bug fixes
-   **Version 25.0.17 - November 2022**
    -   New:
        -   HLA configuration migration: Enables you to export data inputs and source types configuration as an update set, import the update set to the target instance, and start streaming logs using the imported configuration.
        -   Test mode: A designated mode for stabilizing data input mapping. When Test mode is On, the streamed logs do not go through the standard log processing flow but are instead stored under a temporary component in Elasticsearch, which is deleted when Test mode is set to Off.
        -   Test data input connection: Ensures that the data input is configured correctly. When you select Test connection, Health Log Analytics tries to connect the MID Server to the data repository.
        -   Out-of-the-box Operational dashboard: A predefined dashboard with the most common log data visualizations​ to help you monitor your log data. Using this dashboard, you can view log behavior in the last 24 hours and better understand the health of your application services.
        -   Content packs: The ability to configure data streaming for Linux systems with one simple click using the new content packages. This process automatically triggers different functions that shorten onboarding time for the Health Log Analytics application by implementing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.
    -   Changed:
        -   Improvements in the data input mapping form that show the log sources to be created by the current mapping script. Added the ability to increase the number of log samples to 500.
        -   The ability to delete log sources together with their associated indices in Elasticsearch.
    -   Fixed: Surrounding logs issues.
-   **Version 24.0.9 - October 2022**
    -   New:
        -   Starting from this version, you can create customized visualizations and dashboards in the Platform Analytics Workspace. Visualizations enable you to better understand and monitor your log data, especially when it is grouped together in a dashboard. Built on the fields that Health Log Analytics extracts from your logs, dashboards can be easily created to represent any aspect of the data, rather than a breakdown of specific fields \(for example, http status codes\), the geographical distribution of your data, or trends over time of specific fields, such as failed login attempts.
        -   Configure your Slack or Teams channel for HLA alert notification to receive alerts directly to your notification's channels. You can customize the notifications according to your business needs.
        -   Update to provide feedback to the system engine. The Raise feedback option enables you to tell the system when you want the engine to be less sensitive to a specific anomaly.
    -   Changed: Surrounding logs of alerts are shown according to retention settings.
    -   Fixed: PA reports for HLA Dashboard calculation fixes.
-   **Version 24.0.6 - August 2022**
    -   New:
        -   Starting from this version, you can create customized visualizations and dashboards in the Platform Analytics Workspace. Visualizations enable you to better understand and monitor your log data, especially when it is grouped together in a dashboard. Built on the fields that Health Log Analytics extracts from your logs, dashboards can be easily created to represent any aspect of the data, rather than a breakdown of specific fields \(for example, http status codes\), the geographical distribution of your data, or trends over time of specific fields such as failed login attempts.
        -   Configure your Slack or Teams channel to the HLA alert notification to receive alerts directly to your notification channels. You can customize the notifications according to your business needs.
        -   Update to provide feedback to the system engine. The Raise feedback enables you to tell the system when you want the engine to be less sensitive to a specific anomaly.
    -   Changed: Surrounding logs of alerts are shown according to the retention settings.
    -   Bug fixes: Fixes and changes to increase efficiency and improve product experience. These changes are not visible to the user.
    -   Security fixes.
    -   UI fixes.
-   **Version 23.0.20 - June 2022**
    -   New: Test connectivity to data inputs
    -   Changed: System health notifications
    -   Fixed: Bug fixes
-   **Version 21.0.1 - September 2021**
    -   New:
        -   New data inputs:
            -   Amazon CloudWatch
            -   Amazon S3
            -   Microsoft Azure Log Analytics
            -   Microsoft Azure Event Hubs
            -   Apache Kafka
            -   REST API, for streaming your log data to the ServiceNow instance in JSON format
        -   Log viewer filter panel
        -   Domain separation support
    -   Fixed: UI fixes
-   **Version 20.0.11 - July 2021**
    -   New: Log viewer usability functionality Filter panel for extracted properties Personalized view in the Log viewer New templates for the preprocessor, mapping, and source type screens Splunk data input changes
    -   Changed: Define an alert without dependencies
    -   Fixed: Bug fixes Usability fixes
-   **Version 19.1.7 - June 2021**

    Fixed stability issues

-   **Version 19.1.5 - May 2021**

    Fixed: Minor UI fixes

-   **Version 19.1.4 - March 2021**
    -   New:
        -   Benefit from the ability to predict IT issues by detecting anomalies in your log data
        -   Get alerted on an emerging issue before it affects your users
        -   Cut the Mean Time to Repair \(MTTR\) by learning the true root cause of an issue in real-time
        -   Receive instant data-driven advice on how to fix an issue

**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

