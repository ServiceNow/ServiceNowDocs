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

See [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-server-landing.md) for more information.

## Important information for upgrading MID Server to Yokohama

For the latest MID Server system requirements, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/r_MIDServerSystemRequirements.md). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-startup-fails.md) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/c_UpgradeAndTestMIDServer.md): Describes how to upgrade your MID Servers manually.

## New in the Yokohama release

-   **[External Credential Storage and Management supports certificate-based authentication for Azure Key Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-azure-key-vault-integration.md)**

    The External Credential Storage and Management added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.


## Changed in this release

-   **[MID Server supports and requires a minimum JRE version 17](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/r_MIDServerSystemRequirements.md)**

    The MID Server is compiled using Java 17 and is incompatible with any Java version below 17 for runtime execution. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10. See the [MID Server JRE Minimum Version Requirement Update to JRE 17 Starting from Yokohama Release \[KB1704368\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704368) article in the Now Support Knowledge Base for information about required procedures before upgrading the instance.

-   **[Improvements when manually installing a MID Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/mid-server-install-prereqs.md)**

    The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.


## Removed in this release

-   When upgrading to the Yokohama release, 3DES will be permanently removed from MID Server to improve security. See [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950) for more information.

## Activation information

MID Server is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/r-discovery.md)**

    Discovery uses the MID Server to launch probes and patterns that return information to the CMDB about devices and applications running in your environment. Discovery schedules select appropriate MID Servers based on their configured capabilities and assigned IP ranges.

-   **[Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/r-orchestration.md)**

    Orchestration uses the MID Server to do work on internal and external systems. Orchestration selects MID Servers based on their capabilities and the applications that they’re allowed to use.

-   **[Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/c_ServiceMappingOverview.md)**

    Service Mapping uses the MID Server to launch patterns that return information about business services running in your environment.

-   **[Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/c_EM.md)**

    Event Management uses the MID Server to receive and process events, collect data for root cause analysis \(RCA\), and collect SNMP traps.

-   **[Cloud Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/cloud-management-v2-landing-page.md)**

    Cloud Management uses the MID Server to collect and process VMware events.

-   **[Operational Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/operational-metrics.md)**

    Operational Intelligence uses MID Server clusters to capture operational metrics data from external data sources and analyze them for anomalies.

-   **[Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/hla-landing-page.md)**

    Health Log Analytics uses the MID Server to collect log data streaming into your instance and helps you identify the root cause of issues.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-capabilities-rn-landing.md)

