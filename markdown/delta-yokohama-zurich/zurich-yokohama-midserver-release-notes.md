---
title: Combined MID Server release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for MID Server from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-midserver-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined MID Server release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for MID Server from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family MID Server release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading MID Server to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow-staging.fluidtopics.net/access?context=r_MIDServerSystemRequirements&family=yokohama&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow-staging.fluidtopics.net/access?context=mid-startup-fails&family=yokohama&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Zurich

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow-staging.fluidtopics.net/access?context=r_MIDServerSystemRequirements&family=zurich&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow-staging.fluidtopics.net/access?context=mid-startup-fails&family=zurich&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for MID Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[External Credential Storage and Management supports certificate-based authentication for Azure Key Vault](https://servicenow-staging.fluidtopics.net/access?context=mid-azure-key-vault-integration&family=yokohama&ft:locale=en-US)**

The External Credential Storage and Management added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ITOM Infra Services Workspace](https://servicenow-staging.fluidtopics.net/access?context=itom-infra-srv-wrksp-mid&family=zurich&ft:locale=en-US)**

The ITOM Infra Services Workspace provides a concise overview of MID Server activity. The dashboard integrates several previously disparate tables so that issues can be monitored and resolved. The workspace provides real-time monitoring, proactive alerts, automation of common tasks, and centralized diagnostics to reduce downtime and support tickets.

-   **[MID Guardian Agent](https://servicenow-staging.fluidtopics.net/access?context=mid-guardian&family=zurich&ft:locale=en-US)**

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem/ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. By intelligently analyzing logs, signals, and runtime behaviors, it offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing MID Server features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[MID Server supports and requires a minimum JRE version 17](https://servicenow-staging.fluidtopics.net/access?context=r_MIDServerSystemRequirements&family=yokohama&ft:locale=en-US)**

The MID Server is compiled using Java 17 and is incompatible with any Java version below 17 for runtime execution. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10. See the [MID Server JRE Minimum Version Requirement Update to JRE 17 Starting from Yokohama Release \[KB1704368\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704368) article in the Now Support Knowledge Base for information about required procedures before upgrading the instance.

-   **[Improvements when manually installing a MID Server on Windows](https://servicenow-staging.fluidtopics.net/access?context=mid-server-install-prereqs&family=yokohama&ft:locale=en-US)**

The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Smart Workload Manager in clusters](https://servicenow-staging.fluidtopics.net/access?context=t_ConfigureAMIDServerCluster&family=zurich&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[Enhancements to MID Server logging and JFR](https://servicenow-staging.fluidtopics.net/access?context=r_MIDServerTroubleshooting&family=zurich&ft:locale=en-US)**

MID Server logging has been improved with log backups that are preserved in a compressed format on local host with option to fetch to the instance. You can enable JFR logs every four hours and backup JFR files for a set time.

-   **[MID Server has improved performance during heavy discovery load](https://servicenow-staging.fluidtopics.net/access?context=r_MIDServerSystemRequirements&family=zurich&ft:locale=en-US)**

MID Servers no longer have performance degradation due to script include cache misses when using large amounts of worker threads.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some MID Server features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   When upgrading to the Yokohama release, 3DES will be permanently removed from MID Server to improve security. See [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950) for more information.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some MID Server features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

-   MID Server supports and requires a minimum JRE version 17. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10.
-   The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.

 See [MID Server](https://servicenow-staging.fluidtopics.net/access?context=mid-server-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.
-   MID Server logging has been improved with log backups that are preserved in a compressed format on a local host with an option to fetch to the instance.

 See [MID Server](https://servicenow-staging.fluidtopics.net/access?context=mid-server-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

