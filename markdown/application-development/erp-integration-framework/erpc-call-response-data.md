---
title: Specifying where the ERP system data is saved
description: Data that ERP Data Hub retrieves from ERP \(Enterprise Resource Planning\) systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Specifying where the ERP system data is saved

Data that ERP Data Hub retrieves from ERP \(Enterprise Resource Planning\) systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.

## Adding retrieved data to remote tables and extraction tables

Use the JSON contents of the **Response** in a flow's output to save the ERP data in the following ways:

-   Store the data in a remote table. Remote tables get their records from running an associated script against an external data source.
-   Store the data in an extraction table. Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

When you add mapped fields or parameters as outputs and successfully read or update the ERP system, each parameter appears as a field that you can then add to a remote table or an extraction table. Manage the fields for the remote table or extraction table to add the retrieved parameters. For more information, see the following topics:

-   [Customize fields for an ERP remote table in ERP Data Hub](../task/erp-canvas-build-remote-table.md)
-   [Select fields for an extraction table in ERP Data Hub](../task/erpc-select-extraction-table-fields.md)

## Using retrieved ERP data in flows

The **Use ERP Data** action returns ERP data in an output data pill called **Response**. The **Response** pill is available when you build a flow in Workflow Studio with the **Use ERP Data** action. The **Response** data pill is available in the following places of the action:

-   The **Outputs** tab
-   The **Output** section in the **Data** pane

You can then add the **Response** data pill or any of the child **record** data pills to a flow to parse the returned JSON.

For example, you can generate a record for each response from the ERP system, making that data available for use on the ServiceNow AI Platform. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](work-with-erp-data-models.md)

