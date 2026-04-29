---
title: Create a multi-component asset
description: Track and manage your assets by creating a multi-component asset from a multi-component model.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a multi-component asset

Track and manage your assets by creating a multi-component asset from a multi-component model.

## Before you begin

For details on multi-component models, see [Multi-component models and assets in Enterprise Asset Management](../concept/complex-models.md).

Role required:

-   sn\_eam.enterprise\_admin
-   sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Create a model by navigating to **Enterprise Asset Workspace** &gt; **Enterprise model management**

    For details on creating a model, see [Create enterprise models](create-model-eam.md).

2.  After you created a model, add model components to the model.

    For details on creating model components, see [Create enterprise model components](create-model-components-eam.md).

3.  Create assets from the multi-component model.

    You can create a pre-assembled or an user-assembled asset.

    For details on creating an asset, see [Create enterprise assets](create-asset-eam.md). Once you create assets, child assets are automatically created.

    1.  If you create a user-assembled asset, open the asset record.

    2.  Select either of the two to assemble assets:

        -   **Assemble**: gives you a choice to choose the assets present in the parent asset's stockroom. Once you select the assets, select **Assemble**. For details on assembling assets, see
        -   **Auto assemble**: triggers a process that automatically selects assets from a stockroom and associates those assets with the parent asset. If the required quantity of assets is not available, an error appears.
    3.  If you want to release all child assets, select **Release all assets**.

        This process releases all child assets from the parent asset and assigns them back to the parent stockroom.

        The released assets move to **In Stock** status. **Release all assets** is only visible on screen when assets are associated with a parent asset.

4.  To swap child assets, in the Details tab select **SWAP**.

    The multi-component asset needs to be in the **In maintenance** state to swap assets. You can swap multiple child assets at one go with other assets from the same model in any stockroom. The model must be in the **In stock** state and **Available** sub state.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

