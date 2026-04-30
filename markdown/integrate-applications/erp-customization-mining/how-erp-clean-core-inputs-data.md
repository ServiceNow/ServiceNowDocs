---
title: How ERP Semantic Mining extracts and processes data
description: ERP Semantic Mining retrieves data from the ERP \(Enterprise Resource Planning\) system using extractors and processes it before the data is available on the ServiceNow AI Platform.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, ERP Semantic Mining overview, Workflow Data Fabric]
---

# How ERP Semantic Mining extracts and processes data

ERP Semantic Mining retrieves data from the ERP \(Enterprise Resource Planning\) system using extractors and processes it before the data is available on the ServiceNow AI Platform.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Use an SAP extractor to analyze the ERP data sources and validate the syntax. The following extractors are available to retrieve data from the ERP system:

-   APPstats
-   COMPHIER
-   SQLM

The supported extractors process data using ServiceNow AI Platform tables.

<table id="table_kbr_d4d_rzb"><thead><tr><th>

Extractor

</th><th>

Full name

</th><th>

Description

</th><th>

ServiceNow AI Platform processing tables

</th><th>

Populated ServiceNow AI Platform tables

</th></tr></thead><tbody><tr><td>

APPstats

</td><td>

Application Statistics

</td><td>

Collects and analyzes system-level statistics and performance metrics from the ERP application.

</td><td>

sn\_erp\_mining\_erp\_appstat\_data\_staging

 sn\_erp\_mining\_erp\_appstat\_data\_aggr

</td><td>

sn\_erp\_mining\_erp\_application

 sn\_erp\_mining\_erp\_user

</td></tr><tr><td>

COMPHIER

</td><td>

Component Hierarchy

</td><td>

Analyzes the hierarchy and relationships among different components at SAP, including business processes and module configurations.

</td><td>

sn\_erp\_mining\_erp\_comp\_hier\_data\_staging

 sn\_erp\_mining\_erp\_comp\_hier\_data\_aggr

</td><td>

sn\_erp\_mining\_erp\_application

 sn\_erp\_mining\_erp\_module

</td></tr><tr><td>

SQLM

</td><td>

SQL Monitor

</td><td>

Enables the monitoring of all SQL statements and operations that are executed by running ABAP applications. The data collected by SQLM provides aggregated performance indicators \(such as the number of executions, execution time, or number of effected rows\) for all executed database operations.

</td><td>

sn\_erp\_mining\_erp\_sqlm\_data\_staging

 sn\_erp\_mining\_erp\_sqlm\_data\_aggr

</td><td>

sn\_erp\_mining\_erp\_application

 sn\_erp\_mining\_erp\_table

 sn\_erp\_mining\_erp\_application\_table

 sn\_erp\_mining\_erp\_application\_usage

</td></tr></tbody>
</table>**Parent Topic:**[Exploring ERP Semantic Mining](exploring-ecm.md)

