---
title: Zero Copy Connector for ERP data products
description: Use Zero Copy Connector for ERP data products \(formerly named ERP content packs\) as examples to help you implement and deploy applications with less manual work.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, content, pack, content pack, model]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP data products

Use Zero Copy Connector for ERP data products \(formerly named ERP content packs\) as examples to help you implement and deploy applications with less manual work.

**Note:** Currently, data products work only with SAP systems.

Zero Copy Connector for ERP data products are sets of predefined models and process extensions that are useful examples for developers with little or no SAP domain knowledge. For instance, you're integrating a ServiceNow application with SAP, but it's taking a long time because of the complexity of the SAP data. Data products accelerate the work so that building uses cases involving SAP data becomes a faster process that more developers can accomplish.

After installing a data product, the models it contains are listed on the Zero Copy Connector for ERP models page with a prefix of **DP**. The process extensions in the data product are listed on the **Subflows** tab in Workflow Studio with a prefix of **ERP DP**.

Data product models and process extensions are examples. Use them as accelerators that can be tailored to your requirements. The models and process extensions can't be edited, but can be viewed. If you see a model similar to the integration you're trying to create, clone the model, give it a unique name, and edit it as needed. If you find a process extension you want to use, copy, rename, and edit the models it contains as needed.

## Prerequisites

You must have:

-   Zero Copy Connector for ERP installed
-   A linked SAP system from which to pull data
-   The sn\_erp\_integration.erp\_admin role

## Install from the ServiceNow Store

For detailed information about buying and installing Zero Copy Connector for ERP data products, see the [ServiceNow Store Help](https://store.servicenow.com/$appstore.do#!/store/helpcenter) page.

-   **[Zero Copy Connector for ERP data product process extensions](erp-canvas-content-pack-process-extensions.md)**  
Use the process extensions in Zero Copy Connector for ERP data products as examples that can be copied to add subflows with business logic to one or more models.
-   **[Explore a Zero Copy Connector for ERP data product](../task/erp-canvas-explore-a-content-pack.md)**  
Explore a Zero Copy Connector for ERP data product to see what it contains, including models and process extensions. Data product models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP data products](../task/erp-canvas-using-content-packs.md)**  
Learn how to use Zero Copy Connector for ERP data products, from cloning a model to working within a scope. Data product models and process extensions are examples.
-   **[Using Zero Copy Connector for ERP process extensions](../task/erp-canvas-using-process-extensions.md)**  
Learn how to use the process extensions \(subflows\) in Zero Copy Connector for ERP data products. Data product models and process extensions are examples.
-   **[Available Zero Copy Connector for ERP data products](erp-canvas-available-content-packs.md)**  
The following data products are available for use in Zero Copy Connector for ERP to implement and deploy applications with less manual work.
-   **[Zero Copy Connector for ERP Enterprise Data Foundation data product](erp-canvas-enterprise-data-foundation-content-pack.md)**  
Find details about the models and process extensions in the Zero Copy Connector for ERP Enterprise Data Foundation data product.
-   **[Zero Copy Connector for ERP Quote to Cash data product](erp-canvas-sales-order-content-pack.md)**  
Find details about the models and process extensions in the Zero Copy Connector for ERP Sales Order data product.
-   **[Zero Copy Connector for ERP Source to Settle data product](erp-source-to-settle-data-product.md)**  
Find details about the models and process extensions in the Zero Copy Connector for ERP Source to Settle data product.

**Parent Topic:**[Building and managing models to work with ERP data](work-with-erp-data-models.md)

