---
title: Add an Oracle REST entity to a model
description: Set the input parameters, headers, and payload template for an Oracle Fusion or Oracle E-Business Suite \(EBS\) REST entity. The model then sends the request to the Oracle service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/add-an-oracle-rest-entity-to-a-model-operation.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, oracle, fusion, rest, model, entity, operation]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add an Oracle REST entity to a model

Set the input parameters, headers, and payload template for an Oracle Fusion or Oracle E-Business Suite \(EBS\) REST entity. The model then sends the request to the Oracle service.

## Before you begin

An Oracle ERP system with a REST connection must be configured. For more information, see [REST API support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-rest-support.md).

A read operation must be added before an entity can be added to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

**Note:** With Oracle EBS models, only the read operation is supported.

Role required: sn\_erp\_integration.erp\_admin

## About this task

This procedure covers the Oracle-specific settings. For the general process of adding a REST entity to a model operation, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select the read operation.

6.  Select **Select entity** on the **Manage entities** tab.

7.  In **Select type**, select **REST**.

8.  In **Select service**, specify the Oracle REST service to use.

    \[Omitted image "erp-add-oracle-rest-entity-to-model1.jpg"\] Alt text: Add entity page with oracle typed into select service field and two options displayed.

    If you don't see the service you need, add the service. For more information, see [Add a WADL service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.md).

9.  In **REST Services**, select a **REST service** from the drop-down list.

    The service is listed, along with the endpoint and return type.

    \[Omitted image "erp-add-oracle-rest-entity-to-model2.jpg"\] Alt text: Add entity page with Oracle rest service added.

10. Select **Add entity**.

    The entity card shows the date and time when the information was last retrieved.


