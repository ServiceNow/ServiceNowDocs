---
title: Data mapping for Service Graph Connector for Microsoft Azure
description: Data from the Azure data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-data-mapping-azure.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Microsoft Azure

Data from the Azure data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow® CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Azure

When you complete setting up the connection, you can configure the integration to periodically pull data from Azure. The data is loaded into staging tables and then inserted into the target tables.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI and non-CMDB classes for Azure.

<table id="table_qjc_2tn_41c" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Azure Subscriptions

</td><td>

SG Azure Subscriptions \[sn\_sg\_azure\_integ\_subscriptions\]

</td><td>

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Datacenter Updation

</td><td>

SG-Azure Datacenter Updation \[sn\_sg\_azure\_integ\_datacenter\_updation\]

</td><td>

[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Resource Group

</td><td>

SG-Azure Resource Group \[sn\_sg\_azure\_integ\_resource\_groups\]

</td><td>

[Resource Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Availability Zone

</td><td>

SG-Azure Availability Sets \[sn\_sg\_azure\_integ\_availability\_sets\]

</td><td>

[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Storage Volume

</td><td>

SG-Azure Storage Volume \[sn\_sg\_azure\_integ\_storage\_volume\]

</td><td>

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Load Balancers

</td><td>

SG-Azure Load Balancers \[sn\_sg\_azure\_integ\_load\_balancers\]

</td><td>

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud LB IPAddress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Network

</td><td>

SG-Azure Network \[sn\_sg\_azure\_integ\_network\]

</td><td>

[Cloud Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Public IP Address

</td><td>

SG-Azure Public IP Address \[sn\_sg\_azure\_integ\_public\_ip\_address\]

</td><td>

[Cloud Public IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Mgmt Network Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud LB IPAddress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Security Group

</td><td>

SG-Azure Security Group \[sn\_sg\_azure\_integ\_security\_group\]

</td><td>

[Compute Security Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Storage Accounts

</td><td>

SG-Azure Storage Accounts \[sn\_sg\_azure\_integ\_storage\_accounts\]

</td><td>

[Cloud Storage Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Virtual Machines

</td><td>

SG-Azure Virtual Machine \[sn\_sg\_azure\_integ\_virtual\_machine\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Linux Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Windows Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Network Interface

</td><td>

SG-Azure Network Interface \[sn\_sg\_azure\_integ\_network\_interface\]

</td><td>

[Cloud Mgmt Network Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure SQL

</td><td>

SG-Azure SQL \[sn\_sg\_azure\_integ\_sql\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Functions and WebSites

</td><td>

SG-Azure Functions \[sn\_sg\_azure\_integ\_functions\]

</td><td>

[Cloud WebServer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Generic Resources

</td><td>

SG-Azure Generic Resources \[sn\_sg\_azure\_integ\_generic\_resources\]**Note:** The SG-Azure Generic Resources data source imports data for resources that are categorized as `Generic` in the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.

</td><td>

[Cloud Resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Scale Sets

</td><td>

SG-Azure Scale Sets \[sn\_sg\_azure\_integ\_scale\_sets\]

</td><td>

[Instance Scale Set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Scale Sets VMs

</td><td>

SG-Azure Scale Sets VMs \[sn\_sg\_azure\_integ\_scale\_sets\_vms\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Cloud Mgmt Network Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Linux Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Windows Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Software

</td><td>

SG-Azure Software \[sn\_sg\_azure\_integ\_software\]**Note:** The SG-Azure Software data source imports the software data from the ConfigurationData table in the Log Analytics workspace of Azure.

The SG-Azure Software import is set to inactive by default.

</td><td>

When the Software Asset Management \(SAM\) application isn't installed:

 [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 When the SAM application is installed:

 [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Software Remove

</td><td>

SG-Azure Software Remove \[sn\_sg\_azure\_integ\_software\_remove\]The SG-Azure Software Remove import is set to inactive by default.

</td><td>

When the SAM application isn't installed:

 [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 When the SAM application is installed:

 [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure TCP

</td><td>

SG-Azure TCP \[sn\_sg\_azure\_integ\_tcp\]**Note:** The SG-Azure TCP data source imports the TCP and processes data from the VMConnection and VMProcess tables in the Log Analytics workspace of Azure. To populate the tables, you must first enable the VM insights feature in the Azure portal. For more information, see [Enabling VM insights for collecting Azure data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-azure-vm-insights.md).

</td><td>

TCP Connection

 Running Process

</td></tr><tr><td>

SG-Azure Hardware Template Updation​

</td><td>

Hardware templates \[sn\_sg\_azure\_integ\_hardware\_templates\]

</td><td>

[Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure HW Consolidation

</td><td>

SG-Azure HW Consolidation \[sn\_sg\_azure\_integ\_hw\_consolidation\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 [Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr><tr><td>

SG-Azure Run Command

</td><td>

SG-Azure Run Command \[sn\_sg\_azure\_integ\_run\_command\]

</td><td>

No data created

</td></tr><tr><td>

SG-Azure Get Run Command

</td><td>

SG-Azure Get Run Command \[sn\_sg\_azure\_integ\_get\_run\_command\]

</td><td>

[Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

 TCP Connection

 Running Process

</td></tr><tr><td>

SG-Azure Kubernetes Cluster

</td><td>

SG-Azure Kubernetes Cluster \[sn\_sg\_azure\_integ\_kubernetes\_cluster\]

</td><td>

[Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from Azure, see [CMDB classes targeted in Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md) and [Supported Microsoft Azure resource types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-azure-resource-types.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

Additional information about Azure data sources:

-   The Service Graph Connector for Microsoft Azure utilizes the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table to differentiate between generic resources and other supported resource types.

    Any resource that is not populated in the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table is populated in the Cloud Inventory Resource Inclusion Lists \[sa\_cloud\_inventory\_resource\_whitelist\_list\] table.

-   The SG-Azure Hardware Template Updation and SG-Azure HW Consolidation import schedules replace the SG-Azure Hardware Template import schedule from the Service Graph Connector for Microsoft Azure 1.12.0 version. The SG-Azure Hardware Template Updation and SG-Azure HW Consolidation data sources fetch only the data of the hardware templates that are used for VMs in Azure, instead of fetching all hardware templates.
-   The SG-Azure SQL data source populates the `microsoft.dbformysql/flexibleservers` and `microsoft.dbforpostgresql/flexibleservers` resource types in the Cloud Database \[cmdb\_ci\_cloud\_database\] table instead of the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table from the Service Graph Connector for Microsoft Azure 1.14.0 version.

    After upgrading to version 1.14.0, run a full data load to migrate all active flexible servers from the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table to the Cloud Database \[cmdb\_ci\_cloud\_database\] table.

-   All data sources except SG-Azure Scale Sets VMs are migrated from Azure Resource Manager \(ARM\) APIs to Resource Graph APIs for a full data load from the Service Graph Connector for Microsoft Azure 1.14.0 version. Microsoft Azure doesn't support uniform orchestration-type Scale Set VMs on Resource Graph APIs.
-   The import set rows for the SG-Azure Run Command scheduled import job \[sn\_sg\_azure\_integ\_run\_command\] remain in Pending state even after the import set is processed.

## Related content

[CMDB classes targeted in Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

[Service Graph Connector for Microsoft Azure properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-azure-props.md)

