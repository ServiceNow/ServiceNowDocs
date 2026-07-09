---
title: Add an IDoc entity to a model operation
description: Specify the IDoc entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for an update or create operation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/add-an-idoc-entity-to-a-model-operation.html
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

You must have already added the create or update operation before you can add an entity to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

Explore the API for interacting with Zero Copy Connector for ERP models. For detailed information and examples for using the API, see .

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model that you want to add an IDoc operation entity to.

    If you need to create a model, see [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md).

4.  Select the **Manage model** button.

5.  Select a Create or Update operation \(IDoc cannot be used with Read operations\).

6.  Select **Select entity**.

7.  In **Select type**, select **IDoc**.

8.  In **Select message**, enter an IDoc message type, for example ORDERS.

9.  Select the basic type or extension, for example, ORDERS05.

10. When you're finished, select **Add entity**.

    \[Omitted image "erp-add-idoc-entity-to-model1.png"\] Alt text: Add idoc entity details filled in and add entity button highlighted.

    The metadata is retrieved. The entity card shows the date and time information was last retrieved.

    \[Omitted image "erp-add-idoc-entity-to-model2.png"\] Alt text: IDoc operation entities card with retrieval date and time.


**Parent Topic:**[Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-entity-to-model.md)

