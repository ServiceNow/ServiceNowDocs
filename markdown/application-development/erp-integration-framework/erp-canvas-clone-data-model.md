---
title: Clone an ERP model in Zero Copy Connector for ERP
description: Clone a standard ERP \(Enterprise Resource Planning\) model that ships with Zero Copy Connector for ERP. After you clone the model you can make modifications, for example, by adding new fields or tables.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Clone an ERP model in Zero Copy Connector for ERP

Clone a standard ERP \(Enterprise Resource Planning\) model that ships with Zero Copy Connector for ERP. After you clone the model you can make modifications, for example, by adding new fields or tables.

## Before you begin

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. After enabling the **sn\_erp\_integration.enableModelModification** property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or directly typing `sys_properties.list` in the Navigator Filter.

**Note:** You must enable the **sn\_erp\_integration.enableModelModification** property on the correct scope. Enabling the **sn\_erp\_integration.enableModelModification** on a production instance can create new metadata records when new models and fields are added in Zero Copy Connector for ERP.

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

Zero Copy Connector for ERP provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md).

Cloning ERP models to make customizations ensures that your changes don't break connections to other ServiceNow AI Platform applications.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the ERP models icon \(![](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the name of ERP model that you want to clone.

4.  Select **Clone**.

5.  In the **Clone this model** modal, enter the new **ERP model name**.

    ![Clone this model modal.](../image/erpc-clone-model.png)

    **Note:** For your reference, the **Target application** field lists the scope in which the original model was created. The same scope is used for the clone.

6.  Select **Clone this model**.

    Zero Copy Connector for ERP clones the model and displays a success message.

7.  Open the ERP models page by selecting the ERP models icon \(![](../image/erpc-data-model-icon.png)\).

8.  Select the refresh list model icon ![](../../../reuse/icons/product-icons/sync-fill-24.svg).

9.  In the **ERP model name** column, select the cloned model you created.

10. In **ERP softwares**, specify the systems that this model can be used with, for example, ECC 7.5 and SAP S/4HANA 2021.

11. Change information about the ERP model on the **Details** tab, such as updating the name.

    **Warning:** Changing the ERP system connected to the ERP model affects the available remote tables and extraction tables. If you change the ERP system, you must confirm the change on a warning modal.

    For a description of the field values, see [Zero Copy Connector for ERP clone model field descriptions](../reference/erp-canvas-clone-model-fields.md).


## What to do next

Next, manage the model to specify additional criteria, such as which tables it reads and joins, as well as defining read and update operations and input/output parameters. For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

