---
title: Combined ITOM Visibility release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for ITOM Visibility from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-itomvisibility-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined ITOM Visibility release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for ITOM Visibility from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM Visibility release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM Visibility to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Automatically generate a Certificate Signing Request](https://www.servicenow.com/docs/access?context=request-new-csr-automated&family=yokohama&ft:locale=en-US)**

Generate a Certificate Signing Request and a private key with the Employee Center experience, starting with version 3.6.0 of Certificate Inventory and Management.

-   **[Use Service Graph Connectors for extended discovery](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&family=yokohama&ft:locale=en-US)**

Service Graph Connectors are a collection of predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources.

    -   Discover device details from Chromebook and ingest them into the CMDB by using Service Graph Connector for Google Chromebooks store version 1.8.
    -   Discover data from public cloud instances and resources in AWS, Azure, and GCP environments and ingest them into the CMDB by using Service Graph Connector for Wiz. 

</td></tr><tr><td>

Zurich

</td><td>

-   **[Discover AWS EC2 VMs using AWS Systems Manager \(SSM\)](https://www.servicenow.com/docs/access?context=aws-ssm-discovery&family=zurich&ft:locale=en-US)**

Perform detailed discovery of EC2 hosts running in AWS without the requirement for a direct SSH or PowerShell connection by discovering AWS EC2 VMs by using AWS Systems Manager \(SSM\).

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
-   **[Estimate your cloud license count prior to using ITOM cloud solutions using CLE](https://www.servicenow.com/docs/access?context=cloud-license-estimator-landing&family=zurich&ft:locale=en-US)**

Cloud License Estimator \(CLE\) provides an estimated resource count for all cloud resources eligible for licensing.  It validates the  provided cloud  account details and estimates the resource  count  based on the prevailing licensing rules. 


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ITOM Visibility features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Limits in Service Mapping](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&family=yokohama&ft:locale=en-US)**

Limits in Service Mapping prevent the disabling or deletion of jobs scheduled for the Checkpoint Reaper or the Service Model's Blob Reaper.

-   **[Name update in Service Mapping](https://www.servicenow.com/docs/access?context=create-it-services&family=yokohama&ft:locale=en-US)**
    -   Application Services in the navigation menu has been renamed Service Instances.
    -   The label for the \[cmdb\_ci\_service\_auto\] table has been changed from Application Service to Service Instance.
-   **[Discovery status monitoring](https://www.servicenow.com/docs/access?context=c_DiscoveryStatus&family=yokohama&ft:locale=en-US)**

Discovery schedules that have no status updates for over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Streamlined access to Cloud Service Accounts in Discovery](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-home&family=zurich&ft:locale=en-US)**

Starting with Discovery Admin Workspace version 1.10.0, Cloud Service Accounts can be accessed directly from the Discovery section of the navigation menu.


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
-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://www.servicenow.com/docs/access?context=automate-certificates-ejbca-acme&family=zurich&ft:locale=en-US)**

Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://www.servicenow.com/docs/access?context=discover-root-certificate-browser&family=zurich&ft:locale=en-US)**

Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://www.servicenow.com/docs/access?context=create-an-http-classifier&family=zurich&ft:locale=en-US)**

The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.


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

Between your current release family and Australia, some ITOM Visibility features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM Visibility we have noted them here.

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

If any specific browser requirements were introduced or changed for ITOM Visibility we have noted them here.

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

Review details on accessibility information for ITOM Visibility, such as specific requirements or compliance levels.

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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

If there are specific highlight considerations for ITOM Visibility we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

