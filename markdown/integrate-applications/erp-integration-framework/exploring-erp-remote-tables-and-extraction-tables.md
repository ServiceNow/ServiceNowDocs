---
title: Exploring Zero Copy Connector for ERP remote tables and extraction tables
description: Configure remote tables and extraction tables to work with data from the ERP \(Enterprise Resource Planning\) system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/exploring-erp-remote-tables-and-extraction-tables.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, remote, extraction, table]
breadcrumb: [Exploring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP remote tables and extraction tables

Configure remote tables and extraction tables to work with data from the ERP \(Enterprise Resource Planning\) system.

In Zero Copy Connector for ERP, use remote tables and extraction tables to obtain ERP data after a model has been configured. They serve the same general purpose but are designed for different data volumes. You can use them together when a single approach isn't enough.

You configure both table types within Zero Copy Connector for ERP and link them to a model that controls which fields are available. Standard remote and extraction tables are included with Zero Copy Connector for ERP automatically \(for areas such as sales, delivery, and procurement\), and custom tables can be created as needed.

## Remote tables

Remote tables get their records from running an associated script against an external data source. Remote tables describe the schema for the data that you need to retrieve from an ERP system. Use remote tables to connect to third-party sources, or to another instance, so that you can retrieve external data and optionally cache it in memory. You can view external data in lists or forms and process it with standard Glide scripts. You can also group, sort, aggregate, and filter the data just like you would for standard internal tables.

\[Omitted image "erp-canvas-explore-remote-tables.png"\] Alt text: Remote table record showing information including name, module, model, and remote table link.

## Extraction tables

Extraction tables are ETL \(extract, transform, and load\) data sources designed for large volumes of data. Instead of querying the ERP system in real time, extraction tables run on a scheduled basis, such as once per day. Extraction tables pull batches of data from the ERP system, save it to a temporary transform table, and then load it into a Glide table using import sets. The data is then available as a persistent, queryable table. Multiple extraction tables can map to the same ERP model, and you can create as many as needed.

\[Omitted image "erp-canvas-explore-extraction-tables.png"\] Alt text: Extraction table record showing information including name, table transform map, target table link, and model.

## Key benefits

Remote tables provide real-time ERP data with no storage overhead. Because remote table data lives in memory and is never stored in ServiceNow, it is what's in the ERP system at the moment of the request. This makes remote tables ideal for looking up information and lightweight integrations where having current data is critical.

Extraction tables provide high-volume batch processing. For large data sets where querying the ERP system on demand is slow or resource-intensive, extraction tables pull bulk data on a schedule and store it locally. This makes it fast to query, supports complex reporting and analysis, and reduces the load on the ERP system by batching requests rather than making real-time calls.

Both remote and extraction tables let you select exactly which fields to expose. Sensitive fields, such as email addresses or birth dates, can be excluded at the table configuration level. All remote tables are additionally secured with ACLs, giving administrators granular control over which users can see which ERP data.

Data obtained through remote and extraction tables is available as a data source for building on top of ERP data. Use the data with applications such as ServiceNow Studio, Workflow Studio flows and playbooks, Table Builder, UI Builder, and Workspace Builder.

## Use cases

A company wants to build a Source-to-Pay workspace that gives procurement teams visibility into open purchase orders. The data set includes hundreds of thousands of PO records across multiple SAP company codes. The procurement team needs to filter, analyze, and report on that data daily, but doesn't need it updated by the minute.

A developer creates an extraction table linked to the Purchase Orders model. They configure a scheduled extraction to run every day, pulling all open POs for the current month from SAP and loading them into a Glide table. The procurement workspace is built on top of that Glide table, giving users fast, filterable access to PO data without hitting SAP on every page load.

For instant needs, such as obtaining the current status of a PO for a supplier, the developer also configures a remote table pointing to the same model. When a procurement team member opens a PO record and needs live data, the remote table queries SAP directly and returns the current value on demand.

