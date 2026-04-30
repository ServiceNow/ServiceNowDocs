---
title: Add an operation to a model in Zero Copy Connector for ERP
description: Add an operation to an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Add an operation to a model in Zero Copy Connector for ERP

Add an operation to an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

-   Read operations retrieve ERP data by either reading a table or using a BAPI.
-   Update operations use a BAPI to write updates to the ERP system.
-   Create operation creates a new instance of the business object in the SAP system.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the ERP model icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the model to which you want to add an operation.

4.  Select the **Manage model** button.

    ![Add model operation button appears on the ERP model manager page.](../image/erpc-model-operation-page-manager-ys2.png)

5.  Select **Add model operation**.

6.  Specify the type of operation that you're adding in the **Select type** field of the **Add operation** modal.

    -   **Update** sends data back to write to the ERP system.
    -   **Read** reads and retrieves data from the ERP system and brings it onto the ServiceNow AI Platform.
    -   **Create** is used to create a new instance of the business object in the SAP system.
    ![Specify the type of operation you're adding](../image/erpc-add-operation-modal.png "Add operation")

7.  Select **Save and continue**.


## Result

The foundation of the operation is created.

## What to do next

Next, you must add the read or update entity to the operation. For more information, see [Add a read, update, or create entity to a model in Zero Copy Connector for ERP](erpc-add-entity-to-model-op.md)

You can select the delete icon \(![Delete icon](../../../reuse/icons/product-icons/trash-outline-24.svg)\) on the operation's card to remove any operations you don't need, or to start over.

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

