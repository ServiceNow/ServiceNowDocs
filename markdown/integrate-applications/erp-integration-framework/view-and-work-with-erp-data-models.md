---
title: View and edit the foundation of ERP models
description: Create a holistic dataset by building ERP models in Zero Copy Connector for ERP, which encompasses remote tables and extraction tables from the ERP system, as well as create, read, and update operations.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, edit, change, view]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# View and edit the foundation of ERP models

Create a holistic dataset by building ERP models in Zero Copy Connector for ERP, which encompasses remote tables and extraction tables from the ERP system, as well as create, read, and update operations.

## Before you begin

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. The property must be enabled on the correct scope.After enabling the property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. \(Enabling the property on a production instance can create metadata records when new models and fields are added in Zero Copy Connector for ERP.\) System properties are maintained in the System Property table \[sys\_properties\], which you can access by entering `sys_properties.list` directly in the Navigator Filter.

Role required: sn\_erp\_integration.erp\_admin

## About this task

A model functions as a staging area that contains all potential fields you can add to remote and extraction tables, as well as, create, read, and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a new ERP model](erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](../concept/erp-canvas-content-packs.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

    ![Zero Copy Connector for ERP models page](../image/erp-canvas-models-ys2.png)

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

4.  Select a model to view and edit the details of the model.

<table id="table_hsv_q2v_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model name

</td><td>

Name of the ERP model.

</td></tr><tr><td>

ERP module

</td><td>

Brief name of the ERP business area on the system of record.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that represents a connection to a business section of your ERP system of record.

</td></tr><tr><td>

Application

</td><td>

Application scope the ERP model is linked to. For example, if you create a custom model, the model is in that scope.

</td></tr><tr><td>

Model type

</td><td>

ERP model or Platform model.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP model represents.

</td></tr><tr><td>

Long text

</td><td>

A longer description or information about the ERP data model.

</td></tr><tr><td>

ERP software

</td><td>

Supportability of the model. This field is required because it determines which models can be used with a system. When you create or update a model and specify an ERP system, the software linked to that system is automatically added to this field. You can select additional options from the list. The list contains major SAP versions and doesn't include patch versions. When a model is exported, the ERP software information specified here is included.

</td></tr></tbody>
</table>5.  View and work with the following on the **Details** tab of an ERP model:

    -   Public comments and private work notes.
    -   The Activity stream for the model.
    -   File attachments.
6.  Select **Save**.

7.  View and confirm that the table entities included in the model by selecting the **Model entities** tab of the ERP model record.

    View details for an individual table by selecting the table name in the **Model entities** tab.

    Zero Copy Connector for ERP automatically scans the linked ERP system to retrieve the latest entity data. However, you can select the refresh icon to update the data on demand.

<table id="table_g4h_23v_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the model table on the system of record.

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
</table>8.  Export the list of tables in the model by selecting the **Export** button.

    You can select the **File type**, such as **JSON** or **Excel**, and the **Delivery type**, such as **Download**.

9.  View and confirm the table entity fields included in the ERP model by selecting the **Entity fields** tab of the ERP model record.

    For a description of the field values, see [Zero Copy Connector for ERP ERP model table field descriptions](../reference/erp-canvas-erp-data-model-table-fields.md).

    ![Table entity fields for an ERP model](../image/erpc-material-stock.png "Zero Copy Connector for ERP table entity fields")


## What to do next

After you have noted the available fields and tables, you can add new table entities to a model by managing the model. When you manage the model, you can also create read, update, and create operations using table reads and BAPIs \(Business Application Programming Interface\). For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

