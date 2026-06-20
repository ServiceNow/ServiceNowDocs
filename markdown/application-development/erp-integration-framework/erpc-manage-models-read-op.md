---
title: Add an operation to a model in Zero Copy Connector for ERP
description: Add an operation to an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erpc-manage-models-read-op.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Add an operation to a model in Zero Copy Connector for ERP

Add an operation to an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

-   Read operations retrieve ERP data by either reading a table or using a BAPI.
-   Update operations use a BAPI to write updates to the ERP system.
-   Create operation creates a new instance of the business object in the SAP system.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the ERP model icon \(\[Omitted image "erpc-data-model-icon.png"\] Alt text: ERP model icon\) in the side panel.

3.  Select the model to which you want to add an operation.

4.  Select the **Manage model** button.

    \[Omitted image "erpc-model-operation-page-manager-ys2.png"\] Alt text: Add model operation button appears on the ERP model manager page.

5.  Select **Add model operation**.

6.  Specify the type of operation that you're adding in the **Select type** field of the **Add operation** modal.

    -   **Update** sends data back to write to the ERP system.
    -   **Read** reads and retrieves data from the ERP system and brings it onto the ServiceNow AI Platform.
    -   **Create** is used to create a new instance of the business object in the SAP system.
    \[Omitted image "erpc-add-operation-modal.png"\] Alt text: Specify the type of operation you're adding

7.  Select **Save and continue**.


## Result

The foundation of the operation is created.

## What to do next

Next, you must add the read or update entity to the operation. For more information, see [Add a read, update, or create entity to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-add-entity-to-model-op.md)

You can select the delete icon \(\[Omitted image "trash-outline-24.svg"\] Alt text: Delete icon\) on the operation's card to remove any operations you don't need, or to start over.

**Parent Topic:**[Building and managing ERP models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/work-with-erp-data-models.md)

