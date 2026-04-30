---
title: Service Graph Connector for Infoblox
description: Use the Service Graph Connector for Infoblox to pull data from an Infoblox instance into your ServiceNow instance.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Infoblox

Use the Service Graph Connector for Infoblox to pull data from an Infoblox instance into your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported versions: Infoblox API v2.11.2
-   Supported ServiceNow versions:
    -   Yokohama
    -   Zurich
    -   Australia

## Use cases

The following example use cases describe how you can use the Service Graph Connector for Infoblox for different ServiceNow® applications:

-   Configure the Infoblox connection for connecting to an Infoblox instance.
-   Create IP address management \(IPAM\) tasks when subnets are added or deleted.
-   Schedule periodic synchronization of IPAM CIs by configuring scheduled data imports jobs.
-   View imported IPAM CIs and IPAM tasks.

## Important information for upgrading Service Graph Connector for Infoblox

You must run a full data load after upgrading to Service Graph Connector for Infoblox version 1.5.0. After the full data load, all CIs from Service Graph Connector for Infoblox version 1.4.0 and earlier are marked as `retired`. You can decide whether to delete or retain the retired CIs.

You can create table cleanup jobs to automate the cleanup of retired CIs based on your organization's data retention requirements and integration dependencies. For more information, see [Create table cleanup jobs for Service Graph Connector for Infoblox](../task/sgc-infoblox-create-table-cleanup-jobs.md).

The source native keys \(SNKs\) for all CIs in Service Graph Connector for Infoblox version 1.5.0 and later include the Managed Network information to identify the connection that discovered specific CIs and to prevent duplicate records. All new CIs that are created after the initial full data load have updated SNKs.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Infoblox using SGC Central](../../sgc-central/task/sgcc-configure-infoblox-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Infoblox integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Additional resource

[Infoblox 1.5: What's New and Post-Upgrade Configuration \[KB2779014\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2779014) article in the Now Support Knowledge Base

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Data mapping for Service Graph Connector for Infoblox](../reference/cmdb-data-mapping-infoblox.md)

[CMDB classes targeted in Service Graph Connector for Infoblox](../reference/sgc-cmdb-infoblox-classes.md)

[Handling parallel data loading in Service Graph Connector for Infoblox](sgc-cmdb-infoblox-parallel-loading.md)

[Life cycle management of records in Service Graph Connector for Infoblox](sgc-cmdb-infoblox-lc.md)

[Service Graph Connector for Infoblox properties](../reference/cmdb-sgc-infoblox-props.md)

