---
title: Set partition size for parallel loading-enabled Azure accounts
description: Optimize the performance of data sources by setting the partition size in the azure\_full\_pull\_partition\_size system property.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [SGC-Azure, SGC-Microsoft Azure, SGC Azure, SGC Microsoft Azure, SGC for Azure, SGC for Microsoft Azure, Azure SGC, Microsoft Azure SGC, Service Graph Connector for Microsoft Azure, Service Graph Connector for Azure, Azure data sources, SG-Azure data sources, SG-Azure, Azure parallel loading, Azure partition size, azure\_full\_pull\_partition\_size]
breadcrumb: [Additional features, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set partition size for parallel loading-enabled Azure accounts

Optimize the performance of data sources by setting the partition size in the **azure\_full\_pull\_partition\_size** system property.

## Before you begin

Set the application scope to Service Graph Connector for Microsoft Azure using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## About this task

The parallel loading feature is available for the following data sources:

-   Starting with the Service Graph Connector for Microsoft Azure 1.13.0 version:
    -   SG-Azure Functions
    -   SG-Azure Generic Resources
    -   SG-Azure Get Run Command
    -   SG-Azure Hardware Template Updation​
    -   SG-Azure HW Consolidation​
    -   SG-Azure Kubernetes Cluster
    -   SG-Azure Load Balancers
    -   SG-Azure Network Interface
    -   SG-Azure Public IP Address
    -   SG-Azure Run Command
    -   SG-Azure Scale Sets VMs
-   Starting with the Service Graph Connector for Microsoft Azure 1.11.0 version:
    -   SG-Azure Network
    -   SG-Azure Virtual Machines
    -   SG-Azure Storage Volume

For a full data pull, the **azure\_full\_pull\_partition\_size** property determines the number of Azure subscriptions that can be executed as parallel jobs to retrieve configuration item \(CI\) data. Partition size determines how many Azure subscriptions a single parallel-thread evaluates for data retrieval. If you set the **azure\_full\_pull\_partition\_size** property to `100`, the partition size is 100 subscriptions.

**Note:** If the **azure\_full\_pull\_partition\_size** property isn't configured, the partition size computation feature of the Integration Commons for CMDB application automatically determines the partition size for parallel loading at runtime. See [Partition size computation for parallel loading in Integration Commons for CMDB](../concept/integration-commons-part-size.md).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Azure** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  From the **Property** column of the Service Graph Connection Properties related list, select **azure\_full\_pull\_partition\_size**.

    The **azure\_full\_pull\_partition\_size** system property determines the number of subscriptions that each partition processes for a full pull. For more information, see [Service Graph Connector for Microsoft Azure properties](../reference/cmdb-sgc-azure-props.md).

4.  In the **Value** field, enter a numeric value greater than `0` for the partition size.

5.  Select **Update**.

    **Note:** After you enable parallel data loading for a data source, the **Test Load 20 Records** and **Load All Records** options don't work for executing the data source. You must select **Execute Now** from **Scheduled Data Import** to execute the data source for which parallel loading is enabled.


