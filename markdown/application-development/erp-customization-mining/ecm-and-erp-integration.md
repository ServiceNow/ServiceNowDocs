---
title: How ERP-CM works with Zero Copy Connector for ERP and remote tables
description: Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# How ERP-CM works with Zero Copy Connector for ERP and remote tables

Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.

Using Zero Copy Connector for ERP, you can access standard fields for remote tables and ERP extraction tables, while ERP Semantic Mining \(ERP-CM\) enables you to find good candidates for replatforming from the system of record to the ServiceNow AI Platform.

ERP-CM suggests candidates and possible next steps, such as updating remote tables and extraction tables to access ERP data. Remote tables send data to the ServiceNow instance as an attachment, which is then analyzed using AI/ML to identify similar candidates to replatform.

After you've identified candidates to replatform and taken the recommended action in ERP-CM, you need to use only Zero Copy Connector for ERP to access the remote tables and extraction tables. These tables are data sources for building apps, flows, and workspaces.

## Using remote tables and extraction tables with Zero Copy Connector for ERP and ERP-CM

You can use a combination of remote tables and extraction tables to retrieve data from your legacy ERP system.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

Remote tables describe the schema for the data that you want to retrieve from an external source, such as the system of record. Use remote tables to connect the ServiceNow AI Platform to third-party sources, or to another instance, so that you can retrieve external data and optionally cache it in the memory. You can view external data in lists or forms and process it with standard Glide scripts. You can also group, sort, aggregate, and filter the data just like you would for standard internal tables.

By using a remote table, you can retrieve the data from external sources or from another instance with REST or SOAP services. The external data lives in the memory in read-only mode, which makes the data temporary, or transient, within the ServiceNow AI Platform. You can then view and manipulate the external data without importing or storing it. For more information, see [Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Use an extraction table to work with large amounts of ERP data. ERP extraction tables regularly save data to a local transform table on the ServiceNow AI Platform, which you can then process and use as the data foundation of a replatformed app.

**Parent Topic:**[Exploring ERP Semantic Mining](exploring-ecm.md)

