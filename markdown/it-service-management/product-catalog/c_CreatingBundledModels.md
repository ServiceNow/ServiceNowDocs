---
title: Bundled models
description: A bundled model is a single model comprised of individual models. For example, a laptop, printer, keyboard, and mouse can be combined into a single bundled model. If you assign any one asset from the bundled model to an individual, that person receives all the components in the bundle.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Models, Product Catalog, Asset Management, IT Service Management]
---

# Bundled models

A bundled model is a single model comprised of individual models. For example, a laptop, printer, keyboard, and mouse can be combined into a single bundled model. If you assign any one asset from the bundled model to an individual, that person receives all the components in the bundle.

Bundled model is a template to define the kind of assets that would be a part of asset bundles. To maintain the integrity between asset bundles and bundled models, select the **Bundle assets** check box in the Product Model form layout. Once you select the check box, the status of the bundled model defaults to **Build**. While the status is in build, you can add make changes to the bundled model. Once you change the status to **In Production**, no changes can be made to the bundled model. Now that the bundled model is read-only, you can create asset bundles out of this bundled model. You can change the status of the bundled model back to **Build** only if there are no asset bundles associated with the bundled model.

**Note:** The **Bundle assets** check box functionality is available only with the Hardware Asset Management licensable application. Hardware Asset Management is available in the ServiceNow Store. To view more information on the asset bundle functionality, see [asset bundles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/asset-bundles-concept.md).

Bundled models can be abstract or concrete.

-   **Abstract**

    Permits use of one model in multiple bundles. The abstract bundle is created as a container. One asset in the bundle is specified as the main component. Model categories define which assets can be included in a bundle. Model categories also define what can be the main component of a bundle.

    Add a main component to make it easier to track the bundle components. For example, create an abstract bundle adding a computer as the main component and a mouse and keyboard as additional components. When the bundle is assigned to a user, the asset record for the computer shows the computer, mouse, and keyboard all assigned to the user. Abstract bundles are used more often than concrete bundles.

-   **Concrete**

    Is a fixed bundle where the main component is an asset. Specify the main component and the other components to create an exact bundle. Concrete bundles do not allow for a many-to-many relationship with models.


Keep the following tips in mind when creating and using bundled models.

-   Bundles can be nested inside bundles.
-   Any type of model can be used in a bundle.
-   When a parent link is defined, the fields related to assignment and state of the child assets are read-only. They are populated based on the parent's assignment and state fields.
-   If you make a change to the parent bundle, the children in the bundle are affected. For example, if you assign a bundle to an individual, all child asset records show that same individual as the person assigned.
-   You cannot pre-allocate bundles.
-   In a bundle, consumables are consumed and assets are set to the same state as the main component.
-   Only the bundle, not individual components, can be part of a transfer order.
-   You control what can go into a bundle through the model category. For example, the model category **Servers** could be set to never allow servers in bundles.
-   To create a collection of software, you must create a suite instead of a bundled model.
-   A software license cannot be the main component of a bundle.

To create an abstract model, set the model category to **Bundle** and add the components. To create a concrete model, create a model in the **Product Catalog** &gt; **Product Model** &gt; **Bundled Models** module and add components.

-   **[Add model components to a bundle](../task/t_AddingModelComponentsToABundle.md)**  
Add model components to a model as needed, for example, when you upgrade a bundle to include additional assets.
-   **[Remove model components from a bundle](../task/t_RemoveModelCompsFromABundle.md)**  
Remove a component from a bundled model, for example, when you want to replace it with a different component.
-   **[Publish bundled models to product catalog](../task/publish-product-catalog-bundledmodles.md)**  
You can publish bundled models to the product catalog to make the bundled models available in the service catalog.

**Parent Topic:**[Models](c_Models.md)

**Related topics**  


[Consume consumable assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_ConsumingConsumableAssets.md)

[Create pre-allocated assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/t_CreatingPreAllocatedAssets.md)

[Model categories](c_ModelCategories.md)

