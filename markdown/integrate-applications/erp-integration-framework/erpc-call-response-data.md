---
title: Specifying where ERP system data is saved
description: Data that Zero Copy Connector for ERP \(Enterprise Resource Planning\) retrieves from ERP systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, content, pack, model, integration, data hub, zero, copy, connector, sap, system, data, store]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Specifying where ERP system data is saved

Data that Zero Copy Connector for ERP \(Enterprise Resource Planning\) retrieves from ERP systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.

## Adding retrieved data to remote tables and extraction tables

Use the JSON contents of the **Response** in a flow's output to save the ERP data in the following ways:

-   Store the data in a remote table. Remote tables get their records from running an associated script against an external data source.
-   Store the data in an extraction table. Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

When you add mapped fields or parameters as outputs and successfully read or update the ERP system, each parameter appears as a field. You can then add the field to a remote table or an extraction table. Manage the fields for the remote table or extraction table to add the retrieved parameters.

## Using retrieved ERP data in flows

The **Use ERP Data** action returns ERP data in an output data pill called **Response**. The **Response** pill is available when you build a flow in Workflow Studio with the **Use ERP Data** action. The **Response** data pill is available in the following places of the action:

-   The **Outputs** tab
-   The **Output** section in the **Data** pane

You can then add the **Response** data pill or any of the child **record** data pills to a flow to parse the returned JSON.

For example, you can generate a record for each response from the ERP system, making that data available for use on the ServiceNow AI Platform.

**Parent Topic:**[Building and managing models to work with ERP data](work-with-erp-data-models.md)

