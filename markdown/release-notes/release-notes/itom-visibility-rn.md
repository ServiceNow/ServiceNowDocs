---
title: ITOM Visibility release notes
description: The ServiceNow ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-01"
reading_time_minutes: 10
---

# ITOM Visibility release notes

The ServiceNow® ITOM Visibility application provides a unified, connected view of your entire IT infrastructure and the services that it supports. ITOM Visibility was enhanced and updated in the Zurich release.

## ITOM Visibility highlights for the Zurich release

-   Cloud-based scheduling available in Discovery Admin Workspace \(store version 1.11.0\).
-   AWS EC2 VMs discovery using AWS Systems Manager \(SSM\).
-   Tag-based Service Mapping experience in the Service Mapping Workspace \(store version 1.16.3\).
-   Application service maps for containers via Kubernetes Visibility Agent \(KVA\) \(store version 3.11.0\).
-   25 cloud patterns shipped via Discovery and Service Mapping Patterns \(store version 1.28.0\)
-   Certificate Inventory and Management TLS Certificate request flows that support Keyfactor EJBCA \(store version 3.7.0\) and Certificate Inventory and Management Automated TLS Certificate renewal workflows \(store version 3.8.2\).

See [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/r_ITOMApplications.md) for more information.

**Important:** Discovery and Service Mapping Patterns, Cloud Service Graph Connectors, and Kubernetes Visibility Agent \(KVA\) are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[AI-Powered Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/ai-workflows-service-mapping.md)**
    -   Two AI Agents automatically generate service maps from ML candidates and connect Business Applications to discovered Application Services, eliminating manual CSDM relationship maintenance at scale. Available starting with Zurich Patch 9.
    -   Use the Service Mapping MCP tools to query live service topology, relationships, and CI data through a conversational interface via Claude Desktop. Available starting with Zurich Patch 10.
-   **Install ITOM Visibility apps using Now Assist for Setup**

    Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.

-   **[Discover your Alibaba Cloud resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/alibaba-cloud-discovery.md)**

    Starting with Discovery and Service Mapping Patterns store version 1.29.0, Discovery supports Alibaba Cloud. Discovery enables real-time visibility and automated population of the CMDB with configuration data for cloud resources.

-   **[Create a cloud discovery schedule in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-admin-workspace-schedules.md)**

    Starting with version 1.11.0, Discovery Admin Workspace supports creating Discovery schedules for Amazon Web Services, Azure, and Google Cloud Platform cloud providers. This update advances the integration of cloud discovery capabilities into a unified workspace, reducing operational complexity and aligning with the upcoming deprecation of Cloud Discovery Workspace.

    For the procedural information, see:

    -   [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/create-AWS-schedule-DAW.md)
    -   [Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/create-azure-schedule-DAW.md)
    -   [GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/create-gcp-schedule-DAW.md)
-   **[Discover AWS EC2 VMs using AWS Systems Manager \(SSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aws-ssm-discovery.md)**

    Perform detailed discovery of EC2 hosts running in AWS without the requirement for a direct SSH or PowerShell connection by discovering AWS EC2 VMs by using AWS Systems Manager \(SSM\).

-   **[Discovery Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-guided-setup.md)**

    Starting with version 1.11.0, you can access ITOM Discovery Guided Setup from the Discovery Admin Workspace home page. This setup provides a structured process to configure Discovery and maintain accurate CMDB visibility quickly.

-   **[View command validation-related entries using new role in Pattern Designer Enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-command-probe-pattern.md)**

    Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role has permissions to view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer role is restricted to viewing the command list modules and doesn't have permissions to modify or edit them. The pde\_viewer role can view the following tables only:

    -   Command List \[pd\_command\_list\]
    -   Command Validation Task \[pd\_command\_validation\]
    -   Command Validation Task Results \[pd\_command\_validation\_results\]
    -   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
    -   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]
-   **[Discover new products with Discovery and Service Mapping Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/available-patterns.md)**

    Discover the following products using Discovery and Service Mapping Patterns version 1.29.0:

    -   [Alibaba Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/alibaba-cloud-discovery-pattern.md)
    -   [OCI GovCloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/oracle-cloud-infrastructure-discovery.md)
    -   [10 addition Azure cloud services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/azure-cloud-discovery-patterns.md)
    -   [22 additional AWS cloud services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/data-discovered-aws-patterns.md)
    -   [New AWS API Gateway data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aws-api-gateway-discovery.md)
    -   [AWS datacenters with resources only](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/data-discovered-aws-patterns.md)
    -   [OLVM templates, disks, and networks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/red-hat-virtualization-discovery.md)
    -   [Nutanix Prism using API v4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/nutanix-pattern.md)
    Discover the following products using Discovery and Service Mapping Patterns version 1.28.0:

    -   [22 additional Azure cloud services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/azure-cloud-discovery-patterns.md)
    -   [GCP Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/gcp-cloud-functions-patterns.md)
    -   [GCP AlloyDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/gcp-alloydb-postgresql-patterns.md)
    -   [GCP Redis Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/gcp-memorystore-patterns.md)
-   **[Receive updates for activated patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/activate-disabled-pattern.md)**

    Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value.

-   **[Enhance your resource management with the new Tag Categorization feature from Tag Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/tag-categorization-tag-governance.md)**

    Starting with version 1.7.0, automate the tagging process to promote a consistent, organized way to manage tags by using five predefined tag categories provided by Tag Governance.

-   **[Estimate your cloud license count prior to using ITOM cloud solutions using CLE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/cloud-license-estimator-landing.md)**

    Cloud License Estimator \(CLE\) provides an estimated resource count for all cloud resources eligible for licensing.  It validates the  provided cloud  account details and estimates the resource  count  based on the prevailing licensing rules. 

-   **[Improve admin efficiency with new Actions menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-admin-workspace-diagnostics.md)**

    Discovery Admin Workspace version 1.10.0 introduces a new **Actions** drop-down menu on the **Anomaly Detection** tab of the Diagnostics page, offering quick access to anomaly detection settings and a **Clear all anomalies** option to remove related records from key tables.


-   **[Enjoy increased control and improved accuracy in the Automated Service Suggestions feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/components-installed-with-service-mapping-plus.md) in Service Mapping.**

    Ensure that candidates remain relevant and useful through a new property that excludes irrelevant information from Application Service Candidates, such as non-operational or retired servers.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Explore additional Cloud Discovery metrics and visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/c_daw-disco-schedule-details.md)**

    Starting with version 1.10.0, in addition to the IP-based Discovery schedules, Cloud Discovery schedule details and data visualizations are available in the Discovery Admin Workspace. These visualizations provide a comprehensive view of the schedule's performance and status, highlighting key metrics such as the number of discoveries completed, success rate, and any errors encountered.

-   **[Streamlined access to Cloud Service Accounts in Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-admin-workspace-home.md)**

    Starting with Discovery Admin Workspace version 1.10.0, Cloud Service Accounts can be accessed directly from the Discovery section of the navigation menu.

-   **[Use virtual agent to retrieve MID Server settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discovery-admin-workspace-diagnostics.md)**

    Starting with Discovery Admin Workspace version 1.10.0, the virtual agent on the Diagnostics page now enables you to retrieve and download MID Server settings directly, eliminating the need to manually navigate through the MID Server \[mid\_servers\] table.


## Changed in this release

-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/available-patterns.md)**

    Note the following new Pattern improvements using version 1.29.0:

    -   [IBM Hardware Management Console \(HMC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/ibm-hmc-discovery.md): additional fields in IBM Frame \[cmdb\_ci\_ibm\_frame\] and IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\] tables
    -   [Dell PowerMax storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/emc-powermax-discovery-pattern.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [Pure Storage FlashArray](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/flasharray-discovery.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [NetApp Server and Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/netapp-discovery.md): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [AWS Auto Scaling groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aws-auto-scaling-discovery.md): The relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**
-   **[Employ Tag-based mapping in the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/map-tag-based-services-workspace.md)**

    Easily view data and create new tag-based services through an enhanced workspace that includes a dedicated dashboard for managing your tag-based services.

-   **[Name updates in Discovery and Service Mapping Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/red-hat-virtualization-discovery.md)**

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
-   **[Benefit from an updated, curated selection of application service candidates in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/sm-dashboard.md)**

    If you have ITOM Content Service installed, you can view an enhanced selection of Application Service Candidates \(ASCs\) that provides more accurate and useful information, with an automatic filter applied to hide irrelevant and non-essential components.

-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/automate-certificates-ejbca-acme.md)**

    Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/discover-root-certificate-browser.md)**

    Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Kubernetes Visibility Agent \(KVA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/acc-kubernetes-visibility-landing-page.md)**

    KVA performs continuous discovery to detect changes on resources in a Kubernetes cluster and updates the CMDB with the latest data.

    Starting with KVA version 3.11.0, and Informer version 2.5.0, absent namespace CIs aren’t deleted automatically. Create a scheduled job to remove them.

    Starting with KVA version 3.11.0, and Informer version 2.5.0, map application services based on traffic connections between the workloads in Kubernetes, by using istio and linked service meshes or the DaemonSet service.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/create-an-http-classifier.md)**

    The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.

-   **[Automated certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/automated-certificate-renewal.md)**

    Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


## Deprecations

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Activation information

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/t_ActivateTheDiscoveryPlugin.md) and [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/t_ActivateServiceMappingPlugin.md). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version-history release notes.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[ITOM Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/itom-health-landing-page.md)**

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

    Event Management gathers alerts from infrastructure events that both third-party monitoring tools and the ServiceNow® internal agent capture. Event Management uses IT-related information that ServiceNow® Discovery gathers so it can map alerts to configuration items. Based on the collected information, Event Management then provides dashboards that show a consolidated view of all service-impact events.

    The Agent Client Collector application enables you to do the following:

    -   Monitor your service availability.
    -   Examine the health and performance of your environment.
    -   Ensure that your infrastructure and its applications are running properly.
    Agent Client Collector collects events and metrics. It runs in either a Windows or Linux environment.

-   **[Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aiops-leap.md)**

    The AIOps Learning Enhanced Automation Playbook \(LEAP\) application uses AI to analyze incident data and facilitate the creation of automations that resolve high-impact issues for Service Operations teams. By leveraging data-driven analytics to accurately identify critical incidents, LEAP enables a more proactive problem management approach.

-   **[ITOM Cloud Accelerate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/itom-cloud-accelerate-landing-page.md)**

    ITOM Cloud Accelerate workflows streamline cloud automation across the cloud adoption journey via self-service catalogs and controlled workflows. It expedites application migration by facilitating assessment, planning, and resource migration tracking.

    ITOM Cloud Accelerate includes the following apps:

    -   Cloud Account Management
    -   Cloud Services Catalog
    -   Cloud Configuration Governance
    -   Cloud Action Library

**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-operations-management-rn-landing.md)

