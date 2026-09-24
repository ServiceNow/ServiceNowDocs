---
title: Configure Hardware Model Normalization
description: Hardware Model Normalization standardizes manufacturer, model, and model number data across asset records using the Hardware Asset Management Content Service. Normalized data improves the accuracy of asset reporting, lifecycle planning, and cost analysis. Configure hardware normalization before asset managers begin creating or managing hardware models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Integrations and advanced configuration, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Configure Hardware Model Normalization

Hardware Model Normalization standardizes manufacturer, model, and model number data across asset records using the Hardware Asset Management Content Service. Normalized data improves the accuracy of asset reporting, lifecycle planning, and cost analysis. Configure hardware normalization before asset managers begin creating or managing hardware models.

When you opt in to Hardware Model Normalization, HAM compares asset model data against the Content Library and applies standardized values for manufacturer name, model name, model number, and end-of-life and end-of-support dates. You can also create custom models for hardware asset that is not available in the Content Library.

|Configuration task|Purpose|Required|
|------------------|-------|--------|
|[Create a hardware or consumable model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md)|Creates a model record for a hardware or consumable asset|Yes|
|[Copy a hardware model from the Content lookup portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/copy-hardware-model.md)|Copies a hardware model from the Content lookup portal to the Product Model \[cmdb\_model\] table|If needed|
|[Normalize hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md)|Runs normalization to apply standardized manufacturer, model, and lifecycle data from the Content Library|Yes|
|[Add a custom product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/add-custom-hardware-model.md)|Creates a custom product if it is not available the Content Library|If needed|
|[Add a custom hardware model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/add-custom-model.md)|Creates a custom hardware model if it is not available in the Content Library|If needed|
|[Revert normalization of hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/revert-norm-ham.md)|Removes applied normalization and restores original model data|If needed|

-   **[Create a hardware or consumable model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md)**  
To begin tracking your hardware and consumable assets, create a hardware or consumable model. Then, add lifecycle information to keep track of the lifecycle phase of your model.
-   **[Copy a hardware model from the Content lookup portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/copy-hardware-model.md)**  
Copy a hardware model record from the Content lookup portal to add a new model entry to the Product Model \[cmdb\_model\] table.
-   **[Normalize hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md)**  
After you have created your hardware and consumable models, normalize the information of the model.
-   **[Add a custom product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/add-custom-hardware-model.md)**  
If you have a product that is not represented in the Asset Management Content Service yet, you can create a custom product.
-   **[Add a custom hardware model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/add-custom-model.md)**  
If you have a hardware model that isn't represented in the Asset Management Content Service yet, you can create a custom model.
-   **[Revert normalization of hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/revert-norm-ham.md)**  
Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.

**Parent Topic:**[Integrations and advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/integrations-advncd-configs.md)

**Related topics**  


[Hardware Model Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/hardware-normalization.md)

