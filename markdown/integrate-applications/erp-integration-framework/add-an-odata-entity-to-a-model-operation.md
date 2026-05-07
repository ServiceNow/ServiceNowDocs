---
title: Add an OData entity to a model operation
description: Specify the OData entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, odata, entity, model, operation]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add an OData entity to a model operation

Specify the OData entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

You must have already added the read, write, or create operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model that you want to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select an operation.

6.  For help finding relevant entities using the **Ask AI** button, see [Use generative AI to help add an entity to a model](use-ai-to-help-add-an-entity-to-a-model.md).

7.  Select **Select entity** on the **Manage entities** tab.

    ![Add operation entities on the manage models tab.](../image/erpc-manage-entities-manager-ys22.png)

8.  In **Select type**, select **OData**.

9.  In **Select service**, specify the OData service to use.

    If you don't see the service you need, add the service by selecting **+ Add service manually**. For more information, see [Add an OData service manually in Zero Copy Connector for ERP](erp-add-a-service-manually.md).

10. Wait for the **OData Endpoints** field to load and then in **Select the endpoints**, specify an endpoint.

    ![Select the type of entity , the odata service, and an odata endpoint.](../image/erp-add-odata-entity-to-model1.png)

11. When you're finished, select **Add entity**.

    The entity card shows the date and time information was last retrieved.

    ![Manage model tab with entity card showing retrieval date and time.](../image/erp-add-odata-entity-to-model2.png)


**Parent Topic:**[Add an entity to a model](../concept/add-an-entity-to-model.md)

