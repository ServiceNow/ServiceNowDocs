---
title: Model management view
description: Use the Model management view in the Hardware Asset Workspace to create or edit models, view the asset model-related functions such as hardware and consumable models nearing the end of life, and take appropriate actions.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Model management view

Use the Model management view in the Hardware Asset Workspace to create or edit models, view the asset model-related functions such as hardware and consumable models nearing the end of life, and take appropriate actions.

All reports except **Days until next hardware content refresh** under the Model Management view get filtered based on the model category you choose.

![Model management view in the Hardware Asset Workspace.](../image/model-management-view.png "Model management view")

**Note:** Software model tab is hidden when Software Asset Management \(com.snc.software\_asset\_management\) or Software Asset Management Professional \(com.snc.pa.samp\) is active. You can view this Software model tab in Software Asset Workspace.

|Widget or chart|Description|
|---------------|-----------|
|Hardware models up for end of life this year|Count of hardware models whose start date of the end of life phase is the current year.|
|Consumable models up for end of life this year|Count of consumable models whose start date of the end of life phase is the current year.|
|Days until next hardware content refresh|Number of days after which the next hardware content refresh will be performed by Hardware Asset Management.|
|Missing data|Count of models that have missing model name, manufacturer, and model number.|
|Normalization metrics|Count of models that were normalized and those models that didn't get normalized.|
|Model lifecycle overview|Count of models that are present in each life cycle stage such as General Availability, End of Support, End of Life, and End of Sale.|
|Product model status|Current count of hardware, consumable, and software models based on the status of the models.|

