---
title: MID Server release notes
description: The ServiceNow MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# MID Server release notes

The ServiceNow® MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Zurich release.

## MID Server highlights for the Zurich release

-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.
-   MID Server logging has been improved with log backups that are preserved in a compressed format on a local host with an option to fetch to the instance.

See [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/mid-server-landing.md) for more information.

## Important information for upgrading MID Server to Zurich

For the latest MID Server system requirements, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerSystemRequirements.md). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/mid-startup-fails.md) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md): Describes how to upgrade your MID Servers manually.

## New in the Zurich release

-   **[ITOM Infra Services Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/itom-infra-srv-wrksp-mid.md)**

    The ITOM Infra Services Workspace provides a concise overview of MID Server activity. The dashboard integrates several previously disparate tables so that issues can be monitored and resolved. The workspace provides real-time monitoring, proactive alerts, automation of common tasks, and centralized diagnostics to reduce downtime and support tickets.

-   **[MID Guardian Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/mid-guardian.md)**

    The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem/ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. By intelligently analyzing logs, signals, and runtime behaviors, it offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server.


## Changed in this release

-   **[Smart Workload Manager in clusters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_ConfigureAMIDServerCluster.md)**

    MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[Enhancements to MID Server logging and JFR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerTroubleshooting.md)**

    MID Server logging has been improved with log backups that are preserved in a compressed format on local host with option to fetch to the instance. You can enable JFR logs every four hours and backup JFR files for a set time.

-   **[MID Server has improved performance during heavy discovery load](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerSystemRequirements.md)**

    MID Servers no longer have performance degradation due to script include cache misses when using large amounts of worker threads.

-   **[MID Server security logs require 100MB of storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/r_MIDServerSystemRequirements.md)**

    To store the security logs, MID Servers must be installed on a host with at least 100MB of storage capacity.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

MID Server is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/r-discovery.md)**

    ServiceNow®Discovery uses the MID Server to launch probes and patterns that return information to the CMDB about devices and applications running in your environment. Discovery schedules select appropriate MID Servers based on their configured capabilities and assigned IP ranges.

-   **[Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/r-orchestration.md)**

    ServiceNow®Orchestration uses the MID Server to do work on internal and external systems. Orchestration selects MID Servers based on their capabilities and the applications that they’re allowed to use.

-   **[Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/c_ServiceMappingOverview.md)**

    ServiceNow®Service Mapping uses the MID Server to launch patterns that return information about business services running in your environment.

-   **[Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/c_EM.md)**

    ServiceNow®Event Management uses the MID Server to receive and process events, collect data for root cause analysis \(RCA\), and collect SNMP traps.

-   **[Cloud Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/cloud-management-v2-landing-page.md)**

    ServiceNow®Cloud Management uses the MID Server to collect and process VMware events.

-   **[Operational Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/operational-metrics.md)**

    ServiceNow®Operational Intelligence uses MID Server clusters to capture operational metrics data from external data sources and analyze them for anomalies.

-   **[Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/hla-landing-page.md)**

    ServiceNow®Health Log Analytics uses the MID Server to collect log data streaming into your instance and helps you identify the root cause of issues.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-capabilities-rn-landing.md)

