---
title: TSOM Event Management Connectors release notes
description: Version history for the ServiceNow TSOM Event Management Connectors application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-tsom-event-mgmt-connectors.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Telecommunications Service Management version history release notes, ServiceNow Store version history release notes]
---

# TSOM Event Management Connectors release notes

Version history for the ServiceNow® TSOM Event Management Connectors application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 4.0.8 - September 2026**

    This release adds a StackInfra pull connector, along with new launchpad tiles for the Equinix, OpsInsight, StackInfra, and DigitalRealty integrations to make them easier to find and set up. Fortinet devices can now push metrics directly to TSOM instead of only being polled, and Nokia MPN security logs now generate anomaly alerts automatically. Fixes include corrected metric alignment so Equinix data maps to the right CMDB records, resolved issues with Nokia MPN alarms not closing properly and short-lived alarms being missed, corrected incorrect and negative Nokia MPN latency values with improved device inclusion for end-to-end latency calculations, corrected health-status \(red/amber/green\) calculation for radio and core-server devices with fixed event severity labeling, and a fix for a timing issue that could cause incorrect data-recovery windows after a Fortinet/Meraki outage. Nokia MPN device and version resolution and performance-metric collection have also been made more reliable, with health-status logic moved into the connector itself for more consistent results across environments.

-   **Version 3.0.6 - August 2026**

    The Event Management Core app has been fully converted to the Fluent SDK \(Now SDK\) TypeScript format, completing the modernization effort alongside the connector and core apps.

-   **Version 2.9.1 - July 2026**
    -   This release makes EM Connectors enterprise-ready at scale with more reliable data collection, direct operator control, and configuration-time failure detection.
        -   What's new
            -   Configurable metric granularity for Fortinet and Meraki
            -   Configuration-time validation
            -   Meraki rate-limit resilience
            -   Complete data retrieval for large deployments
            -   Reduced installation footprint
        -   Issues fixed
            -   Fortinet API efficiency improvements
            -   SLA accuracy corrections
            -   Collection scheduling fixes
        -   Before you upgrade
            -   Update metricNamingModetodynamicMetricNamingMode.
            -   Ensure kpi\_definitionsaccess roles includetsom\_assurance\_admin.
-   **Version 2.5.1 - June 2026**
    -   New:
        -   Provides a full Nokia MPN Pull Connector for Fault Management \(FM\) and Performance Management \(PM\)
        -   Introduces a KPI Formula Engine with Excel import support for formula definitions
        -   Supports configurable CI names and KPI nodes for Nokia MPN
        -   Detects stale alarms using the alarmClearedTime field mapping
        -   Binds CIs via the EventFieldMapping extension point across vendors
    -   Fixed: Adds missing roles for KPI definitions and network service instances
    -   Changed: Updates localization and translation strings
-   **Version 2.2.2 - May 2026**

    This release enhances the stability, reliability, and usability of SD-WAN connectors, helping ensure smoother operations and more dependable performance. Updates also improve the accuracy and consistency of Meraki Discovery performance test results. The application has been renamed to Service Graph Connector for Meraki Telco SD-WAN to better reflect its purpose and scope. Accessibility improvements include better color contrast and zoom support up to 400%.

-   **Version 2.1.2 - April 2026**

    This release includes bug fixes for SD-WAN connectors to improve stability and reliability.

-   **Version 2.0.0 - March 2026**
    -   New: VeloCloud events
    -   Changed: Added additional metric for Cisco Meraki
-   **Version 1.1.3 - February 2026**
    -   Cisco Meraki events and metrics
    -   Fortinet events and metrics
    -   All connector features released this version, including TMF recovery

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

