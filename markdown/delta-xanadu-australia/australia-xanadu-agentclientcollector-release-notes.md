---
title: Combined Agent Client Collector release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Agent Client Collector from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-agentclientcollector-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Agent Client Collector from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Australia, new features were introduced for Agent Client Collector.

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

-   **[Scan your resource directories for file attributes](https://www.servicenow.com/docs/access?context=directory-scan-checks-policies&family=yokohama&ft:locale=en-US)**

Starting in version 3.13.0, run a check to receive information on the directory file's integrity, size, space, response time, and age.

-   **[Conserve MID Server resources by using MID-less installation for Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-itom-cloud-services&family=yokohama&ft:locale=en-US)**

Starting in version 3.6.5, conserve MID Server resources for more persistent features by using the MID-less installation when installing Agent Client Collector. With this installation, you don't need a MID Server in your system architecture.

-   **[Create tasks to address Agent Client Collector errors](https://www.servicenow.com/docs/access?context=create-error-task&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, create tasks to resolve errors relating to the Agent Client Collector. Tasks are assigned to personnel who investigate the underlying issues and work to resolve the errors.

-   **[Use a proxy server with MID-less installation](https://www.servicenow.com/docs/access?context=acc-yml-options&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, enable using a proxy server when installing Agent Client Collector without a MID Server.

-   **[Discovery MSSQL server components](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=yokohama&ft:locale=en-US)**

Starting in version 1.3.0, enable discovery of MSSQL components by running Discovery as a local system user.

-   **[Java certification Discovery through file-based discovery](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&family=yokohama&ft:locale=en-US)**

Starting in version 1.3.0, discover java file information using Agent Client Collector for Visibility - Content \(ACC-VC\) file based discovery. File based discovery locates java files that are installed on the system but not running, enabling retrieval of data used for licensing and auditing.

-   **[Enable high volume upgrade of agents](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&family=yokohama&ft:locale=en-US)**

Starting in version 4.3.0, enhance efficiency by performing high-volume upgrade of large numbers of Agent Client Collector installations at once.

-   **[Block event creation for non-existent entities](https://www.servicenow.com/docs/access?context=prevent-events-nonexistent-entities&family=yokohama&ft:locale=en-US)**

Starting in version 3.13.0, block the creation of events and alerts if the process monitoring and log files don't exist in their indicated location.

-   **[Control how check results are sent](https://www.servicenow.com/docs/access?context=create-edit-policies&family=yokohama&ft:locale=en-US)**

Starting in version 3.6.5, configure the circumstances when check results are sent.

-   **[Configure and receive notifications of agent key expiration](https://www.servicenow.com/docs/access?context=agent-registration-key-configuration&family=yokohama&ft:locale=en-US)**

Starting in version 3.6.5, receive notifications that indicate when an agent registration key is expiring.

-   **[Monitor network host availability](https://www.servicenow.com/docs/access?context=network-host-availability-check&family=yokohama&ft:locale=en-US)**

Starting in version 4.1.0, use a new check to verify network host availability.

-   **[Identify software running on Linux and Windows devices](https://www.servicenow.com/docs/access?context=acc-visibility-checks-policies&family=yokohama&ft:locale=en-US)**

Starting in version 4.1.0, identify the software that is running on your Linux and Windows servers and devices by using file-based Discovery. File-based Discovery enables you to maintain the records of your software licenses and helps you to evaluate any threats from unwanted files.

-   **[Store ServiceNow instance credentials in the Google Cloud Secret Manager when the Informer uses Google Kubernetes Engine \(GKE\)](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=yokohama&ft:locale=en-US)**

If your organization uses Google Kubernetes Engine \(GKE\) you can store the secret in Google Cloud Secret Manager. The Kubernetes Visibility Agent Informer can then pull the ServiceNow credentials for accessing your instance from the Google Cloud Secret Manager.

-   **[Use a custom CA to enable the Informer to communicate with the ServiceNow instance when using a custom root CA](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=yokohama&ft:locale=en-US)**

Mount a custom certificate authority into the Kubernetes Visibility Agent Informer pod to enable the Informer to communicate with the instance when a custom root CA is used.


</td></tr><tr><td>

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

-   **[Explore metrics with Metric Explorer independent of Agent Client Collector Monitoring](https://www.servicenow.com/docs/access?context=agent-workspace-ops-intelligence&family=yokohama&ft:locale=en-US)**

Starting in version 4.1.0, view and monitor metric data with Metric Explorer, even if you have not installed Agent Client Collector Monitoring.

-   **[\[Placeholder link text to key acc-visibility-landing-page\]](https://www.servicenow.com/docs/access?context=acc-visibility-landing-page&family=yokohama&ft:locale=en-US)**

Starting in version 1.1.0, ACC for Visibility has been renamed as Kubernetes Visibility Agent and consists only of what is currently CNO for Visibility. The term CNO for Visibility has been deprecated and replaced with Kubernetes Visibility Agent. All other ACC for Visibility functions are now part of Agent Client Collector for Visibility - Content.


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
</table>## Deprecations

Between your current release family and Australia, some Agent Client Collector features or functionality were deprecated.

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

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

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

-   Agent Client Collector for Visibility: Starting in version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. CNO for Visibility has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Store instance credentials in the Google Cloud Secret Manager when the Kubernetes Visibility Agent Informer uses Google Kubernetes Engine \(GKE\).
-   Use a custom CA to enable Kubernetes Visibility Agent Informer to communicate with the instance when using a custom root Certificate Authority \(CA\).
-   Configure Agent Client Collector without a MID Server by ßusing MID-less configuration.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

