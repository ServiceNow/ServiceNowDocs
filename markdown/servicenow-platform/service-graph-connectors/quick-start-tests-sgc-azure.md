---
title: Quick start tests for Service Graph Connector for Microsoft Azure
description: Validate that Service Graph Connector for Microsoft Azure still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Service Graph Connector for Microsoft Azure

Validate that Service Graph Connector for Microsoft Azure still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Service Graph Connector for Microsoft Azure

|Test|Description|Release version|
|----|-----------|---------------|
|SG-Azure Availability Zone|Validate the successful ingestion of the record in the Availability Zone table with the prerequisite parent ingestion.|Utah|
|SG-Azure Data Center|Validate the successful ingestion of multiple records in the Azure Data Center table with the prerequisite parent ingestion.|Utah|
|SG-Azure Functions|Validate the successful ingestion of multiple records in the Cloud Service Account, Data Center, Cloud Database, and Cloud Function.|Utah|
|SG-Azure Generic Resources|Validate the successful ingestion of multiple records in the Cloud Resource and Relations table.|Utah|
|SG-Azure Hardware Template|Validate the successful ingesion of multiple records in the Hardware Template and Compute Template tables.|Utah|
|SG-Azure Load Balancers|Validate the successful ingestion of multiple records in the Load Balancer, Computer Security Group and Relations table with the prerequisite parent ingestion.|Utah|
|SG-Azure Network|Validate the successful ingestion of multiple records in the Network table with the prerequisite parent ingestion.|Utah|
|SG-Azure Network Interface|Validate the successful ingestion of multiple records in the Networks, Public IP Address and Relations table.|Utah|
|SG-Azure Public IP Address|Validate the successful ingestion of multiple records in the Public IP Address, Networks, and Load Balancer tables.|Utah|
|SG-Azure Resource Group|Validate the successful ingestion of records in the Resource Group table.|Utah|
|SG-Azure Scale Sets|Validate the successful ingestion of records in the Scale Sets and Relations tables.|Utah|
|SG-Azure Scale Sets VMs|Validate the successful ingestion of multiple records in the Servers, Virtual Machine Instance, Scale Sets, and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Security Groups|Validate the successful ingestion of multiple records in the Cloud Service Account, Computer Security Group, and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Server Config Data|Validate the successful ingestion of multiple records in the Virtual Machine Instance, Linux Server, and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Software|Validate the successful ingestion of multiple records in the Virtual Machine Instance, Software Records, and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure SQL|Validate the successful ingestion of multiple records in the Data Center, Cloud Database, and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Storage Account|Validate the successful ingestion of multiple records in the Storage Account, Computer Security Group and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Storage Volume|Validate the successful ingestion of multiple records in the Storage Volume, Computer Security Group and Relations tables with the prerequisite parent ingestion.|Utah|
|SG-Azure Subscription|Validate the successful ingestion of records in the Cloud Service Account table.|Utah|
|SG-Azure VMs|Validate the successful ingestion of multiple records in the Virtual Machines, Virtual Machine Instance and Relations tables with prerequisite parent ingestion.|Utah|

To learn more about Service Graph Connector for Microsoft Azure, see [Service Graph Connector for Microsoft Azure](../../../product/configuration-management/concept/cmdb-integration-azure.md).

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

