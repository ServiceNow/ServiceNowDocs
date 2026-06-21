---
title: Combined MID Server release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for MID Server from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-midserver-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined MID Server release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for MID Server from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family MID Server release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading MID Server to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=xanadu&ft:locale=en-US). The minimum JRE version supported is 11.0.9 and the recommended version is 11.0.16.1.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&family=xanadu&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Yokohama

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=yokohama&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&family=yokohama&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Zurich

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=zurich&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&family=zurich&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Australia

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 21.0.7.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&family=australia&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for MID Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[MID Server support for Azure Key vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&family=xanadu&ft:locale=en-US)**

The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[External Credential Storage and Management supports certificate-based authentication for Azure Key Vault](https://www.servicenow.com/docs/access?context=mid-azure-key-vault-integration&family=yokohama&ft:locale=en-US)**

The External Credential Storage and Management added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ITOM Infra Services Workspace](https://www.servicenow.com/docs/access?context=itom-infra-srv-wrksp-mid&family=zurich&ft:locale=en-US)**

The ITOM Infra Services Workspace provides a concise overview of MID Server activity. The dashboard integrates several previously disparate tables so that issues can be monitored and resolved. The workspace provides real-time monitoring, proactive alerts, automation of common tasks, and centralized diagnostics to reduce downtime and support tickets.

-   **[MID Guardian Agent](https://www.servicenow.com/docs/access?context=mid-guardian&family=zurich&ft:locale=en-US)**

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem/ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. By intelligently analyzing logs, signals, and runtime behaviors, it offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing MID Server features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[MID Server log enhancement](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637658)**

MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode is not enabled in the base system.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[MID Server supports and requires a minimum JRE version 17](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=yokohama&ft:locale=en-US)**

The MID Server is compiled using Java 17 and is incompatible with any Java version below 17 for runtime execution. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10. See the [MID Server JRE Minimum Version Requirement Update to JRE 17 Starting from Yokohama Release \[KB1704368\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704368) article in the Now Support Knowledge Base for information about required procedures before upgrading the instance.

-   **[Improvements when manually installing a MID Server on Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&family=yokohama&ft:locale=en-US)**

The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&family=zurich&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[Enhancements to MID Server logging and JFR](https://www.servicenow.com/docs/access?context=r_MIDServerTroubleshooting&family=zurich&ft:locale=en-US)**

MID Server logging has been improved with log backups that are preserved in a compressed format on local host with option to fetch to the instance. You can enable JFR logs every four hours and backup JFR files for a set time.

-   **[MID Server has improved performance during heavy discovery load](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=zurich&ft:locale=en-US)**

MID Servers no longer have performance degradation due to script include cache misses when using large amounts of worker threads.


</td></tr><tr><td>

Australia

</td><td>

-   **[MID Server supports PowerShell 7 for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&family=australia&ft:locale=en-US)**

MID Server now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Configure the MID Server for CyberArk CCP](https://www.servicenow.com/docs/access?context=t_ConfigureTheMIDServerForCyberArkCCP&family=australia&ft:locale=en-US)**

MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices. This additional option can reduce dependency overhead and enables you to choose between the AIM SDK and REST-based approaches according to your requirements.

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&family=australia&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[MID Server is bundled with Java Runtime Environment 21](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US)**

MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10. The installer automatically configures Java 21.0.7 to run in your environment. If you have installed your own JRE, see the **Important information for upgrading MID Server to Australia** section to ensure your JRE is compatible.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some MID Server features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   When upgrading to the Yokohama release, 3DES will be permanently removed from MID Server to improve security. See [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950) for more information.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some MID Server features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate MID Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for MID Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for MID Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for MID Server, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for MID Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for MID Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Run other applications without storing any credentials on the instance with the Azure Key vault.
-   MID Server supports log file compression.

 See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   MID Server supports and requires a minimum JRE version 17. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10.
-   The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.

 See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.
-   MID Server logging has been improved with log backups that are preserved in a compressed format on a local host with an option to fetch to the instance.

 See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10.
-   MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices.
-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.

 See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

