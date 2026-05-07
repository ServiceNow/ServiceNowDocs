---
title: Add a BAPI entity to a model operation
description: Specify the BAPI entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, bapi, entity, model, operation]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a BAPI entity to a model operation

Specify the BAPI entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

You must have already added the read, write, or create operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

This video was recorded in the Zurich release.

Video that shows how to add and delete a model operation entity in Zero Copy Connector for ERP. 

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model that you want to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select an operation.

6.  For help finding relevant entities using the **Ask AI** button, see [Use generative AI to help add an entity to a model](use-ai-to-help-add-an-entity-to-a-model.md).

7.  Select **Select entity** on the **Manage entities** tab.

    ![Add operation entities on the manage models tab.](../image/erpc-manage-entities-manager-ys22.png)

8.  In **Select type**, select **Function call \(BAPIs\)**.

9.  In **Select entity**, specify the BAPI to use.

    ![Select the type of entity you're adding and the specific entity.](../image/erp-add-idoc-entity-to-model1.png)

10. When you're finished, select **Add entity**.

    The entity card shows the date and time information was last retrieved.

    ![Manage model tab with entity card showing retrieval date and time.](../image/erp-add-bapi-entity-to-model2.png)


**Parent Topic:**[Add an entity to a model](../concept/add-an-entity-to-model.md)

