---
title: Microsoft Azure Cloud discovery using patterns
description: Discovery uses multiple patterns to discover components of the Microsoft Azure Cloud deployment during horizontal discovery. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 16
keywords: [Patterns, Azure, Cloud, Discovery]
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure Cloud discovery using patterns

Discovery uses multiple patterns to discover components of the Microsoft Azure Cloud deployment during horizontal discovery. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Activate the cloud-related CI relationships**

    To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration]().

-   **Azure Availability Set**

    Wait for the **Clean-Up job for Availability zone to clear availability set record** schedule job to delete all the pre-populated Configuration Items \(CIs\) in the **cmdb\_ci\_azure\_availability\_set** table.

-   **Azure Availability Zone**

    To run a discovery with Azure Availability Zone, register the subscription ID to the **AvailabilityZonePeering** feature with AZ CLI using `az feature register -n AvailabilityZonePeering --namespace Microsoft.Resources` to use the Check Zone Peering API. Check the status with `az feature show -n AvailabilityZonePeering --namespace Microsoft.Resources` before running discovery.

-   **Set up Azure service accounts**

    Enable Cloud Discovery to access your Azure environment. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/setup-azure-service-accounts.md).

-   **Create an Azure cloud discovery schedule**

    For more information, see [Create an Azure Discovery schedule in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/create-azure-schedule-DAW.md).

-   **\(Optional\) Discover datacenters only for new subscriptions**

    Starting with Zurich Patch 2, you can discover datacenters only for new subscriptions added since the last discovery. For more information, see [Discover datacenters only for new cloud accounts]().

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables]().


## Verify the REST API permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Azure resources discovery by datacenters

Azure has multiple datacenters around the world, but resources like load balancers and virtual machines are typically deployed in only some of them. The **Azure Datacenter Discovery** pattern executes before all other Azure patterns to identify the datacenters that have resources related to your service account \("active"\) and the datacenters that don't have your resources \("passive"\). This model improves the performance of the Azure discovery. This execution model is more efficient than the previous one, in which all datacenters were discovered regardless of having relevant resources in them.

After identifying the "active" and "passive" datacenters, the Discovery schedule continues to execute all Azure patterns only for the "active" datacenters, to discover your Azure cloud resources. The "passive" datacenters are ignored while running the schedule.

You might notice differences in Azure discovery log, in discovery time and in the CMDB, depending on the service account and MID Server property settings.

Datacenters that have already been discovered before the upgrade to Discovery and Service Mapping Patterns version 1.15.0, remain in the **Azure Datacenters** table. However, the discovery runtime behavior is now determined by the value of the MID Server property **mid.cloud.discovery.sonar.discover\_all\_azure\_datacenters**. The property is set to **false** by default, to limit the discovery execution to the "active" datacenters, rather than all datacenters. You can discover all datacenters for a service account, including "passive" ones, by setting the property to **true**. For more information, see: [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_MIDServerProperties.md).

If the MID Server property is set to **false**, the Azure Datacenters table shows only active datacenters. All other behaviors remain unchanged from previous Discovery and Service Mapping Patterns versions.

|Discovery and Service Mapping Patterns version|MID Server property setting|Discovered datacenters|Datacenters contained in Azure Datacenters table|Datacenters displayed in discovery log|
|----------------------------------------------|---------------------------|----------------------|------------------------------------------------|--------------------------------------|
|Discovery and Service Mapping Patterns starting with version 1.15.0|False \(default\)|Active only|Active only|Active only|
|Discovery and Service Mapping Patterns starting with version 1.15.0|True|All datacenters|All datacenters|All datacenters|
|Discovery and Service Mapping Patterns before version 1.15.0|False \(default\)|Active only|All datacenters|Active only|
|Discovery and Service Mapping Patterns before version 1.15.0|True|All datacenters|All datacenters|All datacenters|

For management groups, Azure Cloud Discovery discovers all Azure datacenters.

Starting with Discovery and Service Mapping Patterns version 1.29.0, the **Refresh Datacenters** flow displays all regions, not just active ones. You don't need to create another schedule when a resource is added or a datacenter switches from passive to active.

## Azure Hardware Type discovery

Hardware Type discovery has undergone three model changes in recent years. The 1.15.0 model triggers the **Hardware Type** pattern and the **Virtual Machine** pattern after the **Azure Datacenter Discovery** pattern. Starting Discovery and Service Mapping Patterns plugin version 1.15.0, Cloud Discovery identifies which Hardware Type model is used, and launches only one of the two patterns: **Hardware Type \(LP\)** or **Cloud Hardware Type \(LP\)**.

<table id="table_gml_tkv_1bc"><thead><tr><th>

Discovery and Service Mapping Patterns version

</th><th>

Hardware Type Migration status

</th><th>

Which pattern executes

</th><th>

Discovery result

</th></tr></thead><tbody><tr><td>

Prior to 1.0.75

</td><td>

Haven't migrated to the new model

</td><td>

**Hardware Type \(LP\)** pattern

</td><td>

The CI type created: \[cmdb\_ci\_compute\_template\]

</td></tr><tr><td>

Discovery and Service Mapping Patterns version 1.0.75

</td><td>

The migration to the new model is done by migration script. See [KB0955939](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0955939)

</td><td>

**Hardware Type \(LP\)** pattern

</td><td>

The CI type created: \[cmdb\_ci\_cloud\_hardware\_type\]

</td></tr><tr><td>

Discovery and Service Mapping Patterns version 1.6.0

</td><td>

The Hardware Type new model is provided OOB, enabled with the system property: **sn\_itom\_pattern.use a single hardware type for cloud datacenters**. For more information, see[KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337).

</td><td>

According to [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337) Flow Diagram

</td><td>

The CI type created: According to [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337)

</td></tr><tr><td>

Discovery and Service Mapping Patterns 1.15.0

</td><td>

The Hardware Type new model is provided OOB enabled with the system property: **sn\_itom\_pattern.use a single hardware type for cloud datacenters**. For more information, see[KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337).

</td><td>

The flow is as described in [KB1285337](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1285337). However, only one pattern executes. The pattern that used to gracefully terminate doesn't execute.

</td><td>

Either **Hardware Type \(LP\)** pattern or **Cloud Hardware Type \(LP\)** pattern executes.

</td></tr></tbody>
</table>## Tag information collected by Discovery during horizontal discovery

When running the patterns, tag information is collected to populate the cmdb\_key\_value table. Each tag is related to a CI that was discovered during the discovery. Tag discovery is done in the extension section of each pattern.

## Data collected by Service Mapping during tag-based discovery

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

-   **[Azure Application Insight Data Collection Rule pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-insight-data-collect-rule.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Application LB pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-application-lb-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure application load balancers on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Blob Storage pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-blob-storage-pattern.md)**  
Discovery and Service Mapping Patterns finds blob resources within Azure Blob Storage on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Classic Load Balancer pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-classic-load-balancer-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Classic Load Balancers on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Cosmos DB for PostgreSQL Cluster pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cosmos-db-postgresql-cluster.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Data Explorer Cluster pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-data-explorer-cluster.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Database pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-database-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure databases, including SQL Server, MySQL, PostgreSQL, Redis, and Azure Cosmos DB, in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Datacenter discovery pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-datacenter-discovery-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Datacenter resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Dev Center pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-dev-center.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Events pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-events-pattern.md)**  
Discovery uses event patterns to update Microsoft Azure Cloud component data in near real-time. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Express Route Circuit pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-express-route-circuit-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Express Route Circuit resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure File Share pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-file-share-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure File Share resources within Storage Accounts on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Firewall Network Security pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-firewall-network-security.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure hardware type pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-hardware-type-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure hardware type configurations on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Host pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-host-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Hosts on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Key Vault Key pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-key-vault-key.md)**  
Discovery and Service Mapping Patterns finds Azure Key Vault Keys on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Local Network Gateway pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-local-network-gateway-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Local Network Gateway resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Log Analytics Workspace pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-log-analytics-workspace.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Marketplace pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-marketplace-lb-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Marketplace products in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure NAT Gateway pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-nat-gateway-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure NAT Gateway resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Network and Subnet pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-network-subnet-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure virtual networks, subnets, and virtual network peerings on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure NIC pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-nic-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure network interfaces Controller \(NIC\) on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure OS image pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-os-image-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure OS images on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Private DNS Zone pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-private-dns-zone-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Private DNS Zone resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Private Gateway pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-private-gateway-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure virtual network gateways on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Public IP pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-public-ip-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure public IP addresses on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Recovery Services Vault pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-recovery-services-vault.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Recovery Services Vault Backup Item pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-recovery-services-vault-backup.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Resource Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-resource-group-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Resource Groups in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Route Table pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-route-table-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Route Tables in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Security Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-security-group-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Security Groups on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Service Endpoint Policy pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-service-endpoint-policy.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure SQL Server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-sql-server-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure SQL Server virtual machines in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Storage Account pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-account-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Storage Accounts in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Storage Containers pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-container-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Storage Containers in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Storage Volume pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-volume-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Storage Volumes \(managed disks\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure sub account pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-sub-account-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure subscriptions and management groups on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Subscriptions Discovery For Management Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-sub-mgmt-group-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Subscription entities under Management Groups on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure virtual machine pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vm-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure virtual machines \(VMs\) on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Virtual Network Gateway Connection pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vng-connection-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure Virtual Network Gateway Connection resources on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure Web Application Firewall Policy pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-web-app-firewall-policy.md)**  
Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Azure WebSite pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-website-pattern.md)**  
Discovery and Service Mapping Patterns finds Azure App Service web applications in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Parent Topic:**[Available cloud discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns-cloud.md)

**Related topics**  


[Kubernetes discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/kubernetes-discovery.md)

[Azure Key Vault certificate discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/azure-certificate-discovery-pattern.md)

[Microsoft Foundry \(classic\) pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-visibility/microsoft-foundry-classic-pattern.md)

