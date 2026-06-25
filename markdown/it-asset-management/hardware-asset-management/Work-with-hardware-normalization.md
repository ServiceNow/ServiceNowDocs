---
title: Work with hardware normalization
description: Asset Management Hardware Model Normalization enables users to normalize the details, such as manufacturer, product, model, and device type, of your hardware and consumable models. Data from the models is compared against the data in the Hardware Model Normalization Content Service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Work with hardware normalization

Asset Management Hardware Model Normalization enables users to normalize the details, such as manufacturer, product, model, and device type, of your hardware and consumable models. Data from the models is compared against the data in the Hardware Model Normalization Content Service.

The Normalization Data Services Client \(com.glide.data\_services\_canonicalization.client\) plugin is also activated when you activate the Hardware Model Normalization plugin.

**Note:** This documentation is for Hardware Model Normalization. For additional information on Asset Management, see the [Asset Management documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_AssetManagement.md).

## Scheduled jobs

To standardize your hardware and consumable models, the asset data must be normalized. You can manually update the model records with the normalization content, or you can compare your data against the Hardware Asset Management Content Service.

The **HAM- Hardware Normalization** scheduled job runs daily. This job does not add, remove, or merge models, nor does it modify original fields like Model Name, Manufacturer, or Model Number. It only updates the normalization-related fields for existing models, such as Normalized Product, Normalized Manufacturer, Normalized Model, and so on.

Content from the Hardware Model Normalization Content Service is pulled into the ServiceNow AI Platform. Use the Asset Job Log \(asset\_job\_log\) table to review the status of the scheduled job.

The normalization status of models can be reverted by clicking **Revert Normalization** on the model. Any normalization that occurred on the model gets reverted and the rule gets deactivated. When the scheduled job runs, the models are processed with the active rules and the status is updated.

The scheduled job generates hardware and consumable model reports. These reports identify the overall status of your models and provide a breakdown of the normalization status.

The following reports are included.

-   Hardware Product Overall Normalization Status
-   Consumable Product Overall Normalization Status
-   Hardware Model Normalization Status
-   Consumable Model Normalization Status

-   **[Opt-in to the Hardware Asset Management Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/opt-in-hardware-normalization.md)**  
Opt in to the Hardware Asset Management Content Service to improve the normalization process by sharing hardware and consumable model data from your organization with ServiceNow.
-   **[Import and export content data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/import-export-ham.md)**  
Import content data from or export content data to the Hardware Asset Management content library service to support hardware normalization of asset models. On-premise users can import or export data via a zip file using the Manage Hardware Library module.
-   **[Create a hardware or consumable model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md)**  
To begin tracking your hardware and consumable assets, create a hardware or consumable model. Then, add lifecycle information to keep track of the lifecycle phase of your model.
-   **[Copy a hardware model from the Content lookup portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/copy-hardware-model.md)**  
Copy a hardware model record from the Content lookup portal to add a new model entry to the Product Model \[cmdb\_model\] table.
-   **[Normalize hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md)**  
After you have created your hardware and consumable models, normalize the information of the model.
-   **[Revert normalization of hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/revert-norm-ham.md)**  
Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.
-   **[Add a custom product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/add-custom-hardware-model.md)**  
If you have a product that is not represented in the Asset Management Content Service yet, you can create a custom product.
-   **[Add a custom hardware model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/add-custom-model.md)**  
If you have a hardware model that isn't represented in the Asset Management Content Service yet, you can create a custom model.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

[Hardware Model Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/hardware-normalization.md)

