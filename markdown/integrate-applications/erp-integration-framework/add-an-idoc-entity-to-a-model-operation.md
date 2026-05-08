---
title: Add an IDoc entity to a model operation
description: Specify the IDoc entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for an update or create operation.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, idoc, entity, model, operation]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add an IDoc entity to a model operation

Specify the IDoc entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for an update or create operation.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

You must have already added the create or update operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

Explore the API for interacting with Zero Copy Connector for ERP models. For detailed information and examples for using the API, see sn\_erp\_integration API - Scoped, Global.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model that you want to add an IDoc operation entity to.

    If you need to create a model, see [Create a model](erpc-add-new-data-model.md).

4.  Select the **Manage model** button.

5.  Select a Create or Update operation \(IDoc cannot be used with Read operations\).

6.  For help finding relevant entities using the **Ask AI** button, see [Use generative AI to help add an entity to a model](use-ai-to-help-add-an-entity-to-a-model.md).

7.  Select **Select entity**.

8.  In **Select type**, select **IDoc**.

9.  In **Select message**, enter an IDoc message type, for example ORDERS.

10. Select the basic type or extension, for example, ORDERS05.

11. When you're finished, select **Add entity**.

    ![Add idoc entity details filled in and add entity button highlighted.](../image/erp-add-idoc-entity-to-model1.png)

    The metadata is retrieved. The entity card shows the date and time information was last retrieved.

    ![IDoc operation entities card with retrieval date and time.](../image/erp-add-idoc-entity-to-model2.png)


**Parent Topic:**[Add an entity to a model](../concept/add-an-entity-to-model.md)

