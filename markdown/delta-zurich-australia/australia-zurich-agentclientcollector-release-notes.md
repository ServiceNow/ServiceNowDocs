---
title: Combined Agent Client Collector release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Agent Client Collector from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-agentclientcollector-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Agent Client Collector from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Agent Client Collector.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

**Agent Client Collector Framework**

-   **[Upgrade MID-less agents](https://www.servicenow.com/docs/access?context=upgrade-agent-from-instance&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, perform selective and high-volume upgrades on ACC agents when not using a MID Server by using products such as DEX and ACC-VC.

-   **[\[Placeholder link text to key verify-agent-functionality\]](https://www.servicenow.com/docs/access?context=verify-agent-functionality&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, verify that an agent is functioning properly by performing a self-test on the agent.

-   **[\[Placeholder link text to key acc-workspace-dashboard\]](https://www.servicenow.com/docs/access?context=acc-workspace-dashboard&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, view a list of agents and their statuses on the ACC Workspace dashboard.

-   **[Use improved debug logging](https://www.servicenow.com/docs/access?context=acc-configure-log-levels&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, benefit from enhanced debug logging by sending all debug statements to a log file

-   **[Manage Agent Client Collector certificates](https://www.servicenow.com/docs/access?context=acc-yml-options&family=zurich&ft:locale=en-US)**

Starting in version 5.0, configure a schedule by which to rotate Agent Client Collector certificates which enable communication between agents and ITOM Cloud Services. Rotating certificates ensures that when a certificate expires, a new certificate is in place.

-   **[Perform high-volume Agent Client Collector upgrade in a macOS environment](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&family=zurich&ft:locale=en-US)**

Starting in version 5.0, upgrade large numbers of Agent Client Collector agents at a time that are running on macOS. This extends the existing high-volume upgrade capabilities available for Windows and Linux in the 4.3.0 release.

-   **[Use an IMDSv2 endpoint for metadata discovery](https://www.servicenow.com/docs/access?context=acc-configure-websocket-endpoint&family=zurich&ft:locale=en-US)**

Starting in version 5.0, the IMDSv2 endpoint for metadata discovery is invoked when using Agent Client Collector in an AWS EC2 environment.

-   **[Use enhanced errors and diagnostics to troubleshoot issues with servers and endpoints](https://www.servicenow.com/docs/access?context=view-agent-errors&family=zurich&ft:locale=en-US)**

Starting in version 5.0, view errors that occur before or after the registration process when Agent Client Collector connects to the instance. This provides enhanced debugging capabilities by enabling you to view issues in the instance, without requiring direct access to the agent logs.

-   **[Disable checks using heavy system resources while in CPU protection mode](https://www.servicenow.com/docs/access?context=checks-policies&family=zurich&ft:locale=en-US)**

Starting in version 5.0, disable only those checks that are causing high CPU usage while in CPU protection mode. It is still possible to disable all checks and completely stop data collection while in CPU protection mode.

In a Windows environment, Agent Client Collector has improved the accuracy of how check CPU usage is monitored.

-   **[Configuration data files size limit](https://www.servicenow.com/docs/access?context=acc-config-data-files&family=zurich&ft:locale=en-US)**

Starting in version 5.0, configuration data files have a maximum size of 10MB.

-   **[Configure Agent Client Collector with proxy auto-configuration \(PAC\) files](https://www.servicenow.com/docs/access?context=proxy-agent&family=zurich&ft:locale=en-US)**

Starting in version 5.0, enable easier connection of Agent Client Collector to a proxy server by using a proxy auto-configuration \(PAC\) file.


 **Agent Client Collector Monitoring**

-   **[\[Placeholder link text to key gcp-config-file\]](https://www.servicenow.com/docs/access?context=gcp-config-file&family=zurich&ft:locale=en-US)**

Starting in version 3.15.0, GCP checks provide added support to configure metrics through a configuration file in JSON format.


-   **[Monitor Linux events](https://www.servicenow.com/docs/access?context=linux-checks-policies&family=zurich&ft:locale=en-US)**

Starting in version 3.15.0, monitor Linux events using Linux event checks.


 **Agent Client Collector for Visibility - Content**

-   **[Discover MSSQL components using ACC-VC](https://www.servicenow.com/docs/access?context=exploring-accv&family=zurich&ft:locale=en-US)**

Starting in version 1.5.0, use ACC-VC to discover MSSQL components in your environment.

-   **[Discover software information with ACC-VC using SWID tags](https://www.servicenow.com/docs/access?context=exploring-accv&family=zurich&ft:locale=en-US)**

Starting in version 1.5.0, gather software information with ACC-VC using software identification \(SWID\) tags on an agent and a ServiceNow® instance.

-   **[Run certificate Discovery using Agent Client Collector for Visibility - Content](https://www.servicenow.com/docs/access?context=run-cert-discovery-accvc&family=zurich&ft:locale=en-US)**

Starting in version 1.3.0, use the Agent Client Collector for Visibility - Content to discover TLS/SSL certificates used by the ports running on the server's configuration items \(CIs\). Certificate Inventory and Management uses the certificate data to manage the TLS/SSL certificate life cycle.

-   **[File-based Discovery is supported in a macOS environment](https://www.servicenow.com/docs/access?context=file-based-discovery&family=zurich&ft:locale=en-US)**

Starting in version 1.3.0, use File-based Discovery in a macOS environment.

-   **[Collect metrics using non-osqueryd data collection](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=zurich&ft:locale=en-US)**

Starting in version 1.3.0, collect data more efficiently by invoking non-osqueryd data collection.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Agent Client Collector features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Agent Client Collector features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Agent Client Collector features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Agent Client Collector Security Incident Response is no longer supported. For details on replacement options, see the [Deprecation guidance for Agent Client Collector Security Incident Response \[KB2249776\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249776) in the Now Support Knowledge Base.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Agent Client Collector.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Agent Client Collector we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Agent Client Collector we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Discover TLS/SSL certificates using Agent Client Collector for Visibility - Content certificate Discovery.
-   Enhance data collection by disabling only those checks with high resource usage, allowing data collection to continue for other checks.
-   Improve troubleshooting capabilities by viewing errors that occur before and after the registration process in the ServiceNow instance.
-   Use file-based Discovery in a macOS environment.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

