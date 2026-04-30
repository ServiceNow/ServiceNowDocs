---
title: Add a read table entity to a model operation
description: Specify the read table entity that a Zero Copy Connector for ERP model uses for a read, update, or create operation.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, read, table, entity, model, operation]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Add a read table entity to a model operation

Specify the read table entity that a Zero Copy Connector for ERP model uses for a read, update, or create operation.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

You must have already added the read operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model that you want to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select the **Read** operation.

6.  For help finding relevant entities using the **Ask AI** button, see [Use generative AI to help add an entity to a model](use-ai-to-help-add-an-entity-to-a-model.md).

7.  Select **Select entity** on the **Manage entities** tab.

    ![Add operation entities on the manage models tab.](../image/erpc-manage-entities-manager-ys22.png)

8.  In **Select type**, select **Read table**.

    ![Select the type of entity you're adding.](../image/erpc-add-entity-manager-ys2.png)

    You can select **Preview table data** to view table details before specifying an entity. For more information, see [Preview read table entities in Zero Copy Connector for ERP](erp-canvas-preview-entity.md).

9.  In **Select entity**, specify the read table to use.

    The AI Search for this field can help you find what you're looking for faster, for example by entering `Countries` instead of `T005`.

    For table read operations, you may need to check the **Model entities** tab of the current or another related model to get the table name. Alternatively, ask your SAP admin. For more information, see [View and edit the foundation of ERP models](view-and-work-with-erp-data-models.md).

10. When you're finished, select **Add entity**.

    The entity card shows the date and time information was last retrieved.

    ![Manage model tab with entity card showing retrieval date and time.](../image/erp-add-read-entity-to-model1.png)

11. Rearrange and delete table entities as needed.

    **Important:** Reordering deletes any existing table joins for the reordered entities.

    1.  Select **Rearrange order**, drag the tables to the order that you want, and select **Confirm reorder**.

    2.  To remove any tables you don't need, select the delete icon ![](../../../reuse/icons/product-icons/trash-outline-24.svg) on the card for a table.

        Deleting an entity removes all of its related field mappings and table joins.


**Parent Topic:**[Add an entity to a model](../concept/add-an-entity-to-model.md)

