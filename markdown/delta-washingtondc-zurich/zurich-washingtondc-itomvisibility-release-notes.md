---
title: Combined ITOM Visibility release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for ITOM Visibility from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-itomvisibility-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 23
breadcrumb: [Products combined by family]
---

# Combined ITOM Visibility release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for ITOM Visibility from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITOM Visibility release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITOM Visibility to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

For an improved Service Mapping experience, install Service Mapping Plus version 1.13.0 from the ServiceNow® Store.

 Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

</td></tr><tr><td>

Yokohama

</td><td>

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

 After upgrading to Yokohama, a Fix Script named "Add Explicit Public SNMP Credential" might create a public SNMP credential in Production instances. This could lead to unnecessary records via Discovery. The Fix Script is present in Yokohama instances, including OOB. Before applying the upgrade of Discovery core, Yokohama version, verify the fix script behavior in a sandbox environment. Remove the public SNMP credentials if not required.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=available-patterns&family=washingtondc&ft:locale=en-US)**

Update your discovery capabilities through the following Discovery and Service Mapping Patterns:

    -   [IBM WebSEAL TD](https://servicenow-staging.fluidtopics.net/access?context=ibm_webseal_discovery_patterns&family=washingtondc&ft:locale=en-US)
    -   [Azure availability set](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=washingtondc&ft:locale=en-US)
    -   [NetApp Server and Cluster](https://servicenow-staging.fluidtopics.net/access?context=netapp-discovery&family=washingtondc&ft:locale=en-US)
    -   [Generate Software Bill Of Material \[SBOM\]](https://servicenow-staging.fluidtopics.net/access?context=generate-sbom-pattern&family=washingtondc&ft:locale=en-US)
    -   [Bring Your Own License \(BYOL\) for AWS, Azure, GCP](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=washingtondc&ft:locale=en-US)
    -   [Database Administrator \(DBA\) report](https://servicenow-staging.fluidtopics.net/access?context=dba-report-discovery-pattern&family=washingtondc&ft:locale=en-US)
    -   [Citrix NetScaler load balancer](https://servicenow-staging.fluidtopics.net/access?context=c_LoadBalancerCitrixNetscaler&family=washingtondc&ft:locale=en-US)
    -   [Microsoft SQL Server Integration Services \(SSIS\)](https://servicenow-staging.fluidtopics.net/access?context=ms-ssis-pattern&family=washingtondc&ft:locale=en-US)
    -   [SQL Server Analysis Services \(SSAS\)](https://servicenow-staging.fluidtopics.net/access?context=r-SSAS-MSSQL&family=washingtondc&ft:locale=en-US)
    -   [SAP Sybase ASE DB Catalog](https://servicenow-staging.fluidtopics.net/access?context=r-Sybase&family=washingtondc&ft:locale=en-US)
    -   [AWS Certificate Manager \(1.15.0\)](https://servicenow-staging.fluidtopics.net/access?context=aws-certificate-manager-discovery-pattern&family=washingtondc&ft:locale=en-US)
    -   [GCP Certificate Manager \(1.15.0\)](https://servicenow-staging.fluidtopics.net/access?context=gcp-certificate-discovery-pattern&family=washingtondc&ft:locale=en-US)
    -   [Azure Key Vault certificate \(1.15.0\)](https://servicenow-staging.fluidtopics.net/access?context=azure-certificate-discovery-pattern&family=washingtondc&ft:locale=en-US)
    -   [Java KeyStore and Windows Certificate Store \(1.15.0\)](https://servicenow-staging.fluidtopics.net/access?context=x509-certificates-discovery&family=washingtondc&ft:locale=en-US)
-   **[ITOM Content Service](https://servicenow-staging.fluidtopics.net/access?context=discovery-content-services&family=washingtondc&ft:locale=en-US)**

Discover applications and devices not discovered using patterns through a framework updated weekly with new content to gain visibility into your growing and developing infrastructure.

-   **[Discovery CLI commands](https://servicenow-staging.fluidtopics.net/access?context=discovery-cli-commands&family=washingtondc&ft:locale=en-US)**

Use a centralized interface and base system commands to execute Discovery.

-   **[Executing discovery patterns with Agent Client Collector](https://servicenow-staging.fluidtopics.net/access?context=application-patterns-acc&family=washingtondc&ft:locale=en-US)**

Run horizontal and top-down discovery using Agent Client Collector instead of a MID Server to access CIs on the client network.

-   **[Network location and MID affinity in top-down Discovery](https://servicenow-staging.fluidtopics.net/access?context=network-location-mid-affinity-td-discovery&family=washingtondc&ft:locale=en-US)**

Identify the appropriate MID Server to create application services for your network by using MID affinity.

-   **[Quick start tests for Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-service-mapping&family=washingtondc&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping works as expected. If you customized Service Mapping, copy the quick start tests and configure them for your customizations.

-   **[Pull additional resources from Kubernetes clusters into the CMDB](https://servicenow-staging.fluidtopics.net/access?context=cnov-config-pulling-extra-resources&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, configure the Cloud Native Operations for Visibility Informer to pull additional resources from Kubernetes clusters into the Configuration Management Database \(CMDB\) besides the resources it sends to the database by default.

-   **[Create a cmdb\_ci\_linux\_server CI for each Kubernetes node](https://servicenow-staging.fluidtopics.net/access?context=cnov-config-linux-server-ci&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, configure if you want the CNO for Visibility Informer automatically creates a cmdb\_ci\_linux\_server CI for each Kubernetes node. If these CIs are redundant or interfere with other flows in your organization, you can stop this process by setting the associated configuration parameter to false.

-   **[Define include and exclude lists of Labels and Annotations](https://servicenow-staging.fluidtopics.net/access?context=cnov-config-annotations-allowed&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, define include and exclude lists of Labels and Annotations in Kubernetes resources that the CNO for Visibility Informer pulls into the CMDB.

-   **[Display the Kubernetes cluster version in the CMDB](https://servicenow-staging.fluidtopics.net/access?context=cnov-config-see-cluster-version&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, automatically populate the field in the cmdb\_ci\_kubernetes\_cluster CI that shows the Kubernetes cluster version through CNO for Visibility Informer.

-   **[Add custom Labels and Annotations to Kubernetes resources](https://servicenow-staging.fluidtopics.net/access?context=cnov-config-add-custom-labels&family=washingtondc&ft:locale=en-US)**

Starting in version 3.6.2, add custom Labels and Annotations to all resources deployed in the Kubernetes cluster through CNO for Visibility.

-   **[ACME protocol support](https://servicenow-staging.fluidtopics.net/access?context=automated-certificate-management-environment_0&family=washingtondc&ft:locale=en-US)**

Version 3.4.0 introduces the Automated Certificate Management Environment \(ACME\) protocol support, which automates the process of certificate management.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Use Discovery Admin Workspace features to jumpstart discovery implementation.](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace&family=xanadu&ft:locale=en-US)**
    -   View discovery trends and tasks and access relevant ITOM Visibility apps and information through Discovery Admin Workspace Home.
    -   Gain insights into the performance of all your discoveries through the information in the **Schedules** tab.
    -   Analyze discovery errors and troubleshoot them using information in the **Diagnostics** tab.
    -   Access on-demand reports and optimize discovery operations using information in the**Insights** tab.
-   **[Discover products with Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Discover the following products through Discovery and Service Mapping Patterns:

    -   [Dell EMC Data Domain storage](https://servicenow-staging.fluidtopics.net/access?context=emc-data-domain-pattern&family=xanadu&ft:locale=en-US).
    -   [Dell EMC PowerMax storage](https://servicenow-staging.fluidtopics.net/access?context=emc-powermax-discovery-pattern&family=xanadu&ft:locale=en-US).
    -   [AWS services in the China region](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\) on the ServiceNow AI Platform Xanadu Patch 3 instance.
    -   [REST-based Fortinet firewall and FortiGate VDOMs](https://servicenow-staging.fluidtopics.net/access?context=fortinet-fw-vdoms-rest-discovery&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\).
    -   [Azure Marketplace](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=xanadu&ft:locale=en-US) - Available with the Discovery and Service Mapping Patterns November 2024 store release \(1.21.0\). The pattern supports the discovery of the following Azure Marketplace products:
        -   Virtual Machine
        -   SaaS
        -   Azure Application
-   **[Oracle Java process discovery](https://servicenow-staging.fluidtopics.net/access?context=oracle-glas-discovery&family=xanadu&ft:locale=en-US)**

Discover Java processes to comply with Oracle licensing agreements- Use the ITOM Oracle GLAS plugin \(1.8.4\) November 2024 store version to track Java installations and usage.

-   **[MID Server features for better discovery performance](https://servicenow-staging.fluidtopics.net/access?context=mid-server-rn&family=xanadu&ft:locale=en-US)**
    -   Run other applications without storing any credentials on the instance with the Microsoft Azure Key vault.
    -   MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode isn't enabled out of the box.
-   **[Use CMDB based mapping to create new application services](https://servicenow-staging.fluidtopics.net/access?context=cmdb-based-mapping&family=xanadu&ft:locale=en-US)**

Use Automated Service Suggestions and CMDB data instead of the MID Server, to create new application services.

-   **[Use the latest CNO for Visibility features](https://servicenow-staging.fluidtopics.net/access?context=cnov-configuring&family=xanadu&ft:locale=en-US)**

Starting in version 3.6.3, benefit from new features in Cloud Native Operations for Visibility.

    -   Upgrade the CNO for Visibility Informer from the ServiceNow instance.
    -   Control Informer execution parameters from the instance.
    -   Store instance credentials in the Microsoft Azure Vault when Informer uses the Azure Kubernetes Engine \(AKS\)
    -   Enable Informer to connect to the instance using OAuth2.0 authorization
-   **[Enjoy multi-architecture support for docker image](https://servicenow-staging.fluidtopics.net/access?context=cnov-deploy-prepare&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one.

-   **[Change the Informer's extensibility settings from the instance](https://servicenow-staging.fluidtopics.net/access?context=cnov-params-override&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), update the Informer's extensibility configuration directly from the Instance using the **Additional resources ConfigMap** parameter. By providing a JSON map with keys such as `resources`, `mappings`, and `mappings_oob`, you can instruct Cloud Native Operations for Visibility to retrieve additional information. If one of these keys exists and the system finds a change, it patches the ConfigMap and restarts the Informer.

-   **[View the OpenShift version in the Cluster version field on the Kubernetes Cluster CI](https://servicenow-staging.fluidtopics.net/access?context=cnov-deploy-install&family=xanadu&ft:locale=en-US)**

Starting in version 3.9.0 \(Informer version 2.3.0\), see the OpenShift version and the Kubernetes Cluster version in one place. OpenShift operates on top of Kubernetes, so there's an OpenShift version and a Kubernetes Cluster version. By installing the Informer with the **--set openShift=true** flag, the system adds the OpenShift version number to the **cluster\_version** field on the Kubernetes Cluster CI in addition to the Kubernetes Cluster version.

-   **[Use Service Fingerprints to refine the selection of application service candidates](https://servicenow-staging.fluidtopics.net/access?context=auto-serv-suggest&family=xanadu&ft:locale=en-US)**

Explore unique, classified components of application service candidates provided by Automated Service Suggestions. By supplying specific information such as the product name and description, gain deeper insights into the most suitable candidate to convert to an application service.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Discover additional AWS Services using Patterns](https://servicenow-staging.fluidtopics.net/access?context=aws-service-discovery-pattern&family=yokohama&ft:locale=en-US)**
    -   Starting with store version 1.25.0, Discovery and Service Mapping Patterns discovers 27 additional AWS cloud services.
    -   Starting with store version 1.27.0, Discovery and Service Mapping Patterns discovers 7 additional AWS cloud services.
-   **[Discover products with Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=available-patterns&family=yokohama&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.27.0:

    -   [NVIDIA GPUs](https://servicenow-staging.fluidtopics.net/access?context=nvidia-gpu-discovery-pattern&family=yokohama&ft:locale=en-US)
    -   [Microsoft SQL Always On availability groups](https://servicenow-staging.fluidtopics.net/access?context=mssql-data-collected-pattern&family=yokohama&ft:locale=en-US)
    -   [Azure tenants and management groups](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS Application Load Balancer targets](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS web ACL](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [AWS Systems Manager \(SSM\) agents](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=yokohama&ft:locale=en-US)
    -   [Tag collection for Azure VM instance - Uniform scale set](https://servicenow-staging.fluidtopics.net/access?context=AzureVMScaleSetInstance&family=yokohama&ft:locale=en-US)
-   **[Automatically generate a Certificate Signing Request](https://servicenow-staging.fluidtopics.net/access?context=request-new-csr-automated&family=yokohama&ft:locale=en-US)**

Generate a Certificate Signing Request and a private key with the Employee Center experience, starting with version 3.6.0 of Certificate Inventory and Management.

-   **[Use Service Graph Connectors for extended discovery](https://servicenow-staging.fluidtopics.net/access?context=cmdb-sgc-available&family=yokohama&ft:locale=en-US)**

Service Graph Connectors are a collection of predefined integrations that ingest data into the Configuration Management Database \(CMDB\) from third-party sources.

    -   Discover device details from Chromebook and ingest them into the CMDB by using Service Graph Connector for Google Console store version 1.8.
    -   Discover data from public cloud instances and resources in AWS, Azure, and GCP environments and ingest them into the CMDB by using Service Graph Connector for Wiz. 
-   **[Detect anomalies in Discovery schedules](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace-diagnostics&family=yokohama&ft:locale=en-US)**

Starting with Discovery Admin Workspace version 1.8.0, machine learning \(ML\) or statistical methods can detect anomalies in Discovery schedules and display this data in dashboards for admins. It identifies unusual behaviors like failed runs, significant deviations from user-defined thresholds for high error counts, longer discovery status duration, and fewer discovered Configuration Items \(CIs\) or Cloud resources. The ML-based approach to this feature is enabled by default. Thresholds are configurable via the new Settings page, and the results will be shown throughout the workspace.

-   **[Cloud-based Discovery schedules](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace-schedules&family=yokohama&ft:locale=en-US)**

Starting with version 1.8.0, Cloud-based discovery scheduling and reporting is available in Discovery Admin Workspace.

-   **[Configure Discovery to use Event Framework](https://servicenow-staging.fluidtopics.net/access?context=t_ConfigureDiscoveryEventFramework&family=yokohama&ft:locale=en-US)**

Starting with version 1.9.0, Discovery jobs can be configured to use an event-based system, reducing database activity by queuing and processing events at regular intervals with priority and memory monitoring.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Discover your Alibaba Cloud resources](https://servicenow-staging.fluidtopics.net/access?context=alibaba-cloud-discovery&family=zurich&ft:locale=en-US)**

Starting with Discovery and Service Mapping Patterns store version 1.29.0, Discovery supports Alibaba Cloud. Discovery enables real-time visibility and automated population of the CMDB with configuration data for cloud resources.

-   **[Create a cloud discovery schedule in Discovery Admin Workspace](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace-schedules&family=zurich&ft:locale=en-US)**

Starting with version 1.11.0, Discovery Admin Workspace supports creating Discovery schedules for Amazon Web Services, Azure, and Google Cloud Platform cloud providers. This update advances the integration of cloud discovery capabilities into a unified workspace, reducing operational complexity and aligning with the upcoming deprecation of Cloud Discovery Workspace.

For the procedural information, see:

    -   [AWS](https://servicenow-staging.fluidtopics.net/access?context=create-AWS-schedule-DAW&family=zurich&ft:locale=en-US)
    -   [Azure](https://servicenow-staging.fluidtopics.net/access?context=create-azure-schedule-DAW&family=zurich&ft:locale=en-US)
    -   [GCP](https://servicenow-staging.fluidtopics.net/access?context=create-gcp-schedule-DAW&family=zurich&ft:locale=en-US)
-   **[Discover AWS EC2 VMs using AWS Systems Manager \(SSM\)](https://servicenow-staging.fluidtopics.net/access?context=aws-ssm-discovery&family=zurich&ft:locale=en-US)**

Perform detailed discovery of EC2 hosts running in AWS without the requirement for a direct SSH or PowerShell connection by discovering AWS EC2 VMs by using AWS Systems Manager \(SSM\).

-   **[Discovery Guided Setup](https://servicenow-staging.fluidtopics.net/access?context=discovery-guided-setup&family=zurich&ft:locale=en-US)**

Starting with version 1.11.0, you can access ITOM Discovery Guided Setup from the Discovery Admin Workspace home page. This setup provides a structured process to configure Discovery and maintain accurate CMDB visibility quickly.

-   **[View command validation-related entries using new role in Pattern Designer Enhancements](https://servicenow-staging.fluidtopics.net/access?context=discovery-command-probe-pattern&family=zurich&ft:locale=en-US)**

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role has permissions to view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer role is restricted to viewing the command list modules and doesn't have permissions to modify or edit them. The pde\_viewer role can view the following tables only:

    -   Command List \[pd\_command\_list\]
    -   Command Validation Task \[pd\_command\_validation\]
    -   Command Validation Task Results \[pd\_command\_validation\_results\]
    -   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
    -   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]
-   **[Discover new products with Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=available-patterns&family=zurich&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.29.0:

    -   [Alibaba Cloud](https://servicenow-staging.fluidtopics.net/access?context=alibaba-cloud-discovery-pattern&family=zurich&ft:locale=en-US)
    -   [OCI GovCloud](https://servicenow-staging.fluidtopics.net/access?context=oracle-cloud-infrastructure-discovery&family=zurich&ft:locale=en-US)
    -   [10 addition Azure cloud services](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=zurich&ft:locale=en-US)
    -   [22 additional AWS cloud services](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=zurich&ft:locale=en-US)
    -   [New AWS API Gateway data model](https://servicenow-staging.fluidtopics.net/access?context=aws-api-gateway-discovery&family=zurich&ft:locale=en-US)
    -   [AWS datacenters with resources only](https://servicenow-staging.fluidtopics.net/access?context=data-discovered-aws-patterns&family=zurich&ft:locale=en-US)
    -   [OLVM templates, disks, and networks](https://servicenow-staging.fluidtopics.net/access?context=red-hat-virtualization-discovery&family=zurich&ft:locale=en-US)
    -   [Nutanix Prism using API v4](https://servicenow-staging.fluidtopics.net/access?context=nutanix-pattern&family=zurich&ft:locale=en-US)
Discover the following products using Discovery and Service Mapping Patterns version 1.28.0:

    -   [22 additional Azure cloud services](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=zurich&ft:locale=en-US)
    -   [GCP Cloud Function](https://servicenow-staging.fluidtopics.net/access?context=gcp-cloud-functions-patterns&family=zurich&ft:locale=en-US)
    -   [GCP AlloyDB](https://servicenow-staging.fluidtopics.net/access?context=gcp-alloydb-postgresql-patterns&family=zurich&ft:locale=en-US)
    -   [GCP Redis Cluster](https://servicenow-staging.fluidtopics.net/access?context=gcp-memorystore-patterns&family=zurich&ft:locale=en-US)
-   **[Receive updates for activated patterns](https://servicenow-staging.fluidtopics.net/access?context=activate-disabled-pattern&family=zurich&ft:locale=en-US)**

Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value.

-   **[Enhance your resource management with the new Tag Categorization feature from Tag Governance](https://servicenow-staging.fluidtopics.net/access?context=tag-categorization-tag-governance&family=zurich&ft:locale=en-US)**

Starting with version 1.7.0, automate the tagging process to promote a consistent, organized way to manage tags by using five predefined tag categories provided by Tag Governance.

-   **[Estimate your cloud license count prior to using ITOM cloud solutions using CLE](https://servicenow-staging.fluidtopics.net/access?context=cloud-license-estimator-landing&family=zurich&ft:locale=en-US)**

Cloud License Estimator \(CLE\) provides an estimated resource count for all cloud resources eligible for licensing.  It validates the  provided cloud  account details and estimates the resource  count  based on the prevailing licensing rules. 

-   **[Improve admin efficiency with new Actions menu](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace-diagnostics&family=zurich&ft:locale=en-US)**

Discovery Admin Workspace version 1.10.0 introduces a new **Actions** drop-down menu on the **Anomaly Detection** tab of the Diagnostics page, offering quick access to anomaly detection settings and a **Clear all anomalies** option to remove related records from key tables.


-   **[Enjoy increased control and improved accuracy in the Automated Service Suggestions feature](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-service-mapping-plus&family=zurich&ft:locale=en-US) in Service Mapping.**

Ensure that candidates remain relevant and useful through a new property that excludes irrelevant information from Application Service Candidates, such as non-operational or retired servers.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing ITOM Visibility features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Enhanced Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=available-patterns&family=washingtondc&ft:locale=en-US)**

Update your discovery capabilities through the following enhanced Discovery and Service Mapping Patterns:

    -   [Docker container identifier](https://servicenow-staging.fluidtopics.net/access?context=c-docker-virtualization&family=washingtondc&ft:locale=en-US)
    -   [Microsoft SQL Server and Cluster](https://servicenow-staging.fluidtopics.net/access?context=mssql-data-collected-pattern&family=washingtondc&ft:locale=en-US)
    -   [Azure Datacenter Discovery pattern and Hardware Type pattern \(1.15.0\)](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=washingtondc&ft:locale=en-US)
-   **[Service Mapping Unified Map support](https://servicenow-staging.fluidtopics.net/access?context=view-unified-map-sm-workspace&family=washingtondc&ft:locale=en-US)**

Access the centralized Unified Node Map from the Service Mapping workspace and view features of both the dependency view and the service map.

-   **[Unmapped Servers with Candidates](https://servicenow-staging.fluidtopics.net/access?context=unmapped-servers&family=washingtondc&ft:locale=en-US)**

Use unmapped servers aligned with identified application service candidates to create new application services.

-   **[Renamed ServiceNow® ITOM SU Licensing application](https://servicenow-staging.fluidtopics.net/access?context=itom-su-licensing-landing-page&family=washingtondc&ft:locale=en-US)**

Renamed ServiceNow® ITOM SU Licensing to ServiceNow® ITOM/OT SU Licensing.

-   **[Cloud Operations Workspace name change](https://servicenow-staging.fluidtopics.net/access?context=cow-landing-page&family=washingtondc&ft:locale=en-US)**

Starting with version 1.6.1, Cloud Operations Workspace has been renamed Cloud Discovery Workspace.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Use the enhanced Shazzam probe to collect data](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace-insights&family=xanadu&ft:locale=en-US)**

View the extended data collected by the Shazzam probe in the Discovery Admin Workspace **Insights** tab.

-   **[Revised Service Mapping roles](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-service-mapping&family=xanadu&ft:locale=en-US)**

Gain improved visibility of ML-powered candidates in Service Mapping with updated roles:

    -   service\_mapping\_admin replaces sm\_admin.
    -   service\_mapping\_user replaces sm\_user.
-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://servicenow-staging.fluidtopics.net/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Note the following new Pattern extensions and improvements:

    -   [Pure Storage FlashArray](https://servicenow-staging.fluidtopics.net/access?context=flasharray-discovery&family=xanadu&ft:locale=en-US)
    -   [Azure SQL license information](https://servicenow-staging.fluidtopics.net/access?context=azure-cloud-discovery-patterns&family=xanadu&ft:locale=en-US)
    -   [GCP resource inventory](https://servicenow-staging.fluidtopics.net/access?context=gcp-resource-inventory-discovery&family=xanadu&ft:locale=en-US)
-   **[Scale up your Azure change processing](https://servicenow-staging.fluidtopics.net/access?context=azure-change-processing&family=xanadu&ft:locale=en-US)**

Update your CMDB in real time with your Azure cloud resource changes. After upgrading to the enhanced November 2024 Patterns \(1.21.0\) version, run an Azure cloud discovery on all service accounts to ensure receiving all updates.

-   **[Stay informed about Cloud Discovery patterns updates](https://servicenow-staging.fluidtopics.net/access?context=r_SupportedApplications&family=xanadu&ft:locale=en-US)**

Download and use the Cloud Discovery patterns spreadsheet with the latest up-to-date information on Cloud Discovery patterns, including REST-API permissions.

-   **[Run top-down discovery using Service Mapping integrated with Agent Client Collector](https://servicenow-staging.fluidtopics.net/access?context=service-mapping-with-acc&family=xanadu&ft:locale=en-US)**

Top-down Service Mapping and Automated Service Suggestions are supported with Agent Client Collector.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Name suggestions for application service candidates](https://servicenow-staging.fluidtopics.net/access?context=app-services-name-suggestions&family=yokohama&ft:locale=en-US)**

Experience more accurate name suggestions for application service candidates based on Service Fingerprints in Service Mapping Plus store version 1.15.0.

-   **[Limits in Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-service-mapping&family=yokohama&ft:locale=en-US)**

Limits in Service Mapping prevent the disabling or deletion of jobs scheduled for the Checkpoint Reaper or the Service Model's Blob Reaper.

-   **[Limits in tag-based Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-service-mapping-plus&family=yokohama&ft:locale=en-US)**

Starting with version 1.15.2, experience improved performance in Service Mapping. A new property limits the creation of tag-based service candidates to 200 per service family.

-   **[Name update in Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=create-it-services&family=yokohama&ft:locale=en-US)**
    -   Application Services in the navigation menu has been renamed Service Instances.
    -   The label for the \[cmdb\_ci\_service\_auto\] table has been changed from Application Service to Service Instance.
-   **[Discovery status monitoring](https://servicenow-staging.fluidtopics.net/access?context=c_DiscoveryStatus&family=yokohama&ft:locale=en-US)**

Discovery schedules that have no status updates for over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://servicenow-staging.fluidtopics.net/access?context=available-patterns&family=zurich&ft:locale=en-US)**

Note the following new Pattern improvements using version 1.29.0:

    -   [IBM Hardware Management Console \(HMC\)](https://servicenow-staging.fluidtopics.net/access?context=ibm-hmc-discovery&family=zurich&ft:locale=en-US): additional fields in IBM Frame \[cmdb\_ci\_ibm\_frame\] and IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\] tables
    -   [Dell PowerMax storage](https://servicenow-staging.fluidtopics.net/access?context=emc-powermax-discovery-pattern&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [Pure Storage FlashArray](https://servicenow-staging.fluidtopics.net/access?context=flasharray-discovery&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [NetApp Server and Cluster](https://servicenow-staging.fluidtopics.net/access?context=netapp-discovery&family=zurich&ft:locale=en-US): additional fields in Storage Server \[cmdb\_ci\_storage\_server\] table
    -   [AWS Auto Scaling groups](https://servicenow-staging.fluidtopics.net/access?context=aws-auto-scaling-discovery&family=zurich&ft:locale=en-US): The relationship between Instance Scale Set and VM Instance has changed from **Members::Member of** to **Managed by::Manages**
-   **[Employ Tag-based mapping in the Service Mapping Workspace](https://servicenow-staging.fluidtopics.net/access?context=map-tag-based-services-workspace&family=zurich&ft:locale=en-US)**

Easily view data and create new tag-based services through an enhanced workspace that includes a dedicated dashboard for managing your tag-based services.

-   **[Name updates in Discovery and Service Mapping Patterns](https://servicenow-staging.fluidtopics.net/access?context=red-hat-virtualization-discovery&family=zurich&ft:locale=en-US)**

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
-   **[Benefit from an updated, curated selection of application service candidates in Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=sm-dashboard&family=zurich&ft:locale=en-US)**

If you have ITOM Content Service installed, you can view an enhanced selection of Application Service Candidates \(ASCs\) that provides more accurate and useful information, with an automatic filter applied to hide irrelevant and non-essential components.

-   **[Automate your certificate workflows using Keyfactor EJBCA and ACME](https://servicenow-staging.fluidtopics.net/access?context=automate-certificates-ejbca-acme&family=zurich&ft:locale=en-US)**

Starting with version XX of Certificate Inventory and Management, you can automate the life cycle of requesting, renewing, and revoking your certificates by integrating the Keyfactor EJBCA certificate authority with the ACME automated certificate management environment. Predefining your routing policies enables automated completion of the fields in your Certificate Signing Request \(CSR\) and provides a secure environment for an automated flow of certificates.

-   **[Discover a Root Certificate from a Browser](https://servicenow-staging.fluidtopics.net/access?context=discover-root-certificate-browser&family=zurich&ft:locale=en-US)**

Standard Discovery collects information about the certificates stored in your servers. You can also discover root certificates stored outside your servers and connect them to your certificate chain.

-   **[Kubernetes Visibility Agent \(KVA\)](https://servicenow-staging.fluidtopics.net/access?context=acc-kubernetes-visibility-landing-page&family=zurich&ft:locale=en-US)**

KVA performs continuous discovery to detect changes on resources in a Kubernetes cluster and updates the CMDB with the latest data.

Starting with KVA version 3.11.0, and Informer version 2.5.0, absent namespace CIs aren’t deleted automatically. Create a scheduled job to remove them.

Starting with KVA version 3.11.0, and Informer version 2.5.0, map application services based on traffic connections between the workloads in Kubernetes, by using istio and linked service meshes or the DaemonSet service.

-   **[Prevent credential exposure by updating HTTP Classify behavior](https://servicenow-staging.fluidtopics.net/access?context=create-an-http-classifier&family=zurich&ft:locale=en-US)**

The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. This change enhances security by helping prevent potential exposure of credentials over unencrypted connections. To override this behavior, a new MID Server property, **mid.http\_classy.allow\_credentials\_over\_http**, has been introduced. Enabling this setting might expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to false and use HTTPS whenever possible.

-   **[Automated Certificate Renewal](https://servicenow-staging.fluidtopics.net/access?context=automated-certificate-renewal&family=zurich&ft:locale=en-US)**

Starting with version 3.8.2, Certificate Inventory and Management introduces automated renewal capabilities. Administrators can set certificates to renew automatically, either when creating the certificate or by applying the setting to an existing one. The system also enables you to define the renewal window by specifying the number of days before expiration that the process should begin.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some ITOM Visibility features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some ITOM Visibility features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Deprecation of CAPI**

Starting with the Washington DC release, Cloud API Discovery is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Pattern-based Discovery provides the latest experience for the CAPI functionality.

Starting with version 1.6.0, the Firewall Audits and Reporting dashboard is deprecated.

Starting with version 1.6.0, the Certificate Management Dashboard dashboard is deprecated. Its features have been moved to the Next Experience UI's Polaris theme dashboard.

For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

Xanadu

</td><td>

Starting with the Xanadu release, the Discovery Dashboard is no longer part of the Discovery plugin. Use [Discovery Admin Workspace](https://servicenow-staging.fluidtopics.net/access?context=discovery-admin-workspace&family=xanadu&ft:locale=en-US) instead.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Application/Plugin Deprecation Process \[KB0867184\]Discovery CLI](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)**

Starting with version 3.5.0, Discovery CLI is no longer available in the Pattern Designer Enhancements Store App.


</td></tr><tr><td>

Zurich

</td><td>

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITOM Visibility.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require the ITOM Visibility subscription. For details, see [Request Discovery](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateTheDiscoveryPlugin&family=washingtondc&ft:locale=en-US) and [Request Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateServiceMappingPlugin&family=washingtondc&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr><tr><td>

Xanadu

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateTheDiscoveryPlugin&family=xanadu&ft:locale=en-US) and [Request Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateServiceMappingPlugin&family=xanadu&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr><tr><td>

Yokohama

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateTheDiscoveryPlugin&family=yokohama&ft:locale=en-US) and [Request Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateServiceMappingPlugin&family=yokohama&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr><tr><td>

Zurich

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateTheDiscoveryPlugin&family=zurich&ft:locale=en-US) and [Request Service Mapping](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateServiceMappingPlugin&family=zurich&ft:locale=en-US). For full ITOM Visibility functionality, install the latest ITOM Visibility applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version-history release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITOM Visibility we have noted them here.

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ITOM Visibility we have noted them here.

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

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

-   Discover and add applications from suggestions based on Predictive Intelligence by using Discovery Admin Workspace.
-   Use new and enhanced Discovery and Service Mapping Patterns for horizontal and top-down discovery.
-   Better identify the resources required for application services with the network location and MID affinity using the top-down discovery feature.
-   View a centralized map that combines features from both the dependency view and service map.
-   Discover applications and devices not discovered using patterns by using the new Content Service framework.

 See [IT Operations Management](https://servicenow-staging.fluidtopics.net/access?context=r_ITOMApplications&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Elevate the Discovery Admin experience with Discovery Admin Workspace. Benefit from a unified workspace for configuring Discovery, tracking progress, and managing errors, with diagnostic tools that provide insights into discovered data.
-   Enrich your CMDB with a larger number of configuration items using ITOM Content Service.
-   Create application services with CMDB based mapping.
-   Avoid dependence on your Kubernetes admin by upgrading Cloud Native Operations Informer pods and modifying Informer execution parameters directly from the instance.
-   Enjoy multi-architecture support for docker image in Cloud Native Operations for Visibility.

 See [IT Operations Management](https://servicenow-staging.fluidtopics.net/access?context=r_ITOMApplications&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Discovery and Service Mapping Patterns: Gain enhanced visibility into your AWS cloud services with 27 additional patterns starting with store version 1.25.0.
-   Starting with store version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. The CNO for Visibility feature has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Starting with Service Graph Connector for GCP store release 1.8, Service Graph Connector for AWS store release 2.9, and Service Graph Connector for Microsoft Azure store release 1.11, you can use Service Graph Connectors to ingest data into the Configuration Management Database \(CMDB\) from third-party sources.
-   Starting with store version 1.8.0, Discovery admins gain improved visibility into discovery issues and can address root causes using anomaly detection in the Discovery Admin Workspace.

 See [ITOM Visibility](https://servicenow-staging.fluidtopics.net/access?context=itom-visibility-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Cloud-based scheduling available in Discovery Admin Workspace \(store version 1.11.0\).
-   AWS EC2 VMs discovery using AWS Systems Manager \(SSM\).
-   Tag-based Service Mapping experience in the Service Mapping Workspace \(store version 1.16.3\).
-   Application service maps for containers via Kubernetes Visibility Agent \(KVA\) \(store version 3.11.0\).
-   25 cloud patterns shipped via Discovery and Service Mapping Patterns \(store version 1.28.0\)
-   Certificate Inventory and Management TLS Certificate request flows that support Keyfactor EJBCA \(store version 3.7.0\) and Certificate Inventory and Management Automated TLS Certificate renewal workflows \(store version 3.8.2\).

 See [IT Operations Management](https://servicenow-staging.fluidtopics.net/access?context=r_ITOMApplications&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

