---
title: Zero Copy Connector for ERP content packs
description: Use Zero Copy Connector for ERP content packs as examples to help you implement and deploy applications faster with less manual work.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-02-27"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, content, pack, content pack, model]
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP content packs

Use Zero Copy Connector for ERP content packs as examples to help you implement and deploy applications faster with less manual work.

**Note:** Currently, content packs work only with SAP systems.

Zero Copy Connector for ERP content packs are sets of pre-defined models and process extensions that are useful examples for developers with little or no SAP domain knowledge. For instance, you are integrating a ServiceNow application with SAP, but it's taking a long time because of the complexity of the SAP data. Content packs accelerate the work so that building uses cases involving SAP data becomes a faster process that more developers can accomplish.

After installing a content pack, the models it contains are listed on the Zero Copy Connector for ERP models page with a prefix of **DP**. The process extensions in the content pack are listed on the **Subflows** tab in Workflow Studio with a prefix of **ERP DP**.

Content pack models and process extensions are examples. Use them as accelerators that can be tailored to your requirements. The models and process extensions can't be edited, but can be viewed. If you see a model that looks similar to the integration you're trying to create, clone the model, give it a unique name, and edit it as needed. If you find a process extension you want to use, copy, rename, and edit the models it contains as needed.

## Prerequisites

You must have:

-   ERP Canvas installed
-   A linked SAP system from which to pull data
-   The sn\_erp\_integration.erp\_admin role

## Install from the ServiceNow Store

For detailed information about buying and installing an application, see the [ServiceNow Store Help](https://store.servicenow.com/$appstore.do#!/store/helpcenter) page.

-   **[Zero Copy Connector for ERP content pack process extensions](erp-canvas-content-pack-process-extensions.md)**  
Use the process extensions in Zero Copy Connector for ERP content packs as examples that can be copied to add subflows with business logic to one or more models.
-   **[Explore an Zero Copy Connector for ERP content pack](../task/erp-canvas-explore-a-content-pack.md)**  
Explore an Zero Copy Connector for ERP content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP content packs](../task/erp-canvas-using-content-packs.md)**  
Learn how to use Zero Copy Connector for ERP content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP process extensions](../task/erp-canvas-using-process-extensions.md)**  
Learn how to use the process extensions \(subflows\) in Zero Copy Connector for ERP content packs. Content pack models and process extensions are examples.
-   **[Available Zero Copy Connector for ERP content packs](erp-canvas-available-content-packs.md)**  
The following content packs are available for use in Zero Copy Connector for ERP to implement and deploy applications faster with less manual work.
-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](erp-canvas-enterprise-data-foundation-content-pack.md)**  
Find details about the models and process extensions in the Zero Copy Connector for ERP Enterprise Data Foundation content pack.
-   **[Zero Copy Connector for ERP Quote to Cash content pack](erp-canvas-sales-order-content-pack.md)**  
Find details about the models and process extensions in the Zero Copy Connector for ERP Sales Order content pack.

**Parent Topic:**[Building and managing ERP models to work with ERP data](work-with-erp-data-models.md)

