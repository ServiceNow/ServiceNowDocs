---
title: Record removal process in Service Graph Connector for Microsoft Azure
description: The Service Graph Connector for Microsoft Azure uses the Integration Commons record removal process for life cycle management during full data loads. For delta loads, life cycle management of records is based on updates from Microsoft Azure.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-10-12"
reading_time_minutes: 1
breadcrumb: [Reference, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Record removal process in Service Graph Connector for Microsoft Azure

The Service Graph Connector for Microsoft Azure uses the Integration Commons record removal process for life cycle management during full data loads. For delta loads, life cycle management of records is based on updates from Microsoft Azure.

Record removal is the process of handling data that is no longer needed. For any discovered resources deleted later after pulling data, the Service Graph Connector for Microsoft Azure automatically updates the **Install Status** field of the associated CMDB CI classes to indicate any retired or deleted records.

The record removal process in the Service Graph Connector for Microsoft Azure involves marking the **Install Status** of a record as **retired** rather than permanently deleting it from the system. The record remains in the database, making it possible to reference or restore it later. Record removal for Service Graph Connector for Microsoft Azure relies on the Source \[sys\_object\_source table\].

Starting with the Service Graph Connector for Microsoft Azure 1.14.0 version, life cycle management is supported for the following data sources in full data load and delta load:

-   SG-Azure Kubernetes Cluster​
-   SG-Azure Scale Sets​
-   SG-Azure Generic Resources​
-   SG-Azure Functions​
-   SG-Azure SQL​
-   SG-Azure Network Interface​
-   SG-Azure Virtual Machines​
-   SG-Azure Storage Accounts​
-   SG-Azure Security Group​
-   SG-Azure Public IP Address​
-   SG-Azure Network​
-   SG-Azure Load Balancers​
-   SG-Azure Storage Volume​
-   SG-Azure Availability Zone​
-   SG-Azure Resource Group​
-   SG-Azure Subscriptions

When you run a full data load for the first time after upgrading to version 1.14.0, the Install Status of all the records that aren't discovered is set to retired.

**Parent Topic:**[Service Graph Connector for Microsoft Azure reference](sgc-azure-reference.md)

