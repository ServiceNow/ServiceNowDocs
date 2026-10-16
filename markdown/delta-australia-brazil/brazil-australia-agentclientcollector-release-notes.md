---
title: Combined Agent Client Collector release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Agent Client Collector from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-agentclientcollector-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Agent Client Collector from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Brazil, new features were introduced for Agent Client Collector.

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

-   **[Discover portable software installed by package managers](https://www.servicenow.com/docs/access?context=accvc-package-discovery&family=brazil&ft:locale=en-US)**

Discover software installed on endpoints via package managers that isn't discoverable by traditional checks and policies.

-   **[Create a custom filter rule](https://www.servicenow.com/docs/access?context=create-custom-filter-rule&family=brazil&ft:locale=en-US)**

Create a custom software filter rule to exclude irrelevant entries from Discovery in your Software Asset Management \(SAM\) inventory.

-   **[Configure a license key discovery rule and write a parser script](https://www.servicenow.com/docs/access?context=configure-license-key-rule&family=brazil&ft:locale=en-US)**

Verify software legitimacy by creating license keys on your Windows, Linux and macOS devices.

-   **[Categorize software](https://www.servicenow.com/docs/access?context=acc-software-categorization&family=brazil&ft:locale=en-US)**

Use software categorization to group discovered software packages into business-relevant categories. Software categorization helps you avoid manually tagging software and provides administrative teams with an efficient inventory of software records.

-   **[Track software on Windows applications](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=brazil&ft:locale=en-US)**

Use improved software tracking on Windows applications. Software tracking informs you of the last time the application was used.

-   **[Require a maintenance token for Windows uninstalls](https://www.servicenow.com/docs/access?context=require-maintenance-token-uninstall&family=brazil&ft:locale=en-US)**

Require using a maintenance token when uninstalling an agent from a Windows device. A maintenance token provides a layer of protection so that unauthorized personnel can't perform the uninstall.

-   **[Enable a non-persistent virtual desktop infrastructure agent](https://www.servicenow.com/docs/access?context=enable-npvdi-agent&family=brazil&ft:locale=en-US)**

Configure an agent to enable it to work in a Virtual Desktop Infrastructure \(VDI\) environment. VDI agents gather data more quickly than traditional agents not enabled for a VDI.

-   **[Categorize discovered browser extensions and software packages](https://www.servicenow.com/docs/access?context=acc-categorize-discovered-software&family=brazil&ft:locale=en-US)**

Discover browser extensions and software packages by category. Categorization removes the need to tag software records manually and provides an accurate software inventory.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Agent Client Collector features.

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

-   **[View agent errors](https://www.servicenow.com/docs/access?context=view-agent-errors&family=brazil&ft:locale=en-US)**

Errors are now logged using the Error Framework application, instead of Service Error Management. Error Framework provides enhanced context and details for error entries, and error codes begin with the `SN-ACC` prefix.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Agent Client Collector features or functionality were removed.

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

Between your current release family and Brazil, some Agent Client Collector features or functionality were deprecated.

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

-   **UserAssist deprecation during SAM last-used metric collection**

The Windows `UserAssist` registry key is no longer used to determine the **last-used** timestamp for installed software. The **last-used** value is now derived from running-process snapshots collected by the existing SAM metering poll on the endpoint, with a Windows registry **Run** key used for auto-start applications.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Agent Client Collector.

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

-   **Activation information**

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.


**Note:** Agent Client Collector is available in the ServiceNow Store. For details, see the following activation information.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Agent Client Collector we have noted them here.

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

If any specific browser requirements were introduced or changed for Agent Client Collector we have noted them here.

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

Review details on accessibility information for Agent Client Collector, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Agent Client Collector we have noted them here.

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

-   **Localization information**

The current available languages for Agent Client Collector are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Agent Client Collector we have noted them here.

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

-   Monitor the performance and health of your infrastructure components.
-   Enable proactive management and troubleshooting of Configuration Items \(CIs\).
-   Identify characteristics of components running on your servers, as an alternative to horizontal, IP-based Discovery.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

