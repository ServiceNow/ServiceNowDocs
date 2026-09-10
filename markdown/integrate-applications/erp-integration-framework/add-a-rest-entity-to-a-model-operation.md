---
title: Add a REST entity to a model operation
description: Specify the REST entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, rest, entity, model, operation]
breadcrumb: [Connecting to ERP with REST, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a REST entity to a model operation

Specify the REST entity that a Zero Copy Connector for ERP \(Enterprise Resource Planning\) model uses for a read, update, or create operation.

## Before you begin

The read, update, or create operation must be added before an entity can be added to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

The service tables must be populated with any services you want to add using the AI search method. REST services are read from the REST endpoint table.

For an overview of the REST API connector, see [REST API for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-connector.md).

For information about the REST API connector tables added for Zero Copy Connector for ERP, see [REST API connector tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-tables.md).

Oracle E-Business Suite services described by WADL documents are read from the WADL service tables. For more information, see [Oracle E-Business Suite support in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.md)

**Note:** Many REST APIs return deeply nested JSON objects. The connector supports up to three levels of nesting in response mapping. You can define nested levels for both input parameters and output fields in the Model Manager UI.

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select an operation.

6.  Select **Select entity** on the **Manage entities** tab.

7.  In **Select type**, select **REST**.

8.  In **Select service**, specify the REST service to use.

    \[Omitted image "erp-add-rest-entity-to-model7.png"\] Alt text: Add entity page with select service field specified as workday.

    If you don't see the service you need, add the service. For more information, see [Add a REST service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.md).

9.  In **REST Services**, select a **REST service** from the drop-down list.

    The service is listed, along with the endpoint and return type.

    \[Omitted image "erp-add-rest-entity-to-model8.png"\] Alt text: Add entity page with rest service added.

10. Select **Add entity**.

    The entity card shows the date and time when the information was last retrieved.


## What to do next

Take the following actions:

-   Map top-level and nested JSON fields \(up to three levels deep\) to model fields.
-   Configure pagination parameters to control how data is retrieved in batches.
-   Define input parameters and output fields.

