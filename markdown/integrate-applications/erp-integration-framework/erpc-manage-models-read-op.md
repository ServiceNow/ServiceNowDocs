---
title: Add an operation to a model in Zero Copy Connector for ERP
description: Add an operation to an ERP model in Zero Copy Connector for ERP to define how the model retrieves data, writes data, or creates a new instance of the business object.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, operation, create, update, read, crud]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Add an operation to a model in Zero Copy Connector for ERP

Add an operation to an ERP model in Zero Copy Connector for ERP to define how the model retrieves data, writes data, or creates a new instance of the business object.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

This video was recorded in the Zurich release.

Video that shows how to add an operation to a model in Zero Copy Connector for ERP. 

-   Read operations retrieve ERP data by reading a table or using a BAPI, RFC, or OData.
-   Update operations use a BAPI, RFC, OData, or IDoc to write updates to the ERP system.
-   Create operations use a BAPI, RFC, OData, or IDoc to create an instance of the business object in the SAP system.

**Note:** For update operations where ETag is required and OData services are used, the ETag is fetched by default and sent with the update call. Verify that you don't make overriding changes.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model to which you want to add an operation.

4.  Select the **Manage model** button.

5.  Select **Add model operation**.

    ![Add model operation button appears on the ERP model manager page.](../image/erpc-model-operation-page-manager-ys2.png)

6.  In the **Select type** field of the **Add operation** modal, specify the type of operation you're adding.

    -   **Update** sends data back to write to the ERP system.
    -   **Read** reads and retrieves data from the ERP system and brings it onto the ServiceNow AI Platform.
    -   **Create** is used to create a new instance of the business object in the SAP system.
    ![Specify the type of operation you're adding](../image/erpc-add-operation-modal.png)

7.  Select at least one user role or group that can read or run the model operation.

    To prevent disruptions, all existing model operations have been assigned the admin role and the erp\_user role by default. You can edit these permissions on the existing operations at any time to suit your needs. To change the permissions, select the edit \(pencil\) icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg) on the model operation card. For more information about model operation security, see [Set operation-level security on a model](../concept/erp-canvas-set-operation-level-security-on-a-model.md).

8.  Select **Save and continue**.

    The operation tile is displayed with the roles and groups you added.

    ![Manage model page with create, read, and update operations that have user or group roles assigned for security.](../image/erp-operation-security1.png)


## Result

The foundation of the operation is created.

## What to do next

Next, you must add the read or update entity to the operation. For more information, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

You can select the delete icon \(![](../../../reuse/icons/product-icons/trash-outline-24.svg)\) on the operation's card to remove any operations you don't need, or to start over.

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

