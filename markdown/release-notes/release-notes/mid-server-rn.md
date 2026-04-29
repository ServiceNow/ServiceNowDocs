---
title: MID Server release notes
description: The ServiceNow MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# MID Server release notes

The ServiceNow® MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Australia release.

## MID Server highlights for the Australia release

-   MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10.
-   MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices.
-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading MID Server to Australia

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 21.0.7.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

## Changed in this release

-   **[MID Server supports PowerShell 7 for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    MID Server now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Configure the MID Server for CyberArk CCP](https://www.servicenow.com/docs/access?context=t_ConfigureTheMIDServerForCyberArkCCP&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices. This additional option can reduce dependency overhead and enables you to choose between the AIM SDK and REST-based approaches according to your requirements.

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[MID Server is bundled with Java Runtime Environment 21](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10. The installer automatically configures Java 21.0.7 to run in your environment. If you have installed your own JRE, see the **Important information for upgrading MID Server to Australia** section to ensure your JRE is compatible.


## Activation information

MID Server is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Discovery uses the MID Server to launch probes and patterns that return information to the CMDB about devices and applications running in your environment. Discovery schedules select appropriate MID Servers based on their configured capabilities and assigned IP ranges.

-   **[Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    ServiceNow®Orchestration uses the MID Server to do work on internal and external systems. Orchestration selects MID Servers based on their capabilities and the applications that they’re allowed to use.

-   **[Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Service Mapping uses the MID Server to launch patterns that return information about business services running in your environment.

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Event Management uses the MID Server to receive and process events, collect data for root cause analysis \(RCA\), and collect SNMP traps.

-   **[Cloud Management](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Cloud Management uses the MID Server to collect and process VMware events.

-   **[Operational Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Operational Intelligence uses MID Server clusters to capture operational metrics data from external data sources and analyze them for anomalies.

-   **[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    ServiceNow®Health Log Analytics uses the MID Server to collect log data streaming into your instance and helps you identify the root cause of issues.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

