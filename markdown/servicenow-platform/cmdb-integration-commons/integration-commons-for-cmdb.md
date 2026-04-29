---
title: Integration Commons for CMDB
description: The Integration Commons for CMDB application contains the CMDB Integrations Dashboard and a set of Robust Transform Engine \(RTE\) transforms and script includes.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Integration Commons for CMDB

The Integration Commons for CMDB application contains the CMDB Integrations Dashboard and a set of Robust Transform Engine \(RTE\) transforms and script includes.

Integration Commons for CMDB \(sn\_cmdb\_int\_util\) is available on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Dependencies

CMDB and CSDM Data Foundations Dashboards v2.3.5 or later versions \(see [Monitor health in CSDM and CMDB Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md)\)

## Using the CMDB Integrations Dashboard

The Integration Commons for CMDB application provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors and any custom integrations created in IntegrationHub ETL.

See [CMDB Integrations Dashboard](cmdb-integ-dashboard.md#) for more information.

## Using RTE transforms

The Integration Commons for CMDB \(com.snc.cmdb.integration\_util\) plugin provides the Integration Commons functionality. You can use the transforms and script includes to standardize the values stored in the CMDB by different data integrations or by changes. The attributes included in the Integration Commons for CMDB application are attributes that the Identification and Reconciliation Engine \(IRE\) requires for identification or attributes that could be used to derive classes.

**Note:** The RTE transforms are included in the Integration Commons for CMDB app and are available in the [IntegrationHub ETL](integrationhub-etl.md) app. For more information on RTE transforms, see [RTE operation types included within the Integration Commons for CMDB app](../reference/cmdb-rte-operation-types.md) and [RTE transforms template scripts included within the Integration Commons for CMDB app](../reference/cmdb-rte-transforms.md).

ServiceNow Service Graph Connectors that are available at the ServiceNow Store, have dependencies on the transforms and script includes in the Integration Commons for CMDB app. Therefore, when you install such CMDB integrations, the Integration Commons for CMDB store app is automatically installed too.

You can also configure the Application Dependency Mapping \(ADM\) adapter to populate running processes, TCP connections, and applications into the CMDB. For more information, see [Configuring the ADM adapter for Service Graph Connectors](sgc-common-config-adm.md).

**Important:** After upgrades and deployments of new applications or integrations, run quick start tests to verify that Integration Commons for CMDB works as expected. See [Quick start tests for Integration Commons for CMDB](../../../administer/atf-quick-start-tests/reference/quick-start-tests-integration-commons.md) for more information.

**Related topics**  


[Configuring the ADM adapter for Service Graph Connectors](sgc-common-config-adm.md)

[Accessing the connection details of Service Graph Connectors](integration-commons-conn-fw.md)

[Managing CMDB data deletion](cmdb-integ-record-removal.md)

[Partition size computation for parallel loading in Integration Commons for CMDB](integration-commons-part-size.md)

[Quick start tests for Integration Commons for CMDB](../../../administer/atf-quick-start-tests/reference/quick-start-tests-integration-commons.md)

