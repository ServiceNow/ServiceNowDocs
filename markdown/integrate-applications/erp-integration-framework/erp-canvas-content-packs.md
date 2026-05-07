---
title: Zero Copy Connector for ERP content packs
description: Use Zero Copy Connector for ERP content packs as examples to help you implement and deploy applications with less manual work.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, content, pack, content pack, model, integration, data hub, zero, copy, connector, sap]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP content packs

Use Zero Copy Connector for ERP content packs as examples to help you implement and deploy applications with less manual work.

## Content packs

**Note:** Currently, content packs work only with SAP systems.

Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs are sets of predefined models and process extensions that are useful examples for developers with little or no SAP domain knowledge. For instance, you're integrating a ServiceNow application with SAP, but it's taking a long time because of the complexity of the SAP data. Content packs accelerate the work so that building uses cases involving SAP data becomes a faster process that more developers can accomplish.

After installing a content pack, the models it contains are listed on the Zero Copy Connector for ERP models page with a prefix of **DP**. The process extensions in thecontent pack are listed on the **Subflows** tab in Workflow Studio with a prefix of **ERP DP**.

Content pack models and process extensions are examples. Use them as accelerators that can be tailored to your requirements. The models and process extensions can't be edited, but can be viewed. If you see a model similar to the integration you're trying to create, clone the model, give it a unique name, and edit it as needed. If you find a process extension you want to use, copy, rename, and edit the models it contains as needed.

## Process extensions

Process extensions are subflows that can use one or more models. Process extensions enable you to use a model without needing to understand the model details. The process extensions are another abstraction layer on top of the models inside the content pack to make the models easier to use.

Process extensions in a content pack are read-only examples. To use a process extension, make a copy and edit it within Workflow Studio. For the steps to copy a process extension and add cloned models, see [Using Zero Copy Connector for ERP process extensions](../task/erp-canvas-using-process-extensions.md).

![Workflow Studio subflows list showing content pack process extensions.](../image/erpc-process-extensions-list-ws.png)

As an example for how to use process extensions, let's say there's a model for reading a sales order. You want to determine the sales orders that are blocked, but you don't know the SAP field that indicates if a order is blocked or not. Instead of researching to get the field name or asking the SAP experts in your organization, use the process extension named **ERP DP: Read Blocked Sales Orders** to do the work. A process extension can filter or add data when reading, using the model to find exactly what you are looking for based on the process extension description. So, in this example, instead of reading all sales orders, the process extension finds only the blocked sales orders.

## Contact pack prerequisites

You must have:

-   Zero Copy Connector for ERP installed
-   A linked SAP system from which to pull data
-   The sn\_erp\_integration.erp\_admin role

## Install from the ServiceNow Store

For detailed information about buying and installing Zero Copy Connector for ERP content packs, see the [ServiceNow Store Help](https://store.servicenow.com/$appstore.do#!/store/helpcenter) page.

-   **[Explore a Zero Copy Connector for ERP content pack](../task/erp-canvas-explore-a-content-pack.md)**  
Explore a Zero Copy Connector for ERP \(Enterprise Resource Planning\) content pack to see what it contains, including models and process extensions. Content pack models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP content packs](../task/erp-canvas-using-content-packs.md)**  
Learn how to use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs, from cloning a model to working within a scope. Content pack models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP process extensions](../task/erp-canvas-using-process-extensions.md)**  
Learn how to use the process extensions \(subflows\) in Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs. Content pack models and process extensions are examples.
-   **[Available Zero Copy Connector for ERP content packs](erp-canvas-available-content-packs.md)**  
These content packs are available for use in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to implement and deploy applications with less manual work.

**Parent Topic:**[Building and managing models to work with ERP data](work-with-erp-data-models.md)

