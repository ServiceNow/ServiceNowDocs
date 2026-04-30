---
title: Clone an ERP model in ERP Data Hub
description: Clone a standard ERP \(Enterprise Resource Planning\) model that ships with ERP Data Hub. After you clone the model you can make modifications, for example, by adding new fields or tables.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Clone an ERP model in ERP Data Hub

Clone a standard ERP \(Enterprise Resource Planning\) model that ships with ERP Data Hub. After you clone the model you can make modifications, for example, by adding new fields or tables.

## Before you begin

Your administrator must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. After you enable the **sn\_erp\_integration.enableModelModification** property, ERP Data Hub retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or directly typing `sys_properties.list` in the Navigator Filter.

**Note:** You must enable the **sn\_erp\_integration.enableModelModification** property on the correct scope. Enabling the **sn\_erp\_integration.enableModelModification** on a production instance can create new metadata records when new models and fields are added in ERP Data Hub.

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

ERP Data Hub provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for ERP Data Hub](../reference/erp-canvas-standard-extraction-tables.md).

Cloning ERP models to make customizations ensures that your changes don't break connections to other ServiceNow AI Platform applications.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the name of ERP model that you want to clone.

4.  Select the **Clone model** button.

5.  In the **Clone this model** modal, enter the new **ERP model name**.

6.  Select **Clone this model**.

    ERP Data Hub clones the model and displays a success message.

7.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\).

8.  In the **ERP model name** column, select the cloned model you created.

9.  Change the details for the ERP model on the **Details** tab, such as by updating the name.

    **Warning:** Changing the ERP system connected to the ERP model affects the available remote tables and extraction tables. If you change the ERP system, you must confirm the change on a warning modal.

    For a description of the field values, see [ERP Data Hub clone model field descriptions](../reference/erp-canvas-clone-model-fields.md).


## What to do next

Next, manage the model to specify additional criteria, such as which tables it reads and joins, as well as defining read and update operations and input/output parameters. For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

