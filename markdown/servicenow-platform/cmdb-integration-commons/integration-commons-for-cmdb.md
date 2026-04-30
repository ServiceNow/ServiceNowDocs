---
title: Integration Commons for CMDB
description: The Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app contains the CMDB Integrations Dashboard and a set of Robust Transform Engine \(RTE\) transforms and script includes.
locale: en-US
release: xanadu
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Integration Commons for CMDB

The Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app contains the CMDB Integrations Dashboard and a set of Robust Transform Engine \(RTE\) transforms and script includes.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Dependencies

CMDB and CSDM Data Foundations Dashboards v2.3.5 or later versions \(see [Monitor system foundations in the CSDM and the CMDB Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md)\)

## Using the CMDB Integrations Dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors and any custom integrations created in IntegrationHub ETL.

See [CMDB Integrations Dashboard](cmdb-integ-dashboard.md#) for more information.

## Using RTE transforms

The Integration Commons for CMDB \(com.snc.cmdb.integration\_util\) plugin provides the Integration Commons functionality. You can use the transforms and script includes to standardize the values stored in the CMDB by different data integrations or by changes. The attributes that are included in the Integration Commons for CMDB store app are attributes that the Identification and Reconciliation Engine \(IRE\) requires for identification or attributes that could be used to derive classes.

The transforms are common operation types and template scripts available astemplated operations. A templated operation is a transform that controls the logic for the transform. The result is that there can be only a single output. When a transform returns multiple values, then those values are concatenated by a triple pipe \(\|\|\|\). You then must use the split transform to retrieve the values that you’re interested in. The inputs are either a single field or a list of fields. For all but one transform, the inputs are assumed to be a fixed list of fields as described for each of the following individual transform.

**Note:** The RTE transforms are included in the Integration Commons for CMDB store app and are available in the [IntegrationHub ETL](integrationhub-etl.md) store app. For more information on RTE transforms, see[RTE operation types included within the Integration Commons for CMDB app](../reference/cmdb-rte-operation-types.md) and [RTE transforms template scripts included within the Integration Commons for CMDB app](../reference/cmdb-rte-transforms.md).

ServiceNow Service Graph Connectors that are available at the ServiceNow Store, have dependencies on the transforms and script includes in the Integration Commons for CMDB store app. Therefore, when you install such CMDB integration, the Integration Commons for CMDB store app is automatically installed too.

You can also configure the Application Dependency Mapping \(ADM\) adapter to populate running processes, TCP connections, and applications into CMDB. For more information, see [Configuring the ADM adapter for Service Graph Connectors](sgc-common-config-adm.md).

**Important:** After upgrades and deployments of new applications or integrations, run quick start tests to verify that Integration Commons for CMDB works as expected. See [Quick start tests for Integration Commons for CMDB](../../../administer/atf-quick-start-tests/reference/quick-start-tests-integration-commons.md) for more information.

**Related topics**  


[Configuring the ADM adapter for Service Graph Connectors](sgc-common-config-adm.md)

[Accessing the connection details of Service Graph Connectors](integration-commons-conn-fw.md)

[Managing CMDB data deletion](cmdb-integ-record-removal.md)

[Partition size computation for parallel loading in Integration Commons for CMDB](integration-commons-part-size.md)

[Quick start tests for Integration Commons for CMDB](../../../administer/atf-quick-start-tests/reference/quick-start-tests-integration-commons.md)

