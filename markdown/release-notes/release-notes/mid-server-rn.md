---
title: MID Server release notes
description: The ServiceNow MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# MID Server release notes

The ServiceNow® MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Xanadu release.

## MID Server highlights for the Xanadu release

-   Run other applications without storing any credentials on the instance with the Azure Key vault.
-   MID Server supports log file compression.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading MID Server to Xanadu

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 11.0.9 and the recommended version is 11.0.16.1.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

## New in the Xanadu release

-   **[MID Server support for Azure Key vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.


## Changed in this release

-   **[MID Server log enhancement](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637658)**

    MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode is not enabled in the base system.


## Activation information

MID Server is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Discovery uses the MID Server to launch probes and patterns that return information to the CMDB about devices and applications running in your environment. Discovery schedules select appropriate MID Servers based on their configured capabilities and assigned IP ranges.

-   **[Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Orchestration uses the MID Server to do work on internal and external systems. Orchestration selects MID Servers based on their capabilities and the applications that they’re allowed to use.

-   **[Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Service Mapping uses the MID Server to launch patterns that return information about business services running in your environment.

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Event Management uses the MID Server to receive and process events, collect data for root cause analysis \(RCA\), and collect SNMP traps.

-   **[Cloud Management](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Cloud Management uses the MID Server to collect and process VMware events.

-   **[Operational Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Operational Intelligence uses MID Server clusters to capture operational metrics data from external data sources and analyze them for anomalies.

-   **[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Health Log Analytics uses the MID Server to collect log data streaming into your instance and helps you identify the root cause of issues.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

