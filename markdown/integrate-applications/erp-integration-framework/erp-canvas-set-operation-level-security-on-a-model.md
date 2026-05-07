---
title: Set operation-level security on a model
description: Control access to model operations with user roles and groups.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, model, security, operation, model security, integration, data hub, zero, copy, connector, sap]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Set operation-level security on a model

Control access to model operations with user roles and groups.

You must have the sn\_erp\_integration.erp\_admin role to create and edit models.

In Zero Copy Connector for ERP \(Enterprise Resource Planning\), new permission rules for model operations require you to have a specified role or be part of a specified user group to execute model operations. Each model operation must have at least one user role or one user group specified. You can add multiple user roles and groups as needed.

On a single model, different operations can have different permissions. For example, a financial data model can have some users with only read access to review data, but they can't update or create a financial record. For that same model, other users or groups can be given access to update and create financial records.

![Manage model page with create, read, and update operations that have user or group roles assigned for security.](../image/erp-operation-security1.png)

To help prevent disruptions, all existing model operations have been assigned the admin role and the erp\_user role by default.

You can edit these permissions on the existing operations at any time to suit your needs. To change the permissions, select the edit \(pencil\) icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg) on the model operation card.

![Manage model page with create, read, and update operations that have the admin and erp_user role assigned.](../image/erp-operation-security2.png)

To learn more about adding an operation, see [Add an operation to a model in Zero Copy Connector for ERP](../task/erpc-manage-models-read-op.md).

To clone a model, you must have permissions to access the model operations. For more information, see [Clone an ERP model in Zero Copy Connector for ERP](../task/erp-canvas-clone-data-model.md).

**Parent Topic:**[Building and managing models to work with ERP data](work-with-erp-data-models.md)

