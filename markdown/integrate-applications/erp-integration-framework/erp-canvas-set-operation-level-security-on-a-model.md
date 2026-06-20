---
title: Set operation-level security on a model
description: Control access to model operations with user roles and groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/erp-canvas-set-operation-level-security-on-a-model.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, model, security, operation, model security, integration, data hub, zero, copy, connector, sap]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Set operation-level security on a model

Control access to model operations with user roles and groups.

This feature is available starting with the Zurich Patch 4 release.

You must have the sn\_erp\_integration.erp\_admin role to create and edit models.

New permission rules for model operations require you to have a specified role or be part of a specified user group to execute model operations. Each model operation must have at least one user role or one user group specified. You can add multiple user roles and groups as needed.

On a single model, different operations can have different permissions. For example, a financial data model can have some users with only read access to review data, but they can't update or create a financial record. For that same model, other users or groups can be given access to update and create financial records.

\[Omitted image "erp-operation-security1.png"\] Alt text: Manage model page with create, read, and update operations that have user or group roles assigned for security.

To help prevent disruptions, all existing model operations have been assigned the admin role and the erp\_user role by default.

You can edit these permissions on the existing operations at any time to suit your needs. To change the permissions, select the edit \(pencil\) icon \[Omitted image "pencil-outline-24.svg"\] Alt text: on the model operation card.

\[Omitted image "erp-operation-security2.png"\] Alt text: Manage model page with create, read, and update operations that have the admin and erp\_user role assigned.

To learn more about adding an operation, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

To clone a model, you must have permissions to access the model operations. For more information, see [Clone an ERP model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-clone-data-model.md).

**Parent Topic:**[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)

