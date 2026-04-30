---
title: View and edit the foundation of ERP models
description: Create a holistic data set by building ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP, which encompasses remote tables and extraction tables from the ERP system, as well as read and update operations.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# View and edit the foundation of ERP models

Create a holistic data set by building ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP, which encompasses remote tables and extraction tables from the ERP system, as well as read and update operations.

## Before you begin

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. After enabling the **sn\_erp\_integration.enableModelModification** property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or directly typing `sys_properties.list` in the Navigator Filter.

**Note:** You must enable the **sn\_erp\_integration.enableModelModification** property on the correct scope. Enabling the **sn\_erp\_integration.enableModelModification** on a production instance can create new metadata records when new models and fields are added in Zero Copy Connector for ERP.

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

Zero Copy Connector for ERP provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md).

An ERP model functions as a staging area that contains all potential fields you can add to remote and extraction tables, and read and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

    ![ERP Canvas models page](../image/erp-canvas-models-ys2.png)

3.  Review the list of ERP models.

<table id="table_alp_clm_5xb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP model name

</td><td>

Name of the ERP model.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP model represents.

</td></tr><tr><td>

ERP tables

</td><td>

Number of ERP tables on the system of record.

</td></tr><tr><td>

Extraction tables

</td><td>

Number of extraction tables on the ServiceNow AI Platform that are linked to the ERP model.

</td></tr><tr><td>

Remote tables

</td><td>

Number of remote tables on the ServiceNow AI Platform that are linked to the ERP model.

</td></tr><tr><td>

Updated

</td><td>

Date and time the model was last updated.

</td></tr></tbody>
</table>4.  Select an ERP model to view and edit the details of the model.

    |Field|Description|
    |-----|-----------|
    |ERP model name|Name of the ERP model.|
    |ERP module|Brief name of the ERP business area on the system of record.|
    |ERP system|ERP system that represents a connection to a business section of your ERP system of record.|
    |Application|Application scope the ERP model is linked to. For example, if you create a custom model, the model will be in that scope.|
    |Short description|Brief description of what the ERP model represents.|
    |Long text|Any longer description or information about the ERP data model.|

5.  View and work with the following on the **Details** tab of an ERP model:

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

Updated

</td><td>

Date and time the model entity was last updated.

</td></tr></tbody>
</table>8.  Export the list of tables in the model by selecting the **Export** button.

    You can select the **File type**, such as **JSON** or **Excel**, and the **Delivery type**, such as **Download**.

9.  View and confirm the table entity fields included in the ERP model by selecting the **Entity fields** tab of the ERP model record.

    For a description of the field values, see [Zero Copy Connector for ERP ERP model table field descriptions](../reference/erp-canvas-erp-data-model-table-fields.md).

    ![Table entity fields for an ERP model](../image/erpc-material-stock.png "Zero Copy Connector for ERP table entity fields")


## What to do next

After you have noted the available fields and tables, you can add new table entities to a model by managing the model. When you manage the model, you can also create read and update operations using table reads and BAPIs \(Business Application Programming Interface\). For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

