---
title: Combined MID Server release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for MID Server from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-midserver-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined MID Server release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for MID Server from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family MID Server release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading MID Server to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 21.0.7.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

    -   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
    -   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.
All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&family=australia&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

    -   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
    -   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for MID Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing MID Server features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[MID Server security logs require 100MB of storage](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US)**

To store the security logs, MID Servers must be installed on a host with at least 100MB of storage capacity.


 -   **[MID Server supports PowerShell 7 for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&family=australia&ft:locale=en-US)**

MID Server now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Configure the MID Server for CyberArk CCP](https://www.servicenow.com/docs/access?context=t_ConfigureTheMIDServerForCyberArkCCP&family=australia&ft:locale=en-US)**

MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices. This additional option can reduce dependency overhead and enables you to choose between the AIM SDK and REST-based approaches according to your requirements.

-   **[Smart Workload Manager in clusters](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&family=australia&ft:locale=en-US)**

MID Servers in a cluster now assign jobs based on the true load, using a variety of criteria. The smart workload manager continuously evaluates the queue size, execution time, CPU usage, and buffer size. The manager then assigns tasks to ensure that no server is overloaded.

-   **[MID Server is bundled with Java Runtime Environment 21](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US)**

MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10. The installer automatically configures Java 21.0.7 to run in your environment. If you have installed your own JRE, see the **Important information for upgrading MID Server to Australia** section to ensure your JRE is compatible.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some MID Server features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some MID Server features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

MID Server is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for MID Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   MID Server comes bundled with Java Runtime Environment version 21.0.7 and requires a minimum JRE version 17.0.10.
-   MID Server's CyberArk integration adds a REST-based CCP option alongside the existing AIM SDK method, providing flexible, interchangeable integration choices.
-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.

 See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

