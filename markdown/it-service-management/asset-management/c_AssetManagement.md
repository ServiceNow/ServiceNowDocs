---
title: Asset Management
description: The ServiceNow Asset Management application integrates the physical, technological, contractual, and financial aspects of information technology assets.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [IT Service Management]
---

# Asset Management

The ServiceNow® Asset Management application integrates the physical, technological, contractual, and financial aspects of information technology assets.

**Note:** Beginning with the ServiceNow AI Platform® Washington DC release, we will provide limited support for the Asset Management Core UI interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform release, we encourage you to move to the new workspace experience. For more information, see [KB1584548](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584548), [Exploring Asset Management Workspace](https://www.servicenow.com/docs/access?context=exploring-asset-management&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) and [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Asset management business practices have a common set of goals.

-   Control inventory that is purchased and used.
-   Reduce the cost of purchasing and managing assets.
-   Select the proper tools for managing assets.
-   Manage the asset life cycle from planning to disposal.
-   Achieve compliance with relevant standards and regulations.
-   Improve IT service to end users.
-   Create standards and processes for managing assets.

Most successful ITAM programs involve various people and departments, including IT, finance, services, and end users.

Asset Management and the Configuration Management Database \(CMDB\) are related, but have different goals. Asset Management focuses on the financial tracking of company property. Configuration management focuses on building and maintaining elements that create an available network of services.

-   **[Mobile app for Hardware Asset Management](../../../administer/mobile-my-asset/concept/mobile-my-asset.md)**  
Use the ServiceNow Mobile and ServiceNow Agent apps to manage your assets.
-   **[Asset and CI management](c_ManagingAssets.md#)**  
Asset and configuration item \(CI\) management refers to creating assets, setting appropriate states and substates, synchronizing assets and CIs, managing consumables, and retiring assets.
-   **[Manage various assets through asset classes](c_AssetClasses.md)**  
The default asset classes are Hardware, Software License, Consumable, Bundle, Software Entitlement, and Facility. These general classes can be used to manage various assets.
-   **[Create fixed assets](c_CreatingFixedAssets.md#)**  
Fixed assets are containers that can hold multiple assets. Fixed assets are commonly tracked at the corporate level by a finance or accounting department, but may contain IT assets such as hardware and software.
-   **[Consumables life cycle](c_FollowLifeCycleConsumbl.md#)**  
Consumables are assets that are not tracked individually, but as a group of the same model.
-   **[Create pre-allocated assets](../task/t_CreatingPreAllocatedAssets.md#)**  
Create a pre-allocated asset that physically exists, but isn’t yet a financial liability.
-   **[Stockrooms](c_Stockrooms.md#)**  
Stockrooms are places to which assets are assigned.
-   **[Transfer orders for Asset Management](transfer-orders-asset.md#)**  
Transfer orders move assets between company stockrooms.
-   **[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md#)**  
Create a transfer order in order to transfer assets from one location to the other.
-   **[Perform bulk updates for transfer order lines](../task/create-bulk-transfer.md)**  
Update tasks for multiple transfer order lines at one go to streamline the transfer order process.
-   **[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md#)**  
As transfer order line actions are triggered, the stock information and states of any affected assets are updated. Consumables and non-consumables are tracked differently.
-   **[Example Asset Management process](../task/t_AssetManagementProcess.md)**  
The best method for managing assets depends on business needs and how your business is organized.
-   **[CSDM framework for HAM](../../hardware-asset-management/concept/csdm-framework-for-ham.md)**  
Common Service Data Model \(CSDM\) is a standard and consistent set of terms and definitions to adopt across all ServiceNow products on the ServiceNow AI Platform.
-   **[ITSM Software Asset Management](itsm-sam.md)**  
The software asset management features of the ITSM suite can be activated using one of the plugins in the feature table.
-   **[Organization Management](../reference/r_OrganizationManagement.md#)**  
The Organization Management application provides an easy way to perform such asset management tasks as updating users and adding vendors.
-   **[Installed with Model Management](c_InstalledWithModelManagement.md#)**  
Several types of components are installed with Model Management.
-   **[Installed with Asset Management](../reference/r_InstalledWithAssetManagement.md)**  
Several tables, user roles, UI policies, script includes, client scripts, and business rules are installed with Asset Management.
-   **[Domain separation and Asset Management](domain-separation-asset-management.md)**  
Domain separation is supported in Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Quick start test for Asset Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-am.md)**  
Validate that Asset Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Contract Management](../../contract-management/concept/c_ContractManagement.md)**  
Manage and track contracts with the ServiceNow® Contract Management application.
-   **[Procurement](../../procurement/concept/c_Procurement.md)**  
Procurement managers can use the ServiceNow® Procurement application to create purchase orders and to obtain items for fulfilling service catalog requests.
-   **[Product Catalog](../../product-catalog/concept/c_ProductCatalog.md)**  
The product catalog is a set of information about individual models. Models are specific versions or various configurations of an asset. Asset managers use the product catalog as a centralized repository for model information.

**Parent Topic:**[IT Service Management](../../it-service-management/reference/r_ITServiceManagement.md)

**Related topics**  


[Domain separation and Asset Management](domain-separation-asset-management.md)

