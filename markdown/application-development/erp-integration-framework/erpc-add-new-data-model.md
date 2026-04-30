---
title: Add a new ERP model
description: Add an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to create a data set that contains ERP tables from the system of record, and enables you to read and send updates to the ERP system.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Add a new ERP model

Add an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to create a data set that contains ERP tables from the system of record, and enables you to read and send updates to the ERP system.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

An ERP model functions as a staging area that contains all potential fields you can add to remote and extraction tables, and read and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select **New**.

4.  On the new model tab, fill in the fields.

    For a description of the field values, see [ERP Data Hub new model field descriptions](../reference/erp-canvas-new-model-descriptions.md).

5.  Select **Save**.

6.  Open the ERP models page again by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\).

7.  Update the page by selecting the refresh list icon.

    The new model is displayed in the list.


## What to do next

After you add a new ERP model, you can manage it to specify additional criteria, such as which tables it reads and joins, any parameters for inputs and outputs, and whether it uses a BAPIs \(Business Application Programming Interface\) to update the system of record. For more information, see the following topics:

-   [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md)
-   [Add joins between ERP tables](erp-canvas-add-join-data-model.md)

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

