---
title: Combined Agent Client Collector release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Agent Client Collector from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-agentclientcollector-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Agent Client Collector from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

Yokohama

</td><td>

-   **[Create tasks to address Agent Client Collector errors](https://www.servicenow.com/docs/access?context=create-error-task&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, create tasks to resolve errors relating to the Agent Client Collector. Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.

-   **[Use a proxy server with MID-less installation](https://www.servicenow.com/docs/access?context=acc-yml-options&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, enable using a proxy server when installing Agent Client Collector without a MID Server.

-   **[Discovery MSSQL server components](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=yokohama&ft:locale=en-US)**

Starting in version 1.3.0, enable discovery of MSSQL components by running Discovery as a local system user.

-   **[Java certification Discovery through file-based discovery](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=yokohama&ft:locale=en-US)**

Starting in version 1.3.0, discover java file information using Agent Client Collector for Visibility Content \(ACC-VC\) file based discovery. File based discovery locates java files that are installed on the system but not running, enabling retrieval of data used for licensing and auditing.

-   **[Enable high volume upgrade of agents](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, enhance efficiency by performing high-volume upgrade of large numbers of Agent Client Collector installations at once.


</td></tr><tr><td>

Zurich

</td><td>

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


 -   **[\[Placeholder link text to key gcp-config-file\]](https://www.servicenow.com/docs/access?context=gcp-config-file&family=zurich&ft:locale=en-US)**

Starting in version 3.15.0, GCP checks provide added support to configure metrics through a configuration file in JSON format.


 -   **[Run certificate Discovery using Agent Client Collector for Visibility Content](https://www.servicenow.com/docs/access?context=run-cert-discovery-accvc&family=zurich&ft:locale=en-US)**

Starting in version 1.3.0, use the Agent Client Collector for Visibility Content to discover TLS/SSL certificates used by the ports running on the server's configuration items \(CIs\). Certificate Inventory and Management uses the certificate data to manage the TLS/SSL certificate life cycle.

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

Yokohama

</td><td>

-   **[Explore metrics with Metric Explorer independent of Agent Client Collector Monitoring](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&family=yokohama&ft:locale=en-US)**

Starting in version 4.1.0, view and monitor metric data with Metric Explorer, even if you have not installed Agent Client Collector Monitoring.


</td></tr><tr><td>

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
</table>## Deprecations

Between your current release family and Australia, some Agent Client Collector features or functionality were deprecated.

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

Yokohama

</td><td>

-   **Activation information**

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

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

If any specific browser requirements were introduced or changed for Agent Client Collector we have noted them here.

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

If there are specific localization considerations for Agent Client Collector we have noted them here.

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

Yokohama

</td><td>

-   Agent Client Collector for Visibility: Starting in version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility Content. CNO for Visibility has been extracted from Agent Client Collector for Visibility Content and is now a separate application.
-   Store instance credentials in the Google Cloud Secret Manager when the Kubernetes Visibility Agent Informer uses Google Kubernetes Engine \(GKE\).
-   Use a custom CA to enable Kubernetes Visibility Agent Informer to communicate with the instance when using a custom root Certificate Authority \(CA\).
-   Configure Agent Client Collector without a MID Server by ßusing MID-less configuration.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Discover TLS/SSL certificates using Agent Client Collector for Visibility Content certificate Discovery.
-   Enhance data collection by disabling only those checks with high resource usage, allowing data collection to continue for other checks.
-   Improve troubleshooting capabilities by viewing errors that occur before and after the registration process in the ServiceNow instance.
-   Use file-based Discovery in a macOS environment.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

