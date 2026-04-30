---
title: MID Server release notes
description: The ServiceNow MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# MID Server release notes

The ServiceNow® MID Server application enables communication and data transfers between a ServiceNow instance and external applications, data sources, and services. MID Server was enhanced and updated in the Yokohama release.

## MID Server highlights for the Yokohama release

-   MID Server supports and requires a minimum JRE version 17. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10.
-   The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading MID Server to Yokohama

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

## New in the Yokohama release

-   **[External Credential Storage and Management supports certificate-based authentication for Azure Key Vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The External Credential Storage and Management added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.


## Changed in this release

-   **[MID Server supports and requires a minimum JRE version 17](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The MID Server is compiled using Java 17 and is incompatible with any Java version below 17 for runtime execution. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10. See the [MID Server JRE Minimum Version Requirement Update to JRE 17 Starting from Yokohama Release \[KB1704368\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704368) article in the Now Support Knowledge Base for information about required procedures before upgrading the instance.

-   **[Improvements when manually installing a MID Server on Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.


## Removed in this release

-   When upgrading to the Yokohama release, 3DES will be permanently removed from MID Server to improve security. See [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950) for more information.

## Activation information

MID Server is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Discovery uses the MID Server to launch probes and patterns that return information to the CMDB about devices and applications running in your environment. Discovery schedules select appropriate MID Servers based on their configured capabilities and assigned IP ranges.

-   **[Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Orchestration uses the MID Server to do work on internal and external systems. Orchestration selects MID Servers based on their capabilities and the applications that they’re allowed to use.

-   **[Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Service Mapping uses the MID Server to launch patterns that return information about business services running in your environment.

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Event Management uses the MID Server to receive and process events, collect data for root cause analysis \(RCA\), and collect SNMP traps.

-   **[Cloud Management](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Cloud Management uses the MID Server to collect and process VMware events.

-   **[Operational Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Operational Intelligence uses MID Server clusters to capture operational metrics data from external data sources and analyze them for anomalies.

-   **[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Health Log Analytics uses the MID Server to collect log data streaming into your instance and helps you identify the root cause of issues.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

