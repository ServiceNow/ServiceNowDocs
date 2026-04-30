---
title: Service Graph Connector for Google Console
description: Use the Service Graph Connector for Google Console to import device details from Chromebooks into the Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Google Console

Use the Service Graph Connector for Google Console to import device details from Chromebooks into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

-   Get visibility across Chromebook devices.
-   Get started quickly with a streamlined onboarding process.
-   Use only the credentials you need.

## Supported versions

<table id="table_kbm_ghs_2bc"><thead><tr><th>

Google Console

</th><th>

ServiceNow

</th></tr></thead><tbody><tr><td>

Last tested on July 05, 2024

</td><td>

-   Xanadu
-   Washington DC
-   Vancouver
-   Utah

</td></tr></tbody>
</table>## Use cases

You can use the Service Graph Connector for Google Console to get visibility into Google ChromeOS devices, enabling administrators to centrally manage enrollment, configuration, and monitoring these devices.

## Guided setup

The guided setup for the Service Graph Connector for Google Console provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for Google Console](../task/sgc-config-google-console-integ.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Google Console integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Google Console data source is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from the Google Console application.

**Note:** For any discovered resources that were deleted later, the Service Graph Connector for Google Console automatically marks the corresponding records as no longer active or valid in CMDB.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes as where data is stored for a Chromebook device within Google Console.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

CMDB CI classes

</th><th>

Resource type

</th></tr></thead><tbody><tr><td>

SG-GoogleConsole-ChromeDevices

</td><td>

SG-GoogleConsole-ChromeDevices \[sn\_googleconsole\_i\_sg\_googleconsole\_chromedevices\]

</td><td>

[Computer](../reference/sgc-cmdb-google-console-classes.md#section_oms_1jg_4bc)[IP Address](../reference/sgc-cmdb-google-console-classes.md#section_dtc_bjg_4bc)

[Network Adapter](../reference/sgc-cmdb-google-console-classes.md#section_blk_bjg_4bc)

When the Software Asset Management \(SAM\) and SAM Foundation applications are not installed:

[Software](../reference/sgc-cmdb-google-console-classes.md#section_elt_bjg_4bc)

[Software Instance](../reference/sgc-cmdb-google-console-classes.md#section_hbl_cjg_4bc)

When the SAM application, the SAM Foundation application, or both are installed:

[Software Installation](../reference/sgc-cmdb-google-console-classes.md#section_d2c_cjg_4bc)

</td><td>

Chrome OS devices

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from a Chromebook device, see [CMDB classes targeted in Service Graph Connector for Google Console](../reference/sgc-cmdb-google-console-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

