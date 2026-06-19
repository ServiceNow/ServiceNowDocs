---
title: Add an OData entity to a model operation
description: Specify the OData entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/add-an-odata-entity-to-a-model-operation.html
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

You must have already added the read, write, or create operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model that you want to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select an operation.

6.  Select **Select entity** on the **Manage entities** tab.

    \[Omitted image "erpc-manage-entities-manager-ys22.png"\] Alt text: Add operation entities on the manage models tab.

7.  In **Select type**, select **OData**.

8.  In **Select service**, specify the OData service to use.

    If you don't see the service you need, add the service by selecting **+ Add service manually**. For more information, see [Add an OData service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-service-manually.md).

9.  Wait for the **OData Endpoints** field to load and then in **Select the endpoints**, specify an endpoint.

    \[Omitted image "erp-add-odata-entity-to-model1.png"\] Alt text: Select the type of entity , the odata service, and an odata endpoint.

10. When you're finished, select **Add entity**.

    The entity card shows the date and time information was last retrieved.

    \[Omitted image "erp-add-odata-entity-to-model2.png"\] Alt text: Manage model tab with entity card showing retrieval date and time.


**Parent Topic:**[Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-entity-to-model.md)

