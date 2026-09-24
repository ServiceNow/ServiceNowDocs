---
title: Combined Agent Client Collector release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Agent Client Collector from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-agentclientcollector-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Agent Client Collector from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

Xanadu

</td><td>

-   **[Load the allow list only from a configuration file](https://www.servicenow.com/docs/access?context=acc-yml-options&family=xanadu&ft:locale=en-US)**

Enhance system security by loading the allow list from the file specified in the **allow-list** parameter of the configuration file while ignoring the allow lists that are bundled with the plugins.

-   **[Configure agent log level from the instance](https://www.servicenow.com/docs/access?context=set-agent-log-level&family=xanadu&ft:locale=en-US)**

Configure the agent log level from the ServiceNow instance without having to access the `acc.yml` configuration file.

-   **[Ensure secure agent connections](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&family=xanadu&ft:locale=en-US)**

Ensure that your agent connections are secure by adding a self-signed certificate to your operating system's truststore, which verifies that the certificate is authentic.

-   **[Update existing assets](https://www.servicenow.com/docs/access?context=agent-plugins-remove&family=xanadu&ft:locale=en-US)**

Update your Agent Client Collector \(ACC\) plugins to the latest version by removing your existing plugins before reinstalling.

-   **[Use expanded Linux and Windows checks](https://www.servicenow.com/docs/access?context=linux-checks-policies&family=xanadu&ft:locale=en-US)**

Enable enhanced check functionality by using the expanded Linux and Windows checks provided with the system.

-   **[Upgrade Agent Client Collector for Kubernetes – Visibility Informers remotely](https://www.servicenow.com/docs/access?context=cnov-informer-upgrade-remote&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, upgrade Informer pods in Kubernetes clusters remotely from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Override Informer parameters from the Instance](https://www.servicenow.com/docs/access?context=cnov-params-override&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, control CNO for Visibility Informer execution parameters from the ServiceNow instance to avoid dependence on your Kubernetes admin.

-   **[Store Instance credentials in Microsoft Azure Vault when Informer uses Azure Kubernetes Service \(AKS\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, if your organization uses AKS, you can store the secret in the Microsoft Azure Vault. The Informer then pulls the ServiceNow credentials for accessing your instance from the Azure Vault.

-   **[Enable Informer to connect to the instance using OAuth2.0 authorization](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, the Informer can use OAuth2.0 authorization to connect to the ServiceNow instance for enhanced security.

-   **[Enable expanded processing for the MID server on Network Interface Controllers \(NICs\) during keepalive operation](https://www.servicenow.com/docs/access?context=acc-yml-options&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, benefit from enhanced stability when running a keepalive operation by using the enhanced MID Server capability to configure the number of Network Interface Controllers \(NICs\) that can be monitored by a keepalive operation.

-   **[Upgrade Agent Client Collector manually on a macOS system](https://www.servicenow.com/docs/access?context=acc-macos-upgrade-manual&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, run the consolidated upgrade procedure manually for the Agent Client Collector in a macOS environment.

-   **[Configure the Dynatrace connector instance](https://www.servicenow.com/docs/access?context=configure-dynatrace-connector&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, Event Management supports collecting raw metric data collection using the Dynatrace metric connector

-   **[Consolidate agent errors](https://www.servicenow.com/docs/access?context=view-agent-errors&family=xanadu&ft:locale=en-US)**

Starting in version 4.1.0, view errors for all agents on the Agent Error Messages page. Additionally, you can view errors per individual agent by selecting the agent and selecting the **ACC Error Messages** tab .

-   **[Use Linux commands to enable additional system capabilities beyond your permission level](https://www.servicenow.com/docs/access?context=acc-installation&family=xanadu&ft:locale=en-US)**

Starting in version 4.1.0, use Linux commands to grant enhanced permissions, which are enabled once the installation `.exe` file is executed. These enhanced capabilities are provided securely, ensuring that there is no security risk to your environment.

-   **[Use the new Windows event check for enhanced event details](https://www.servicenow.com/docs/access?context=windows-checks-policies&family=xanadu&ft:locale=en-US)**

Starting in version 3.12.0, use the new Windows event check to collect and filter Windows event logs.

-   **[Use the network port check to determine port availability](https://www.servicenow.com/docs/access?context=network-port-checks-policies&family=xanadu&ft:locale=en-US)**

Starting in version 3.12.0, use the Network port check to create events for all ports of a specified host address, which indicates whether each port is available or in use.

-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Store ServiceNow instance credentials in the Google Cloud Secret Manager when the Informer uses Google Kubernetes Engine \(GKE\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=yokohama&ft:locale=en-US)**

If your organization uses Google Kubernetes Engine \(GKE\) you can store the secret in Google Cloud Secret Manager. The Kubernetes Visibility Agent Informer can then pull the ServiceNow credentials for accessing your instance from the Google Cloud Secret Manager.

-   **[Use a custom CA to enable the Informer to communicate with the ServiceNow instance when using a custom root CA](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=yokohama&ft:locale=en-US)**

Mount a custom certificate authority into the Kubernetes Visibility Agent Informer pod to enable the Informer to communicate with the instance when a custom root CA is used.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Upgrade MID-less agents](https://www.servicenow.com/docs/access?context=upgrade-agent-from-instance&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, perform selective and high-volume upgrades on ACC agents when not using a MID Server by using products such as DEX and ACC-VC.

-   **[\[Placeholder link text to key verify-agent-functionality\]](https://www.servicenow.com/docs/access?context=verify-agent-functionality&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, verify that an agent is functioning properly by performing a self-test on the agent.

-   **[\[Placeholder link text to key acc-workspace-dashboard\]](https://www.servicenow.com/docs/access?context=acc-workspace-dashboard&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, view a list of agents and their statuses on the ACC Workspace dashboard.


 -   **[Monitor Linux events](https://www.servicenow.com/docs/access?context=linux-checks-policies&family=zurich&ft:locale=en-US)**

Starting in version 3.15.0, monitor Linux events using Linux event checks.


 -   **[Discover MSSQL components using ACC-VC](https://www.servicenow.com/docs/access?context=exploring-accv&family=zurich&ft:locale=en-US)**

Starting in version 1.5.0, use ACC-VC to discover MSSQL components in your environment.

-   **[Discover software information with ACC-VC using SWID tags](https://www.servicenow.com/docs/access?context=exploring-accv&family=zurich&ft:locale=en-US)**

Starting in version 1.5.0, gather software information with ACC-VC using software identification \(SWID\) tags on an agent and a ServiceNow® instance.


</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[Use the updated Windows event check](https://www.servicenow.com/docs/access?context=windows-checks-policies&family=xanadu&ft:locale=en-US)**

Starting in version 3.12.0, the Windows event check `os.windows.check-event-log` has been renamed `os.windows.check-event-log-count` and has enhanced data gathering capabilities.


-   **Updated plugin dependency**

Starting in version 4.1.0, the Service Error Management plugin is dependent on the ACC-F scoped app. The plugin gets installed automatically when the customer installs the ACC-F scoped app from the ServiceNow store.

-   **[New allow list parameter for checks running in shell execution mode](https://www.servicenow.com/docs/access?context=check-definition-form&family=xanadu&ft:locale=en-US)**

Starting in version 4.1.0, when running a check in with execution mode \(**Exec Mode**\) set to **shell**, add the **allow\_shell** parameter and set it to **true** for the allow list entry corresponding to the check.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[\[Placeholder link text to key acc-visibility-landing-page\]](https://www.servicenow.com/docs/access?context=acc-visibility-landing-page&family=yokohama&ft:locale=en-US)**

Starting in version 1.1.0, ACC for Visibility has been renamed as Kubernetes Visibility Agent and consists only of what is currently CNO for Visibility. The term CNO for Visibility has been deprecated and replaced with Kubernetes Visibility Agent. All other ACC for Visibility functions are now part of Agent Client Collector for Visibility Content.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Agent Client Collector features or functionality were removed.

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

Agent Client Collector Security Incident Response is no longer supported. For details on replacement options, see the [Deprecation guidance for Agent Client Collector Security Incident Response \[KB2249776\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249776) in the Now Support Knowledge Base.

</td></tr><tr><td>

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

Xanadu

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

-   Ensure secure agent connections by adding a self-signed certificate.
-   Enhance check functionality by using expanded Linux and Windows checks, enabling you to gather additional information on your Linux and Windows servers.
-   Upgrade the Cloud Native Operations for Visibility Informer from the ServiceNow instance.
-   Store Instance credentials in the Microsoft Azure Vault when Informer uses Azure Kubernetes Engine \(AKS\).
-   Enjoy multi-architecture support for docker image.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

