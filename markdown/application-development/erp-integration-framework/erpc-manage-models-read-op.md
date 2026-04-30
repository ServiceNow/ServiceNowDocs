---
title: Add an operation to a model in ERP Data Hub
description: Add an operation to an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Add an operation to a model in ERP Data Hub

Add an operation to an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

-   Read operations retrieve ERP data by either reading a table or using a BAPI.
-   Update operations use a BAPI to write updates to the ERP system.
-   Create operation creates a new instance of the business object in the SAP system. \(Available starting in Xanadu Store Release 2\)

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP model page by selecting the ERP model icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the model to which you want to add an operation.

4.  Select the **Manage model** button.

    ![Add model operation button appears on the ERP model manager page](../image/erpc-model-operation-page-manager.png "ERP model manager page")

5.  Select **Add model operation**.

6.  Specify the type of operation that you're adding in the **Select type** field of the **Add operation** modal.

    -   **Update** sends data back to write to the ERP system.
    -   **Read** reads and retrieves data from the ERP system and brings it onto the ServiceNow AI Platform.
    -   **Create** is used to create a new instance of the business object in the SAP system. \(Available starting in Xanadu Store Release 2\)
    ![Specify the type of operation you're adding](../image/erpc-add-operation-modal.png "Add operation")

7.  Select **Save and continue**.


## Result

The foundation of the operation is created.

## What to do next

Next, you must add the read or update entity to the operation. For more information, see [Add a read, update, or create entity to a model in ERP Data Hub](erpc-add-entity-to-model-op.md)

You can select the delete icon \(![Delete icon](../../../reuse/icons/product-icons/trash-outline-24.svg)\) on the operation's card to remove any operations you don't need, or to start over.

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

