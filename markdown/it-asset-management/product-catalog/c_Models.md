---
title: Models
description: Models are specific versions or various configurations of an asset. Models are used for managing and tracking assets through various ServiceNow platform asset applications, including Product Catalog, Asset Management, and Procurement.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Product Catalog, IT Asset Management]
---

# Models

Models are specific versions or various configurations of an asset. Models are used for managing and tracking assets through various ServiceNow platform asset applications, including Product Catalog, Asset Management, and Procurement.

Model definitions can be based on vendor-provided criteria, for example, the manufacturer name Apple MacBook Pro, or on a custom abstraction, for example, Graphic Designer Workstation. All model information is located in the Product Catalog application.

A model can be in one or more [model categories](c_ModelCategories.md). For example, a laptop can be a computer and a server. Model definitions specify whether the model creates an asset, a configuration item, or both. On a hardware model record, compatible hardware models can be added.

Unless otherwise noted, working with product models requires the model\_manager role. This role is contained by other roles, such as sam, category\_manager, and asset.

## Creating models

Models are created in the **Product Catalog** &gt; **Product Model** &gt; **All Models** module.

See [Model form fields](../reference/r_ModelFormFields.md) for a list of the fields that appear on all models, regardless of the type of model.

-   **[Model form fields](../reference/r_ModelFormFields.md)**  
There are fields on the Model form that apply to all types of models.
-   **[Create hardware models](../task/t_CreatingHardwareModels.md)**  
Use hardware models to track equipment assets such as servers and racks. You can create a new hardware model.
-   **[Create consumable models](../task/t_CreatingConsumableModels.md)**  
Consumables are items that are tracked as a group, not individually. An example of consumable items is computer keyboards.
-   **[Bundled models](c_CreatingBundledModels.md)**  
A bundled model is a single model comprised of individual models. For example, a laptop, printer, keyboard, and mouse can be combined into a single bundled model. If you assign any one asset from the bundled model to an individual, that person receives all the components in the bundle.
-   **[Software models](c_CreatingSoftwareModels.md)**  
Software models are created as part of the asset management process. You can create product models for software from the product catalog, but you cannot administer all aspects of the software models.
-   **[Create application models](../task/t_CreatingApplicationModels.md)**  
You can create application models that can be managed and tracked within a Scrum development process.
-   **[Work order models](c_CreatingWorkOrderModels.md)**  
When work management is activated, the ServiceNow platform adds the Work Order Models and Work Task Models modules to the product catalog.
-   **[Models created for VMware support and Amazon EC2](c_ModCreateForVMWSuppAmazEC2.md)**  
When you activate Orchestration for VMware and Amazon EC2, the system creates models automatically.
-   **[Add skills to a model](../task/t_AddingSkillsToAModel.md)**  
You can associate skills with any model. Creating associations between skills and models is helpful if you are using work management and want to assign tasks to agents based on their skills with specific models.
-   **[Publish models to the hardware or software catalog](../task/t_PublishingModToHrdwreOrSftCat.md)**  
You can publish models to the hardware or software catalog to make the models available in the service catalog.
-   **[Delete models](../task/t_DeletingModels.md)**  
If a model is no longer needed, you can delete it as long as no assets or configuration items use the model.

**Parent Topic:**[Product Catalog](c_ProductCatalog.md)

**Related topics**  


[Components installed with Product Catalog](../reference/r_InstalledWithProductCatalog.md)

[Vendor catalog items](c_ManageVendorCatalogItems.md)

[Product catalog items](c_ManagingProductCatalogItems.md)

[Model categories](c_ModelCategories.md)

[Domain separation and Product Catalog](domain-separation-product-catalog.md)

[Asset Management](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Procurement](../../procurement/concept/c_Procurement.md)

