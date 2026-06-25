---
title: Combined ITOM Visibility release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for ITOM Visibility from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-itomvisibility-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined ITOM Visibility release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for ITOM Visibility from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM Visibility release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM Visibility to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

For an improved Service Mapping experience, install Service Mapping Plus version 1.13.0 from the ServiceNow® Store.

 Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

</td></tr><tr><td>

Yokohama

</td><td>

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

 After upgrading to Yokohama, a Fix Script named "Add Explicit Public SNMP Credential" might create a public SNMP credential in Production instances. This could lead to unnecessary records via Discovery. The Fix Script is present in Yokohama instances, including OOB. Before applying the upgrade of Discovery core, Yokohama version, verify the fix script behavior in a sandbox environment. Remove the public SNMP credentials if not required.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use Discovery Admin Workspace features to jumpstart discovery implementation.](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&family=xanadu&ft:locale=en-US)**
    -   View discovery trends and tasks and access relevant ITOM Visibility apps and information through Discovery Admin Workspace Home.
    -   Gain insights into the performance of all your discoveries through the information in the **Schedules** tab.
    -   Analyze discovery errors and troubleshoot them using information in the **Diagnostics** tab.
    -   Access on-demand reports and optimize discovery operations using information in the**Insights** tab.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Discover the following products through Discovery and Service Mapping Patterns:

    -   [Dell EMC Data Domain storage](https://www.servicenow.com/docs/access?context=emc-data-domain-pattern&family=xanadu&ft:locale=en-US).
    -   [Dell EMC PowerMax storage](https://www.servicenow.com/docs/access?context=emc-powermax-discovery-pattern&family=xanadu&ft:locale=en-US).
    -   [AWS services in the China region](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\) on the ServiceNow AI Platform Xanadu Patch 3 instance.
    -   [REST-based Fortinet firewall and FortiGate VDOMs](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\).
    -   [Azure Marketplace](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\). The pattern supports the discovery of the following Azure Marketplace products:
        -   Virtual Machine
        -   SaaS
        -   Azure Application
-   **[Oracle Java process discovery](https://www.servicenow.com/docs/access?context=oracle-glas-discovery&family=xanadu&ft:locale=en-US)**

Discover Java processes to comply with Oracle licensing agreements- Use the ITOM Oracle GLAS plugin \(1.8.4\) November 2024 store version to track Java installations and usage.

-   **[MID Server features for better discovery performance](https://www.servicenow.com/docs/access?context=mid-server-rn&family=xanadu&ft:locale=en-US)**
    -   Run other applications without storing any credentials on the instance with the Microsoft Azure Key vault.
    -   MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode isn't enabled out of the box.
-   **[Use CMDB based mapping to create new application services](https://www.servicenow.com/docs/access?context=cmdb-based-mapping&family=xanadu&ft:locale=en-US)**

Use Automated Service Suggestions and CMDB data instead of the MID Server, to create new application services.

-   **[Use the latest CNO for Visibility features](https://www.servicenow.com/docs/access?context=cnov-configuring&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, benefit from new features in Cloud Native Operations for Visibility.

    -   Upgrade the CNO for Visibility Informer from the ServiceNow instance.
    -   Control Informer execution parameters from the instance.
    -   Store instance credentials in the Microsoft Azure Vault when Informer uses the Azure Kubernetes Engine \(AKS\)
    -   Enable Informer to connect to the instance using OAuth2.0 authorization
-   **[Enjoy multi-architecture support for docker image](https://www.servicenow.com/docs/access?context=cnov-deploy-prepare&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://www.servicenow.com/docs/access?context=cnov-params-override&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://www.servicenow.com/docs/access?context=cnov-deploy-install&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.

-   **[Use Service Fingerprints to refine the selection of application service candidates](https://www.servicenow.com/docs/access?context=auto-serv-suggest&family=xanadu&ft:locale=en-US)**

Explore unique, classified components of application service candidates provided by Automated Service Suggestions. By supplying specific information such as the product name and description, gain deeper insights into the most suitable candidate to convert to an application service.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Discover additional AWS Services using Patterns](https://www.servicenow.com/docs/access?context=aws-service-discovery-pattern&family=yokohama&ft:locale=en-US)**
    -   Starting with store version 1.25.0, Discovery and Service Mapping Patterns discovers 27 additional AWS cloud services.
    -   Starting with store version 1.27.0, Discovery and Service Mapping Patterns discovers 7 additional AWS cloud services.
-   **[Discover products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=available-patterns&family=yokohama&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.27.0:

    -   [NVIDIA GPUs](https://www.servicenow.com/docs/access?context=nvidia-gpu-discovery-pattern&family=yokohama&ft:locale=en-US)
    -   [Microsoft SQL Always On availability groups](https://www.servicenow.com/docs/access?context=mssql-data-collected-pattern&family=yokohama&ft:locale=en-US)
    -   [Azure tenants and management groups](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS Application Load Balancer targets](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS web ACL](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS Systems Manager \(SSM\) agents](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [Tag collection for Azure VM instance - Uniform scale set](https://www.servicenow.com/docs/access?context=AzureVMScaleSetInstance&family=yokohama&ft:locale=en-US)
-   **[Automatically generate a Certificate Signing Request](https://www.servicenow.com/docs/access?context=request-new-csr-automated&family=yokohama&ft:locale=en-US)**

Generate a Certificate Signing Request and a private key with the Employee Center experience, starting with version 3.6.0 of Certificate Inventory and Management.

-   **[Use Service Graph Connectors for extended discovery](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&family=yokohama&ft:locale=en-US)**

Service Graph Connectors are a collection of predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources.

    -   Discover device details from Chromebook and ingest them into the CMDB by using Service Graph Connector for Google Console store version 1.8.
    -   Discover data from public cloud instances and resources in AWS, Azure, and GCP environments and ingest them into the CMDB by using Service Graph Connector for Wiz. 
-   **[Detect anomalies in Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-diagnostics&family=yokohama&ft:locale=en-US)**

Starting with Discovery Admin Workspace version 1.8.0, machine learning \(ML\) or statistical methods can detect anomalies in Discovery schedules and display this data in dashboards for admins. It identifies unusual behaviors like failed runs, significant deviations from user-defined thresholds for high error counts, longer discovery status duration, and fewer discovered Configuration Items \(CIs\) or Cloud resources. The ML-based approach to this feature is enabled by default. Thresholds are configurable via the new Settings page, and the results will be shown throughout the workspace.

-   **[Cloud-based Discovery schedules](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-schedules&family=yokohama&ft:locale=en-US)**

Starting with version 1.8.0, Cloud-based discovery scheduling and reporting is available in Discovery Admin Workspace.

-   **[Configure Discovery to use Event Framework](https://www.servicenow.com/docs/access?context=t_ConfigureDiscoveryEventFramework&family=yokohama&ft:locale=en-US)**

Starting with version 1.9.0, Discovery jobs can be configured to use an event-based system, reducing database activity by queuing and processing events at regular intervals with priority and memory monitoring.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing ITOM Visibility features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use the enhanced Shazzam probe to collect data](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-insights&family=xanadu&ft:locale=en-US)**

View the extended data collected by the Shazzam probe in the Discovery Admin Workspace **Insights** tab.

-   **[Revised Service Mapping roles](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&family=xanadu&ft:locale=en-US)**

Gain improved visibility of ML-powered candidates in Service Mapping with updated roles:

    -   service\_mapping\_admin replaces sm\_admin.
    -   service\_mapping\_user replaces sm\_user.
-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://www.servicenow.com/docs/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Note the following new Pattern extensions and improvements:

    -   [Pure Storage FlashArray](https://www.servicenow.com/docs/access?context=flasharray-discovery&family=xanadu&ft:locale=en-US)
    -   [Azure SQL license information](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&family=xanadu&ft:locale=en-US)
    -   [GCP asset inventory](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&family=xanadu&ft:locale=en-US)
-   **[Scale up your Azure change processing](https://www.servicenow.com/docs/access?context=azure-change-processing&family=xanadu&ft:locale=en-US)**

Update your CMDB in real time with your Azure cloud resource changes. After upgrading to the enhanced November 2024 Patterns \(1.21.0\) version, run an Azure cloud discovery on all service accounts to ensure receiving all updates.

-   **[Stay informed about Cloud Discovery patterns updates](https://www.servicenow.com/docs/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Download and use the Cloud Discovery patterns spreadsheet with the latest up-to-date information on Cloud Discovery patterns, including REST-API permissions.

-   **[Run top-down discovery using Service Mapping integrated with Agent Client Collector](https://www.servicenow.com/docs/access?context=service-mapping-with-acc&family=xanadu&ft:locale=en-US)**

Top-down Service Mapping and Automated Service Suggestions are supported with Agent Client Collector.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Name suggestions for application service candidates](https://www.servicenow.com/docs/access?context=app-services-name-suggestions&family=yokohama&ft:locale=en-US)**

Experience more accurate name suggestions for application service candidates based on Service Fingerprints in Service Mapping Plus store version 1.15.0.

-   **[Limits in Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&family=yokohama&ft:locale=en-US)**

Limits in Service Mapping prevent the disabling or deletion of jobs scheduled for the Checkpoint Reaper or the Service Model's Blob Reaper.

-   **[Limits in tag-based Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping-plus&family=yokohama&ft:locale=en-US)**

Starting with version 1.15.2, experience improved performance in Service Mapping. A new property limits the creation of tag-based service candidates to 200 per service family.

-   **[Name update in Service Mapping](https://www.servicenow.com/docs/access?context=create-it-services&family=yokohama&ft:locale=en-US)**
    -   Application Services in the navigation menu has been renamed Service Instances.
    -   The label for the \[cmdb\_ci\_service\_auto\] table has been changed from Application Service to Service Instance.
-   **[Discovery status monitoring](https://www.servicenow.com/docs/access?context=c_DiscoveryStatus&family=yokohama&ft:locale=en-US)**

Discovery schedules that have no status updates for over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some ITOM Visibility features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some ITOM Visibility features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Starting with the Xanadu release, the Discovery Dashboard is no longer part of the Discovery plugin. Use [Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&family=xanadu&ft:locale=en-US) instead.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Application/Plugin Deprecation Process \[KB0867184\]Discovery CLI](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)**

Starting with version 3.5.0, Discovery CLI is no longer available in the Pattern Designer Enhancements Store App.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=xanadu&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=xanadu&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr><tr><td>

Yokohama

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=yokohama&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=yokohama&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM Visibility we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ITOM Visibility we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ITOM Visibility, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ITOM Visibility we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ITOM Visibility we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Elevate the Discovery Admin experience with Discovery Admin Workspace. Benefit from a unified workspace for configuring Discovery, tracking progress, and managing errors, with diagnostic tools that provide insights into discovered data.
-   Enrich your CMDB with a larger number of configuration items using ITOM Content Service.
-   Create application services with CMDB based mapping.
-   Avoid dependence on your Kubernetes admin by upgrading Cloud Native Operations Informer pods and modifying Informer execution parameters directly from the instance.
-   Enjoy multi-architecture support for docker image in Cloud Native Operations for Visibility.

 See [IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Discovery and Service Mapping Patterns: Gain enhanced visibility into your AWS cloud services with 27 additional patterns starting with store version 1.25.0.
-   Starting with store version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. The CNO for Visibility feature has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Starting with Service Graph Connector for GCP store release 1.8, Service Graph Connector for AWS store release 2.9, and Service Graph Connector for Microsoft Azure store release 1.11, you can use Service Graph Connectors to ingest data into the Configuration Management Database \(CMDB\) from third-party sources.
-   Starting with store version 1.8.0, Discovery admins gain improved visibility into discovery issues and can address root causes using anomaly detection in the Discovery Admin Workspace.

 See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

