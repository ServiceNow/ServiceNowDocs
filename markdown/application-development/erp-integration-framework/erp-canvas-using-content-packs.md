---
title: Using Zero Copy Connector for ERP content packs
description: Learn how to use Zero Copy Connector for ERP content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-canvas-using-content-packs.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-04-17"
reading_time_minutes: 4
breadcrumb: [Zero Copy Connector for ERP content packs, Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Using Zero Copy Connector for ERP content packs

Learn how to use Zero Copy Connector for ERP content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Follow these steps to create an application in a new application scope and clone a content pack model within that same scope. Using this process packages the application with its own scope and a cloned model that you can edit. Working in a scope creates ownership of the application and cloned model. The owner can give access to others to edit the application and cloned model.

Before completing the procedure, it may be helpful to review the list of [Available Zero Copy Connector for ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-available-content-packs.md) and to [Explore an Zero Copy Connector for ERP content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-explore-a-content-pack.md) to review its contents.

## Procedure

1.  Create a new application.

    Use a builder application, such as Creator Studio or ServiceNow Studio, to create an application in a new scope. For detailed information and steps, see:

    -   [Create the foundation of an app in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/creator-studio/create-app-creator-studio.md)
    -   [Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md)
    -   [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/c_ApplicationScope.md)
2.  Confirm that an update set was created for the new application.

    1.  Navigate to **All** &gt; **** &gt; **System update sets** &gt; **Local update sets**.

    2.  Find the default update set created for the new application and select the name to open the record.

        \[Omitted image "erpc-check-update-set-content-pack-model-clone.png"\] Alt text: Update set list with default update set for the new application highlighted.

        If a default update set was not created for the new application, follow the instructions in [Create and select an update set as the current set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/system-update-sets/create-select-update-set.md).

    3.  In **Name**, type a unique name for the update set.

    4.  Select **Update**.

3.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

4.  Open the ERP models page by selecting the ERP models icon \(\[Omitted image "erpc-data-model-icon.png"\] Alt text: ERP model icon\) in the side panel.

5.  Review the list of ERP models.

    \[Omitted image "erpc-select-content-pack-model.png"\] Alt text: ERP canvas models page with content pack models highlighted in the list.

6.  Select a content pack model to clone.

    Models that are part of a content pack have **DP** at the beginning of their ERP model name.

7.  Confirm that you are still in the scope of your new application.

    Two messages in blue are displayed. The message in the record states the application in which the model resides and that the record cannot be edited. Remember that models in a content pack are always read only and that you must clone the model to take ownership and make changes.

    A second message states the current application scope, which should be the application you created earlier in this procedure.

    \[Omitted image "erpc-check-scope-content-pack-model-clone.png"\] Alt text: Model record with two messages highlighted.

8.  Select **Clone**.

    1.  Type a new model name.

    2.  Check that the correct target application is specified.

    3.  Select **Clone this model**.

        \[Omitted image "erpc-cloned-content-pack-model.png"\] Alt text: Clone this model modal with new name added.

        When the clone is complete, a success message in green is displayed.

        \[Omitted image "erpc-cloned-success-content-pack-model.png"\] Alt text: Model page with success message highlighted.

        For more information about cloning models, see [Clone an ERP model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-clone-data-model.md).

    4.  Select the **Models** tab.

    5.  Select the refresh list model icon \[Omitted image "sync-fill-24.svg"\].

    6.  Confirm that the new cloned model is listed.

        \[Omitted image "erpc-cloned-content-pack-model-in-list.png"\] Alt text: ERP Canvas models list with new cloned model highlighted.


## What to do next

Explore the new, cloned model and make changes as needed. For example, edit the mappings, inputs, or outputs. For more information, see [Building and managing ERP models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/work-with-erp-data-models.md).

**Parent Topic:**[Zero Copy Connector for ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-content-packs.md)

