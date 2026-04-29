---
title: Service Graph Connector for GCP
description: Use the Service Graph Connector for GCP to ingest CMDB data from a Google Cloud Platform \(GCP\) project using the REST APIs.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for GCP

Use the Service Graph Connector for GCP to ingest CMDB data from a Google Cloud Platform \(GCP\) project using the REST APIs.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

-   Get started quickly with a streamlined onboarding process.
-   Use only the credentials you need.
-   No MID Server required.
-   Get end-to-end data coverage.
-   No agents or individual scanning needed.
-   Performant at scale.

## Supported versions

<table id="table_oyh_yfs_2bc"><thead><tr><th>

GCP

</th><th>

ServiceNow

</th></tr></thead><tbody><tr><td>

Last tested on February 26, 2026

</td><td>

-   Yokohama
-   Zurich
-   Australia

</td></tr></tbody>
</table>## Use cases

You can use the Service Graph Connector for GCP to get visibility into cloud resource identities, relationships, and state in real-time.

## Important information for upgrading Service Graph Connector for GCP

After you've installed the latest version of the Service Graph Connector for GCP, you must synchronize the newly added data sources. Use the Advanced Setup section in the guided setup to synchronize data sources. For more information, see [Configure Service Graph Connector for GCP](../task/sgc-config-gcp-integration.md).

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for GCP using SGC Central](../../sgc-central/task/sgcc-configure-gcp-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring GCP integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## BYOL and BYOS support

Bringing your own licenses \(BYOL\) or bringing your own subscriptions \(BYOS\) is the process of bringing previously purchased on-premises licenses or subscriptions to Google Cloud. The connector supports the BYOL and BYOS of the Image CIs for the Red Hat Enterprise Linux \(RHEL\) and SUSE Linux Enterprise Server \(SLES\) services on Google Cloud. The connector populates the Key Value \[cmdb\_key\_value\] table with the licensing information. Depending on the platform usage, the key is set to either `Windows_OS_License_Type_automatic` or `Linux_OS_License_Type_automatic`, and the key value is set to either `BYOL` or `BYOS`.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Data mapping for Service Graph Connector for GCP](../reference/cmdb-data-mapping-gcp.md)

[CMDB classes targeted in Service Graph Connector for GCP](../reference/sgc-cmdb-gcp-classes.md)

[GCP discovery solutions comparison](../../it-operations-management/reference/gcp-discovery-methods.md)

[Handling import failures for large GCP resources](sgc-cmdb-large-data-vol.md)

[Deep discovery for Service Graph Connector for GCP](sgc-gcp-deep-discovery.md)

[Life cycle management of records in Service Graph Connector for GCP](sgc-cmdb-gcp-lc.md)

