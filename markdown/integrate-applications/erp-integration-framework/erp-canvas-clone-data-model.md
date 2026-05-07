---
title: Clone an ERP model in Zero Copy Connector for ERP
description: Clone a standard ERP \(Enterprise Resource Planning\) model that ships with Zero Copy Connector for ERP. After you clone the model you can make modifications, such as adding new fields or tables.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, clone, duplicate, copy, model]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Clone an ERP model in Zero Copy Connector for ERP

Clone a standard ERP \(Enterprise Resource Planning\) model that ships with Zero Copy Connector for ERP. After you clone the model you can make modifications, such as adding new fields or tables.

## Before you begin

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables.

-   The property must be enabled on the correct scope.
-   After enabling the property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.
-   The property must be configured for either a non-production or production state. \(Enabling the property on a production instance can create metadata records when new models and fields are added in Zero Copy Connector for ERP.\)
-   System properties are maintained in the System Property table \[sys\_properties\], which you can access by entering `sys_properties.list` directly in the Navigator Filter.

Role required: sn\_erp\_integration.erp\_admin

## About this task

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a model](erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](../concept/erp-canvas-content-packs.md).

Clone ERP models to make customizations so that your changes don't break connections to other ServiceNow AI Platform applications.

**Note:** You must have permissions to access the model operations to clone a model. For more information, see [Set operation-level security on a model](../concept/erp-canvas-set-operation-level-security-on-a-model.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the name of the ERP model that you want to clone.

4.  Select **Clone**.

5.  In the **Clone this model** modal, enter the new **ERP model name**.

    ![Clone this model modal.](../image/erpc-clone-model.png)

    **Note:** The **Target application** field lists the scope in which the original model was created. The same scope is used for the clone.

6.  Select **Clone this model**.

    The cloned model is created and opens in a new tab.

7.  Change information about the cloned model on the **Details** tab, such as updating the name.

    **Warning:** Changing the ERP system connected to the ERP model affects the available remote tables and extraction tables. If you change the ERP system, you must confirm the change on a warning modal.

    For a description of the field values, see [Zero Copy Connector for ERP clone model field descriptions](../reference/erp-canvas-clone-model-fields.md).


## What to do next

Next, manage the model to specify additional criteria, such as the tables it reads and joins. You can also define create, read, and update operations, and input/output parameters. For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

