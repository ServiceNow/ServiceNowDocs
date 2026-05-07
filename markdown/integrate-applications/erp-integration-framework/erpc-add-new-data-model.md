---
title: Create a model
description: Add a model in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to create a dataset containing ERP tables from the system of record to read and send updates to the ERP system.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, create, new, build]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Create a model

Add a model in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to create a dataset containing ERP tables from the system of record to read and send updates to the ERP system.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

This video was recorded in the Zurich release.

Video that shows how to create a custom model in Zero Copy Connector for ERP. 

## About this task

A model functions as a staging area that contains all potential fields you can add to remote and extraction tables, as well as, create, read, and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select **New**.

4.  On the new model tab, fill in the fields.

    For a description of the field values, see [Zero Copy Connector for ERP new model field descriptions](../reference/erp-canvas-new-model-descriptions.md).

5.  Select **Save**.

6.  Open the ERP models page again by selecting the models icon ![](../image/erpc-data-model-icon.png).

7.  Update the page by selecting the refresh list icon.

    The new model is displayed in the list.


## What to do next

After you add a new ERP model, specify additional criteria. For example, which tables it reads and joins, any parameters for inputs and outputs, and whether it uses a BAPI to update the system of record. For more information, see the following topics:

-   [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md)
-   [Add joins between ERP tables](erp-canvas-add-join-data-model.md)

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

