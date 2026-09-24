---
title: Combined ITOM Visibility release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ITOM Visibility from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-itomvisibility-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined ITOM Visibility release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ITOM Visibility from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM Visibility release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM Visibility to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

-   **Upgrade information**

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

After upgrading to Yokohama, a Fix Script named "Add Explicit Public SNMP Credential" might create a public SNMP credential in Production instances. This could lead to unnecessary records via Discovery. The Fix Script is present in Yokohama instances, including OOB. Before applying the upgrade of Discovery core, Yokohama version, verify the fix script behavior in a sandbox environment. Remove the public SNMP credentials if not required.


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

Between your current release family and Brazil, new features were introduced for ITOM Visibility.

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

-   **[Configure Discovery to use Event Framework](https://www.servicenow.com/docs/access?context=t_ConfigureDiscoveryEventFramework&family=yokohama&ft:locale=en-US)**

Starting with version 1.9.0, Discovery jobs can be configured to use an event-based system, reducing database activity by queuing and processing events at regular intervals with priority and memory monitoring.


</td></tr><tr><td>

Zurich

</td><td>

-   **[AI-Powered Service Mapping](https://www.servicenow.com/docs/access?context=ai-workflows-service-mapping&family=zurich&ft:locale=en-US)**
    -   Two AI Agents automatically generate service maps from ML candidates and connect Business Applications to discovered Application Services, eliminating manual CSDM relationship maintenance at scale. Available starting with Zurich Patch 9.
    -   Use the Service Mapping MCP tools to query live service topology, relationships, and CI data through a conversational interface via Claude Desktop. Available starting with Zurich Patch 10.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ITOM Visibility features.

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
    -   [GCP resource inventory](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&family=xanadu&ft:locale=en-US)
-   **[Scale up your Azure change processing](https://www.servicenow.com/docs/access?context=azure-change-processing&family=xanadu&ft:locale=en-US)**

Update your CMDB in real time with your Azure cloud resource changes. After upgrading to the enhanced November 2024 Patterns \(1.21.0\) version, run an Azure cloud discovery on all service accounts to ensure receiving all updates.

-   **[Stay informed about Cloud Discovery patterns updates](https://www.servicenow.com/docs/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Download and use the Cloud Discovery patterns spreadsheet with the latest up-to-date information on Cloud Discovery patterns, including REST-API permissions.

-   **[Run top-down discovery using Service Mapping integrated with Agent Client Collector](https://www.servicenow.com/docs/access?context=service-mapping-with-acc&family=xanadu&ft:locale=en-US)**

Top-down Service Mapping and Automated Service Suggestions are supported with Agent Client Collector.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Limits in tag-based Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping-plus&family=yokohama&ft:locale=en-US)**

Starting with version 1.15.2, experience improved performance in Service Mapping. A new property limits the creation of tag-based service candidates to 200 per service family.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Automated certificate renewal](https://www.servicenow.com/docs/access?context=automated-certificate-renewal&family=zurich&ft:locale=en-US)**

Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


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

Between your current release family and Brazil, some ITOM Visibility features or functionality were removed.

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

Between your current release family and Brazil, some ITOM Visibility features or functionality were deprecated.

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


</td></tr><tr><td>

Zurich

</td><td>

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

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

-   **Activation information**

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=yokohama&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=yokohama&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=zurich&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=zurich&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version-history release notes.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=australia&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=australia&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store..


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=brazil&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=brazil&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store. ITOM Visibility installation is also available in the ITOM Product Hub for ServiceNow Otto users.For more information, see [Install ITOM Visibility](https://www.servicenow.com/docs/access?context=install-nowassist-setup-itom-visibility&family=brazil&ft:locale=en-US)


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

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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
-   Starting with store version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility Content. The CNO for Visibility feature has been extracted from Agent Client Collector for Visibility Content and is now a separate application.
-   Starting with Service Graph Connector for GCP store release 1.8, Service Graph Connector for AWS store release 2.9, and Service Graph Connector for Microsoft Azure store release 1.11, you can use Service Graph Connectors to ingest data into the Configuration Management Database \(CMDB\) from third-party sources.
-   Starting with store version 1.8.0, Discovery admins gain improved visibility into discovery issues and can address root causes using anomaly detection in the Discovery Admin Workspace.

 See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Cloud-based scheduling available in Discovery Admin Workspace \(store version 1.11.0\).
-   AWS EC2 VMs discovery using AWS Systems Manager \(SSM\).
-   Tag-based Service Mapping experience in the Service Mapping Workspace \(store version 1.16.3\).
-   Application service maps for containers via Kubernetes Visibility Agent \(KVA\) \(store version 3.11.0\).
-   25 cloud patterns shipped via Discovery and Service Mapping Patterns \(store version 1.28.0\)
-   Certificate Inventory and Management TLS Certificate request flows that support Keyfactor EJBCA \(store version 3.7.0\) and Certificate Inventory and Management Automated TLS Certificate renewal workflows \(store version 3.8.2\).

 See [IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Discovery: Power Shell 7 support for Discovery.
-   Kubernetes Visibility Agent \(KVA\) and Service Mapping: Create service maps for extended services beyond Kubernetes.
-   AI Agent Topology Mapping: Discover AI agent infrastructure and dependencies using the new AI Agent Topology Mapping application, including:
    -   Amazon Bedrock AI agents, models, and prompts
    -   Microsoft Foundry \(Classic\) AI agents, models, and prompts
-   Cryptographic Asset Compliance: Inventory, assess, and manage cryptographic assets, including certificates and keys, across cloud and on-premises environments to support post-quantum cryptography \(PQC\) readiness and maintain security compliance.

 -   **[Store updates for ITOM Visibility](https://www.servicenow.com/docs/access?context=store-rn-itom-visibility-landing&family=australia&ft:locale=en-US)**

The majority of Visibility apps are updated monthly or quarterly via the ServiceNow Store. The latest updates are available in the ServiceNow Store. For cumulative release notes and compatibility information, see the ServiceNow Store version details.

    -   [Cryptographic Asset Compliance](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-advanced.html)

Cryptographic Asset Compliance is a part of the ITOM - Advanced app. This app helps you manage cryptographic assets, including certificates and cloud keys \(AWS KMS and Azure Key Vault\) discovered across on-premises and cloud environments from a centralized inventory. You can identify at-risk cryptographic assets with policy-based risk indicators and focus remediation efforts where they matter most.

    -   [Service Mapping Plus](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-mapping-plus.html)

Multi-Source Service Mapping – gain a single, trusted view of your services by eliminating fragmented maps and blind spots across discovery and service mapping methods. Unify top-down, tag-based, and ML-powered services into composite service maps.

    -   [AI-Powered Service Mapping](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html)

Two AI Agents automatically generate service maps from ML candidates and connect Business Applications to discovered Application Services, eliminating manual CSDM relationship maintenance at scale. Available starting with Australia Patch 2.

Use the Service Mapping MCP tools to query live service topology, relationships, and CI data through a conversational interface via Claude Desktop. Available starting with Australia Patch 3.

    -   [Discovery Admin Workspace](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-discovery-admin-workspace.html)

Expanded Cloud support to include Alibaba, IBM, OCI, OpenStack, oVirt, and Vmware. New dashboards: URL Discovery Insights, Discovery Operations Monitor. Create discovery schedules automatically using integration with IP Address Management \(IPAM\) systems. Create discovery schedules for multi-cloud deployments. Improve security posture for Discovery. Receive real-time alerts including Discovery Schedule failures, Anomaly detection, MID down and Automated discovery schedule in Microsoft Teams and Outlook. Improve security posture for Discovery.

    -   [Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-patterns.html)

New CI classes and fields for NSX infrastructure. Scan container repositories not reachable through a proxy using the new system property "sn\_itom\_pattern.container\_image\_scan\_no\_proxy". Container image scanning now supports MID Server selection per datacenter for private repositories. Multiple fixes and improvements for patterns for cloud and on premise discovery.

    -   [Certificate Inventory and Management](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cert-inv-mgmt.html)

Seamless certificate renewal via Microsoft Outlook and CMDB Data Certification for TLS certificates.

    -   [Kubernetes Visibility Agent](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-kubernetes-visibility-agent.html) and [Agent Client Collector for Visibility](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-visibility.html)

Increase visibility and control over Kubernetes environments: Service maps for Kubernetes and all related service resources, service maps for micro-services, KubeVirt VMs added to the CMDB, CI visualization. KVA is supported in OKE \(Oracle Kubernetes Engine\).

    -   [Service Graph Connector for AWS](https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-aws.html)
    -   [Service Graph Connector for Microsoft Azure](https://www.servicenow.com/docs/r/store-release-notes/store/platform-c/store-platcap-rn-service-graph-connector-ms-azure.html)

Resource types aren't dynamically populated in the allowlist.

    -   [Service Graph Connector for GCP](https://www.servicenow.com/docs/r/store-release-notes/page/release-notes/store/platform-capabilities/store-platcap-rn-service-graph-connector-gcp.html)

The Project Number field is populated in the GCP Project \[cmdb\_ci\_gcp\_project\] table, enabling the quick identification of GCP projects when searching by project number.

    -   [Tag Governance](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-tag-governance.html)

Enhanced functionality for better visualization and navigation.

    -   [Learning Enhanced Automation Playbook \(LEAP\)](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-aiops-leap.html)

The Learning Enhanced Automation Playbook \(LEAP\) application uses AI to analyze incident data and facilitate the creation of automation that resolves high-impact issues for Service Operations teams. By leveraging data-driven analytics to accurately identify critical incidents, LEAP enables a more proactive problem management approach.

    -   [AI Agent Topology Mapping](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-agent-topology-mapping.html)

Get transparency and oversight of AI agents, including clear tracking of their business ownership.


 See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   AI-powered features in ITOM Visibility help administrators automate service map creation, diagnose discovery issues, manage certificates, and request firewall rules, using generative AI, AI agents, and agentic workflows.
-   Administrators can use the Discovery Admin Workspace, Service Mapping Workspace, and Firewall Admin Workspace to automate workflows and monitor process statuses.
-   Discover, monitor, and renew TLS/SSL certificates with a centralized inventory, and automate certificate requests, renewals, and revocations through supported certificate authorities with Certificate Inventory and Management.
-   Cryptographic Asset Compliance helps you manage cryptographic assets across cloud and on-premises environments to support post-quantum cryptography \(PQC\) readiness and help maintain security compliance.

 See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

