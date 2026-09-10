---
title: View and edit models
description: Create a holistic dataset by building ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP. Models encompass remote tables and extraction tables from the ERP system, as well as create, read, and update operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/view-and-work-with-erp-data-models.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, edit, change, view]
breadcrumb: [ERP models, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# View and edit models

Create a holistic dataset by building ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP. Models encompass remote tables and extraction tables from the ERP system, as well as create, read, and update operations.

## Before you begin

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables.

-   The property must be enabled on the correct scope.
-   After enabling the property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.
-   The property must be configured for either a non-production or production state. \(Enabling the property on a production instance can create metadata records when new models and fields are added in Zero Copy Connector for ERP.\)
-   System properties are maintained in the System Property table \[sys\_properties\], which you can access by entering `sys_properties.list` directly in the Navigator Filter.

Role required: sn\_erp\_integration.erp\_admin

## About this task

A model functions as a staging area that contains all potential fields you can add to remote and extraction tables, as well as, create, read, and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard extraction tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-content-packs.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the models page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

    \[Omitted image "erp-canvas-models-ys2.png"\] Alt text: Zero Copy Connector for ERP models page

3.  Review the list of ERP models.

    |Column|Description|
    |------|-----------|
    |Model name|Name of the model.|
    |Model type|ERP model or Platform model.|
    |Short description|Brief description of what the model represents.|
    |Remote tables|Number of remote tables on the ServiceNow AI Platform that are linked to the ERP model.|
    |Extraction tables|Number of extraction tables on the ServiceNow AI Platform that are linked to the ERP model.|
    |Version|Specific variant of the model.|
    |Updated|Date and time the model was last updated.|

4.  View and work with the following on the **Details** tab of an ERP model:

    -   Public comments and private work notes.
    -   The Activity stream for the model.
    -   File attachments.
5.  Select **Save**.

6.  View and confirm that the table entities included in the model by selecting the **Model entities** tab of the ERP model record.

    View details for an individual table by selecting the table name in the **Model entities** tab.

    Zero Copy Connector for ERP automatically scans the linked ERP system to retrieve the latest entity data. However, you can select the refresh icon to update the data on demand.

<table id="table_g4h_23v_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the model table on the ERP system.

</td></tr><tr><td>

Alias

</td><td>

Alias for the table.The alias refers to an alternative or substitute name for the table. An alias enables you to assign and customize a recognizable name for easier reference and identification.

The alias can be a maximum of 40 characters, and contain a-z, A-Z, 0-9, and underscores.

</td></tr><tr><td>

Status

</td><td>

Status of the data synchronization, such as **Retrieved table data**.

</td></tr><tr><td>

Updates

</td><td>

Number of times the model entity was updated.

</td></tr></tbody>
</table>7.  Export the list of tables in the model by selecting the **Export** button.

    You can select the **File type**, such as **JSON** or **Excel**, and the **Delivery type**, such as **Download**.

8.  View and confirm the table entity fields included in the ERP model by selecting the **Entity fields** tab of the ERP model record.

    For a description of the field values, see [Zero Copy Connector for ERP ERP model table field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-erp-data-model-table-fields.md).

    \[Omitted image "erpc-material-stock.png"\] Alt text: Table entity fields for an ERP model


## What to do next

After you have noted the available fields and tables, you can add new table entities to a model by managing the model. When you manage the model, you can also create read, update, and create operations using table reads and BAPIs \(Business Application Programming Interface\). For more information, see [Exploring Zero Copy Connector for ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/exploring-erp-models.md).

