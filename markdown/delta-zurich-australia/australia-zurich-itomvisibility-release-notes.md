---
title: Combined ITOM Visibility release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ITOM Visibility from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-itomvisibility-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined ITOM Visibility release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ITOM Visibility from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM Visibility release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM Visibility to Australia

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

Between your current release family and Australia, new features were introduced for ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[AI-Powered Service Mapping](https://www.servicenow.com/docs/access?context=ai-workflows-service-mapping&family=zurich&ft:locale=en-US)**
    -   Two AI Agents automatically generate service maps from ML candidates and connect Business Applications to discovered Application Services, eliminating manual CSDM relationship maintenance at scale. Available starting with Zurich Patch 9.
    -   Use the Service Mapping MCP tools to query live service topology, relationships, and CI data through a conversational interface via Claude Desktop. Available starting with Zurich Patch 10.
-   **[Install ITOM Visibility apps using Now Assist for Setup](https://www.servicenow.com/docs/access?context=nowassist-setup-itom-visibility-landing-page&family=zurich&ft:locale=en-US)**

Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.

-   **[Discover your Alibaba Cloud resources](https://www.servicenow.com/docs/access?context=alibaba-cloud-discovery&family=zurich&ft:locale=en-US)**

Starting with Discovery and Service Mapping Patterns store version 1.29.0, Discovery supports Alibaba Cloud. Discovery enables real-time visibility and automated population of the CMDB with configuration data for cloud resources.

-   **[Create a cloud discovery schedule in Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-schedules&family=zurich&ft:locale=en-US)**

Starting with version 1.11.0, Discovery Admin Workspace supports creating Discovery schedules for Amazon Web Services, Azure, and Google Cloud Platform cloud providers. This update advances the integration of cloud discovery capabilities into a unified workspace, reducing operational complexity and aligning with the upcoming deprecation of Cloud Discovery Workspace.

For the procedural information, see:

    -   [AWS](https://www.servicenow.com/docs/access?context=create-AWS-schedule-DAW&family=zurich&ft:locale=en-US)
    -   [Azure](https://www.servicenow.com/docs/access?context=create-azure-schedule-DAW&family=zurich&ft:locale=en-US)
    -   [GCP](https://www.servicenow.com/docs/access?context=create-gcp-schedule-DAW&family=zurich&ft:locale=en-US)
-   **[Discover AWS EC2 VMs using AWS Systems Manager \(SSM\)](https://www.servicenow.com/docs/access?context=aws-ssm-discovery&family=zurich&ft:locale=en-US)**

Perform detailed discovery of EC2 hosts running in AWS without the requirement for a direct SSH or PowerShell connection by discovering AWS EC2 VMs by using AWS Systems Manager \(SSM\).

-   **[Discovery Guided Setup](https://www.servicenow.com/docs/access?context=discovery-guided-setup&family=zurich&ft:locale=en-US)**

Starting with version 1.11.0, you can access ITOM Discovery Guided Setup from the Discovery Admin Workspace home page. This setup provides a structured process to configure Discovery and maintain accurate CMDB visibility quickly.

-   **[View command validation-related entries using new role in Pattern Designer Enhancements](https://www.servicenow.com/docs/access?context=discovery-command-probe-pattern&family=zurich&ft:locale=en-US)**

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role has permissions to view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer role is restricted to viewing the command list modules and doesn't have permissions to modify or edit them. The pde\_viewer role can view the following tables only:

    -   Command List \[pd\_command\_list\]
    -   Command Validation Task \[pd\_command\_validation\]
    -   Command Validation Task Results \[pd\_command\_validation\_results\]
    -   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
    -   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]
-   **[Discover new products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=available-patterns&family=zurich&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.29.0:

    -   [Alibaba Cloud](https://www.servicenow.com/docs/access?context=alibaba-cloud-discovery-pattern&family=zurich&ft:locale=en-US)
    -   [OCI GovCloud](https://www.servicenow.com/docs/access?context=oracle-cloud-infrastructure-discovery&family=zurich&ft:locale=en-US)
    -   [10 addition Azure cloud services](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&family=zurich&ft:locale=en-US)
    -   [22 additional AWS cloud services](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=zurich&ft:locale=en-US)
    -   [New AWS API Gateway data model](https://www.servicenow.com/docs/access?context=aws-api-gateway-discovery&family=zurich&ft:locale=en-US)
    -   [AWS datacenters with resources only](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&family=zurich&ft:locale=en-US)
    -   [OLVM templates, disks, and networks](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&family=zurich&ft:locale=en-US)
    -   [Nutanix Prism using API v4](https://www.servicenow.com/docs/access?context=nutanix-pattern&family=zurich&ft:locale=en-US)
Discover the following products using Discovery and Service Mapping Patterns version 1.28.0:

    -   [22 additional Azure cloud services](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&family=zurich&ft:locale=en-US)
    -   [GCP Cloud Function](https://www.servicenow.com/docs/access?context=gcp-cloud-functions-patterns&family=zurich&ft:locale=en-US)
    -   [GCP AlloyDB](https://www.servicenow.com/docs/access?context=gcp-alloydb-postgresql-patterns&family=zurich&ft:locale=en-US)
    -   [GCP Redis Cluster](https://www.servicenow.com/docs/access?context=gcp-memorystore-patterns&family=zurich&ft:locale=en-US)
-   **[Receive updates for activated patterns](https://www.servicenow.com/docs/access?context=activate-disabled-pattern&family=zurich&ft:locale=en-US)**

Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value.

-   **[Enhance your resource management with the new Tag Categorization feature from Tag Governance](https://www.servicenow.com/docs/access?context=tag-categorization-tag-governance&family=zurich&ft:locale=en-US)**

Starting with version 1.7.0, automate the tagging process to promote a consistent, organized way to manage tags by using five predefined tag categories provided by Tag Governance.

-   **[Estimate your cloud license count prior to using ITOM cloud solutions using CLE](https://www.servicenow.com/docs/access?context=cloud-license-estimator-landing&family=zurich&ft:locale=en-US)**

Cloud License Estimator \(CLE\) provides an estimated resource count for all cloud resources eligible for licensing.  It validates the  provided cloud  account details and estimates the resource  count  based on the prevailing licensing rules. 

-   **[Improve admin efficiency with new Actions menu](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-diagnostics&family=zurich&ft:locale=en-US)**

Discovery Admin Workspace version 1.10.0 introduces a new **Actions** drop-down menu on the **Anomaly Detection** tab of the Diagnostics page, offering quick access to anomaly detection settings and a **Clear all anomalies** option to remove related records from key tables.


-   **[Enjoy increased control and improved accuracy in the Automated Service Suggestions feature](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping-plus&family=zurich&ft:locale=en-US) in Service Mapping.**

Ensure that candidates remain relevant and useful through a new property that excludes irrelevant information from Application Service Candidates, such as non-operational or retired servers.


</td></tr><tr><td>

Australia

</td><td>

-   **[Install ITOM Visibility apps using Now Assist for Setup](https://www.servicenow.com/docs/access?context=nowassist-setup-itom-visibility-landing-page&family=australia&ft:locale=en-US)**

Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.


-   **[PowerShell 7 support for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&family=australia&ft:locale=en-US)**

Discovery now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Discovery on Code Signing instances](https://www.servicenow.com/docs/access?context=code-sign-disco-probes&family=australia&ft:locale=en-US)**

Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.

-   **[Discovery generic attributes](https://www.servicenow.com/docs/access?context=disco-generic-attributes&family=australia&ft:locale=en-US)**

Enhance Configuration Management Database \(CMDB\) data accuracy with new Discovery capabilities that auto-populate non-discoverable attributes using a schedule-based mechanism. This update simplifies configuration item \(CI\) management by propagating generic attribute values across schedules and ranges, reducing manual effort and improving usability.

-   **[Use Kubernetes Visibility Agent \(KVA\) and Service Mapping to create service maps for extended services beyond Kubernetes](https://www.servicenow.com/docs/access?context=mapping-k8s-sm-kva&family=australia&ft:locale=en-US)**

Service Mapping complements Kubernetes Visibility Agent \(KVA\) capabilities to map services that include Kubernetes and all related service resources beyond the Kubernetes environment. Install the latest version of Kubernetes Visibility Agent \(KVA\) to detect the latest changes in your Kubernetes cluster and run Service Mapping to have an up to date visualization of your services across Kubernetes and related resources.

-   **[Quick start tests for Service Mapping](https://www.servicenow.com/docs/access?context=quick-start-tests-service-mapping&family=australia&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping works as expected. If you customized Service Mapping, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ITOM Visibility features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://www.servicenow.com/docs/access?context=available-patterns&family=zurich&ft:locale=en-US)**

Note the following new Pattern improvements using version 1.29.0:

    -   [IBM Hardware Management Console \(HMC\)](https://www.servicenow.com/docs/access?context=ibm-hmc-discovery&family=zurich&ft:locale=en-US): additional fields in IBM Frame \[cmdb\_ci\_ibm\_frame\] and IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\] tables
    -   [Dell PowerMax storage](https://www.servicenow.com/docs/access?context=emc-powermax-discovery-pattern&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [Pure Storage FlashArray](https://www.servicenow.com/docs/access?context=flasharray-discovery&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [NetApp Server and Cluster](https://www.servicenow.com/docs/access?context=netapp-discovery&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [AWS Auto Scaling groups](https://www.servicenow.com/docs/access?context=aws-auto-scaling-discovery&family=zurich&ft:locale=en-US): The relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**
-   **[Employ Tag-based mapping in the Service Mapping Workspace](https://www.servicenow.com/docs/access?context=map-tag-based-services-workspace&family=zurich&ft:locale=en-US)**

Easily view data and create new tag-based services through an enhanced workspace that includes a dedicated dashboard for managing your tag-based services.

-   **[Name updates in Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&family=zurich&ft:locale=en-US)**

Name updates starting with Discovery and Service Mapping Patterns version 1.28.0:

    -   The RHV cloud provider has been changed to oVirt
    -   The RHV MID Server capability has been changed to oVirt
    -   The label for the \[cmdb\_ci\_rhv\_ldc\] datacenter type has been changed from RHV LDC to oVirt LDC
    -   The label for the \[rhv\_credentials\] credential type has been changed from RHV Credentials to oVirt Credentials
    -   The following pattern names have been changed from RHV to oVirt:
        -   From RHV Clusters and Hosts to oVirt Clusters and Hosts
        -   From RHV Discover Logical datacenters to oVirt Discover Logical datacenters
        -   From RHV Virtual Machines to oVirt Virtual Machines
        -   From RHV Discover Manager Instance to oVirt Discover Manager Instance
    -   The following table labels have been changed from RHV to oVirt:
        -   The \[cmdb\_ci\_rhv\_vm\_instance\] table label from RHV Virtual Machine Instance to oVirt Virtual Machine Instance
        -   The \[cmdb\_ci\_rhv\_cluster\] table label from RHV Cluster to oVirt Cluster
        -   The \[cmdb\_ci\_rhv\_ldc\] table label from RHV LDC to oVirt LDC
        -   The \[cmdb\_ci\_rhv\_manager\] table label from RHV Manager to oVirt Manager
        -   The \[cmdb\_ci\_rhv\_object\] table label from RHV Object to oVirt Object
        -   The \[cmdb\_ci\_rhv\_server\] table label from RHV Server to oVirt Server
-   **[Benefit from an updated, curated selection of application service candidates in Service Mapping](https://www.servicenow.com/docs/access?context=sm-dashboard&family=zurich&ft:locale=en-US)**

If you have ITOM Content Service installed, you can view an enhanced selection of Application Service Candidates \(ASCs\) that provides more accurate and useful information, with an automatic filter applied to hide irrelevant and non-essential components.

-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://www.servicenow.com/docs/access?context=automate-certificates-ejbca-acme&family=zurich&ft:locale=en-US)**

Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://www.servicenow.com/docs/access?context=discover-root-certificate-browser&family=zurich&ft:locale=en-US)**

Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Kubernetes Visibility Agent \(KVA\)](https://www.servicenow.com/docs/access?context=acc-kubernetes-visibility-landing-page&family=zurich&ft:locale=en-US)**

KVA performs continuous discovery to detect changes on resources in a Kubernetes cluster and updates the CMDB with the latest data.

Starting with KVA version 3.11.0, and Informer version 2.5.0, absent namespace CIs aren’t deleted automatically. Create a scheduled job to remove them.

Starting with KVA version 3.11.0, and Informer version 2.5.0, map application services based on traffic connections between the workloads in Kubernetes, by using istio and linked service meshes or the DaemonSet service.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://www.servicenow.com/docs/access?context=create-an-http-classifier&family=zurich&ft:locale=en-US)**

The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.

-   **[Automated Certificate Renewal](https://www.servicenow.com/docs/access?context=automated-certificate-renewal&family=zurich&ft:locale=en-US)**

Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ITOM Visibility features or functionality were removed.

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

Between your current release family and Australia, some ITOM Visibility features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Australia

</td><td>

-   Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=zurich&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=zurich&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version-history release notes.

</td></tr><tr><td>

Australia

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&family=australia&ft:locale=en-US) and [Request Service Mapping](https://www.servicenow.com/docs/access?context=t_ActivateServiceMappingPlugin&family=australia&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store..

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM Visibility we have noted them here.

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

If any specific browser requirements were introduced or changed for ITOM Visibility we have noted them here.

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

Review details on accessibility information for ITOM Visibility, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

 -   **[Store updates for ITOM Visibility](https://www.servicenow.com/docs/access?context=store-rn-itom-visibility-landing&family=australia&ft:locale=en-US)**

The majority of Visibility apps are updated monthly or quarterly via the ServiceNow Store. The latest updates are available in the ServiceNow Store. For cumulative release notes and compatibility information, see the ServiceNow Store version details.

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

    -   [Learning Enhanced Automation Playbook \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&family=australia&ft:locale=en-US)

The Learning Enhanced Automation Playbook \(LEAP\) application uses AI to analyze incident data and facilitate the creation of automations that resolve high-impact issues for Service Operations teams. By leveraging data-driven analytics to accurately identify critical incidents, LEAP enables a more proactive problem management approach.

    -   [AI Agent Topology Mapping](https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-agent-topology-mapping.html)

Get transparency and oversight of AI agents, including clear tracking of their business ownership.


 See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

