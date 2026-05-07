---
title: Using model versioning
description: Use model versioning in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to determine the version of a model on development and production instances.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, version, variant, history]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Using model versioning

Use model versioning in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to determine the version of a model on development and production instances.

## Before you begin

For versioning to take place, the **sn\_erp\_integration.enableModelModification** system property must be set to true on your development instance. For more information about the system property, see [Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

As you work with model records on a development instance, at certain intervals you’re likely to export the model, and then import the model to your production instance. Each time you export a model, the version number increases by one on the development instance. The version number appears in the model list and on individual model records. By checking the model list on your development and production instances, you can easily determine if the most recent version of a model is in use on your production instance.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

    View the **Version** column in the list.

    ![Model list with version column highlighted.](../image/erp-model-versions1.png)

3.  Select a model in the list to open a record.

4.  View the version on the individual model record.

    ![Model record with version number highlighted.](../image/erp-model-versions2.png)


**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

