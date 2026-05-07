---
title: Using Zero Copy Connector for ERP content packs
description: Learn how to use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, content, pack, sample, example, model, application]
breadcrumb: [Content packs, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Using Zero Copy Connector for ERP content packs

Learn how to use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Follow these steps to create an application in a new application scope and clone a content pack model within that same scope. Using this process packages the application with its own scope and a cloned model that you can edit. Working in a scope creates ownership of the application and cloned model. The owner can give access to others to edit the application and cloned model as needed.

Before completing the procedure, it may be helpful to review the list of [Available Zero Copy Connector for ERP content packs](../concept/erp-canvas-available-content-packs.md) and to [Explore a Zero Copy Connector for ERP content pack](erp-canvas-explore-a-content-pack.md) to review its contents.

## Procedure

1.  Create an application.

    Use a builder application, such as Creator Studio or ServiceNow Studio, to create an application in a new scope. For detailed information and steps, see:

    -   [Create the foundation of an app in Creator Studio](https://www.servicenow.com/docs/access?context=create-app-creator-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)
    -   [Create an application in ServiceNow Studio](https://www.servicenow.com/docs/access?context=create-an-application-in-servicenow-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)
    -   [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US)
2.  Confirm that an update set was created for the new application.

    1.  Navigate to **All** &gt; **System update sets** &gt; **Local update sets**.

    2.  Find the default update set created for the new application and select the name to open the record.

        ![Update set list with default update set for the new application highlighted.](../image/erpc-check-update-set-content-pack-model-clone.png)

        If a default update set wasn't created for the new application, follow the instructions in [Create and select an update set as the current set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=australia&pubname=australia-application-development&ft:locale=en-US).

    3.  In **Name**, enter a unique name for the update set.

    4.  Select **Update**.

3.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

4.  Open the ERP models page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

5.  Review the list of ERP models.

    ![List of models with name column highlighted.](../image/erpc-select-content-pack-model.png)

6.  Select a content pack model to clone.

    Models that are part of a content pack have **DP** at the beginning of their ERP model name.

7.  Confirm that you're still in the scope of your new application.

    Two messages in blue are displayed. The message in the record states the application in which the model resides and that the record can't be edited. Remember that models in a content pack are read only and that you must clone the model to take ownership and make changes.

    A second message states the current application scope, which should be the application you created earlier in this procedure.

    ![Model page with two scope messages highlighted.](../image/erpc-check-scope-content-pack-model-clone.png)

8.  Select **Clone**.

    1.  Enter a new model name.

    2.  Check that the correct target application is specified.

    3.  Select **Clone this model**.

        ![Clone this model modal with new name added.](../image/erpc-cloned-content-pack-model.png)

        When the clone is complete, a success message is displayed.

        For more information about cloning models, see [Clone an ERP model in Zero Copy Connector for ERP](erp-canvas-clone-data-model.md).

    4.  Select the **Models** tab.

    5.  Select the refresh list model icon ![](../../../reuse/icons/product-icons/sync-fill-24.svg).

    6.  Confirm that the new cloned model is listed.


## What to do next

Explore the new, cloned model and make changes as needed. For example, edit the mappings, inputs, or outputs. For more information, see [Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md).

**Parent Topic:**[Zero Copy Connector for ERP content packs](../concept/erp-canvas-content-packs.md)

