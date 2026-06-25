---
title: Models
description: Models are specific versions or various configurations of an asset. Models are used for managing and tracking assets through various ServiceNow platform asset applications, including Product Catalog, Asset Management, and Procurement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/product-catalog/c\_Models.html
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

A model can be in one or more [model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_ModelCategories.md). For example, a laptop can be a computer and a server. Model definitions specify whether the model creates an asset, a configuration item, or both. On a hardware model record, compatible hardware models can be added.

Unless otherwise noted, working with product models requires the model\_manager role. This role is contained by other roles, such as sam, category\_manager, and asset.

## Creating models

Models are created in the **Product Catalog** &gt; **Product Model** &gt; **All Models** module.

See [Model form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/r_ModelFormFields.md) for a list of the fields that appear on all models, regardless of the type of model.

-   **[Model form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/r_ModelFormFields.md)**  
There are fields on the Model form that apply to all types of models.
-   **[Create hardware models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_CreatingHardwareModels.md)**  
Use hardware models to track equipment assets such as servers and racks. You can create a new hardware model.
-   **[Create consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_CreatingConsumableModels.md)**  
Consumables are items that are tracked as a group, not individually. An example of consumable items is computer keyboards.
-   **[Bundled models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_CreatingBundledModels.md)**  
A bundled model is a single model comprised of individual models. For example, a laptop, printer, keyboard, and mouse can be combined into a single bundled model. If you assign any one asset from the bundled model to an individual, that person receives all the components in the bundle.
-   **[Software models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_CreatingSoftwareModels.md)**  
Software models are created as part of the asset management process. You can create product models for software from the product catalog, but you cannot administer all aspects of the software models.
-   **[Create application models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_CreatingApplicationModels.md)**  
You can create application models that can be managed and tracked within a Scrum development process.
-   **[Work order models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_CreatingWorkOrderModels.md)**  
When work management is activated, the ServiceNow platform adds the Work Order Models and Work Task Models modules to the product catalog.
-   **[Models created for VMware support and Amazon EC2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_ModCreateForVMWSuppAmazEC2.md)**  
When you activate Orchestration for VMware and Amazon EC2, the system creates models automatically.
-   **[Add skills to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_AddingSkillsToAModel.md)**  
You can associate skills with any model. Creating associations between skills and models is helpful if you are using work management and want to assign tasks to agents based on their skills with specific models.
-   **[Publish models to the hardware or software catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_PublishingModToHrdwreOrSftCat.md)**  
You can publish models to the hardware or software catalog to make the models available in the service catalog.
-   **[Delete models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/t_DeletingModels.md)**  
If a model is no longer needed, you can delete it as long as no assets or configuration items use the model.

**Parent Topic:**[Product Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/product-catalog/c_ProductCatalog.md)

**Related topics**  


[Components installed with Product Catalog]()

[Vendor catalog items]()

[Product catalog items]()

[Model categories]()

[Domain separation and Product Catalog]()

[Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_AssetManagement.md)

[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/c_Procurement.md)

