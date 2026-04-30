---
title: Model categories
description: Model categories associate CI classes with asset classes. Model categories are part of the Product Catalog application.
locale: en-US
release: xanadu
product: Product Catalog
classification: product-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Product Catalog, Asset Management, IT Service Management]
---

# Model categories

Model categories associate CI classes with asset classes. Model categories are part of the Product Catalog application.

The model category configuration determines if the ServiceNow platform creates an asset from a CI, and, if so, what class of asset. Asset classes in the base system are **Hardware**, **Software License**, and **Consumable**. You can associate a model category to many models and a model to many model categories. For example, a specific model of a computer can be a **Computer** and a **Server**.

![Models diagram](../image/ModelsDiagram.png "Models diagram")

Any item that is provided as a service or sold to your customer is tracked as an Install Base Item \(IBI\). The Model category table associates Asset class, CI class, and Install Base Item \(IBI\) class.

**Note:** The Install Base Item class field is available on the Model category form only when the Customer Service Install Base Management \[com.snc.install\_base\] plugin is installed. Currently, only the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] is supported when the Healthcare and Life Sciences Service Management Core application is installed. For more details, see [Medical device install base item table](https://www.servicenow.com/docs/access?context=hcls-clinical-device-ib-item&version=xanadu&pubname=xanadu-healthcare-life-sciences&ft:locale=en-US). When an IBI class is created, it associates with an asset when the asset exists, otherwise an asset is created.

The fields in the Asset class and the IBI class are synchronized as follows:

1.  When an IBI class is updated, the Account, Consumer, Location, and Install date field changes are synchronized with the corresponding fields of the Asset class.
2.  When an Asset class is updated, the Location and Install date field changes are synchronized with the corresponding fields of the IBI class.

-   **[View model categories](../task/t_ViewingModelCategories.md)**  
Default model categories are included with product catalog. You can view a list of default categories and the categories that you created.
-   **[Create model categories](../task/t_CreatingModelCategories.md)**  
You can add custom model categories for your instance.
-   **[Create assets manually](../task/t_CreatingAssetsManually.md)**  
The ServiceNow AI Platform does not create an asset automatically under certain conditions. You can create an asset manually as needed.
-   **[Edit model categories](../task/t_EditingModelCategories.md)**  
All default model categories can be edited, except for the Contract model category. You can edit any custom model categories that you created at any time.
-   **[Delete model categories](../task/t_DeletingModelCategories.md)**  
If a model category is no longer needed, you can delete it.

**Parent Topic:**[Product Catalog](c_ProductCatalog.md)

**Related topics**  


[Components installed with Product Catalog](../reference/r_InstalledWithProductCatalog.md)

[Models](c_Models.md)

[Vendor catalog items](c_ManageVendorCatalogItems.md)

[Product catalog items](c_ManagingProductCatalogItems.md)

[Domain separation and Product Catalog](domain-separation-product-catalog.md)

[CMDB classifications and class dependency](https://www.servicenow.com/docs/access?context=c_CMDBClassifications&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Create an asset class](../../asset-management/task/t_CreateAnAssetClass.md)

