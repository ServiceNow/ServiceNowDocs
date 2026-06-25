---
title: Combined Agent Client Collector release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Agent Client Collector from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-agentclientcollector-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Agent Client Collector release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Agent Client Collector from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Agent Client Collector release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Agent Client Collector to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Agent Client Collector.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Using metric connector enhancements](https://www.servicenow.com/docs/access?context=operational-metrics&family=washingtondc&ft:locale=en-US)**

Use agent-less System Center Operations Manager \(SCOM\) connectors for high-performance SCOM metric integration.

-   **[Application patterns for the Agent Client Collector](https://www.servicenow.com/docs/access?context=application-patterns-acc&family=washingtondc&ft:locale=en-US)**

Run application patterns through the Agent Client Collector. Application patterns enable discovering details about applications running on an agent’s host.

-   **[Enhanced system properties](https://www.servicenow.com/docs/access?context=acc-policy-collection-properties&family=washingtondc&ft:locale=en-US)**

Monitor the behavior of the Agent Client Collector application with the enhanced Policy Calculation and Framework Configuration system properties, including the enhancements to agent Discovery, automatic MID Server selection, and error message logging.

-   **[Configuration data files added to checks](https://www.servicenow.com/docs/access?context=acc-config-data-files&family=washingtondc&ft:locale=en-US)**

Provide the enhanced data collection in the Agent Client Collector application by communicating the instance data with the agent. The configuration data files are also sent to the agent’s associated MID Server.

-   **[Mongo DB checks](https://www.servicenow.com/docs/access?context=mongodb-checks-policies&family=washingtondc&ft:locale=en-US)**

Monitor MongoDB resources with additional metrics that relate to the metadata, memory, and disk space.

-   **[Continuously discover the resources in your Kubernetes clusters](https://www.servicenow.com/docs/access?context=cnov-exploring&family=washingtondc&ft:locale=en-US)**

Continuously discover the resources in your Kubernetes clusters in Agent Client Collector for Visibility by using Cloud Native Operations \(CNO\) for Visibility. CNO for Visibility promptly reports changes in the resources to the instance and updates the Configuration Management Database \(CMDB\).

-   **[Retrieving the metrics for cloud resources](https://www.servicenow.com/docs/access?context=agent-policies-checks&family=washingtondc&ft:locale=en-US)**

Retrieve the high-performance metrics for virtual resources in the cloud by using VMware.

-   **[Pull additional resources from Kubernetes clusters into the CMDB](https://www.servicenow.com/docs/access?context=cnov-config-pulling-extra-resources&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, configure the Cloud Native Operations for Visibility Informer to pull additional resources from Kubernetes clusters into the Configuration Management Database \(CMDB\), besides the resources it sends to the database by default.

-   **[Create a cmdb\_ci\_linux\_server CI for each Kubernetes node](https://www.servicenow.com/docs/access?context=cnov-config-linux-server-ci&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, configure if you want the CNO for Visibility Informer to create a cmdb\_ci\_linux\_server CI for each Kubernetes node. By default, the Informer creates a cmdb\_ci\_linux\_server CI for every Kubernetes node. If this CI is redundant or interferes with other flows in your organization, you can set the associated configuration parameter to false.

-   **[Define include and exclude lists of Labels and Annotations](https://www.servicenow.com/docs/access?context=cnov-config-annotations-allowed&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, define include and exclude lists of Labels and Annotations in Kubernetes resources that the CNO for Visibility Informer pulls into the CMDB.

-   **[Display the Kubernetes cluster version in the CMDB](https://www.servicenow.com/docs/access?context=cnov-config-see-cluster-version&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, make the CNO for Visibility Informer populate the field in the cmdb\_ci\_kubernetes\_cluster CI that shows the Kubernetes cluster version.

-   **[Add custom Labels and Annotations to Kubernetes resources](https://www.servicenow.com/docs/access?context=cnov-config-add-custom-labels&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, CNO for Visibility enables you to add custom Labels and Annotations to all your resources deployed in the Kubernetes cluster.

-   **[Secure check verification through the allow-list](https://www.servicenow.com/docs/access?context=acc-yml-options&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, enhance your system's security by verifying checks only with the allow-list from your global configurations. An allow-list from installed plugins is not used.

-   **[Add a self-signed certificate to your operating system's truststore](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, enhance security by adding a self-signed certificate to your OS's trust store.

-   **[Clear agent assets](https://www.servicenow.com/docs/access?context=agent-plugins-remove&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, remove an agent's plugin files by selecting **Clear Assets** on the UI, instead of removing the plugins manually.

-   **[New Linux and Windows checks supported](https://www.servicenow.com/docs/access?context=agent-policies-checks&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, Agent Client Collector supports additional Linux and Windows checks.


</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Agent Client Collector features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Automatic MID Server selection](https://www.servicenow.com/docs/access?context=acc-auto-mid-selection&family=washingtondc&ft:locale=en-US)**
    -   Receive additional MID Server information to be used as alternative points of communication during automatic MID Server selection.
    -   Automatic MID Server selection is off by default.
-   **[Metric rules](https://www.servicenow.com/docs/access?context=create-metric-rules&family=washingtondc&ft:locale=en-US)**

Configure manual thresholds for generating metric alerts using the Metric Rules feature instead of the Static Thresholds UI.

-   **[Retrieving the metrics for cloud resources](https://www.servicenow.com/docs/access?context=azure-checks-policies&family=washingtondc&ft:locale=en-US)**

Use Azure checks and policies to retrieve high-performance metrics for the virtual resources in the cloud.

-   **[Monitoring Technology Dashboards](https://www.servicenow.com/docs/access?context=monitor-tech-dashboard-concept&family=washingtondc&ft:locale=en-US)**
    -   Filter metrics by the selected configuration item \(CI\) in the AWS and GCP Monitoring Technology Dashboards.
    -   Use the updated Monitoring Technology Dashboard for Azure. The dashboard contains additional tabs which provide more information on your Azure infrastructure.
    -   Viewing Monitoring Technology Dashboards requires the dashboard\_admin role in addition to the existing agent\_client\_collector\_admin role.
-   **[Agent table cleaner](https://www.servicenow.com/docs/access?context=acc-installation&family=washingtondc&ft:locale=en-US)**

Delete the agent records that have been disconnected or inactive for more than 30 days by using the Autoflush form.

-   **[SNMP checks](https://www.servicenow.com/docs/access?context=agent-policies-checks&family=washingtondc&ft:locale=en-US)**

SNMP checks work by default with v3.

-   **[Set the agent log level](https://www.servicenow.com/docs/access?context=set-agent-log-level&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, configure the agent log level through the ServiceNow® instance, without needing to access the `acc.yml` configuration file.

-   **[Host system requirements for Agent Client Collector Monitoring](https://www.servicenow.com/docs/access?context=acc-installation&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, utilize the updated minimum host system requirements when installing Agent Client Collector Monitoring.

-   **[Import a script include to enable using the Instance scan](https://www.servicenow.com/docs/access?context=hs-landing-page&family=washingtondc&ft:locale=en-US)**

Starting in version 3.5.1, import **global.ACCInstanceScanUtil** to enable using the Instance scan feature, as described in the [KB1630132](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1630132) knowledge base article.


</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Agent Client Collector features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Agent Client Collector features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

Xanadu

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

Yokohama

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Agent Client Collector we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Washington DC

</td><td>

-   Use the enhanced system properties for agent Discovery, automatic MID Server selection, and error message logging to monitor the Agent Client Collector policies and framework configuration.
-   Use the configuration data files to provide the data from an instance directly to an agent.
-   Retrieve the metrics for Azure policies in the cloud.

 See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

