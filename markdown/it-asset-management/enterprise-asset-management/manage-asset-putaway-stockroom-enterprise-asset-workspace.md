---
title: Manage asset put away using the Enterprise Asset Workspace
description: Enable the Asset put away task explicitly for your stockroom to put away the assets from the receiving bay in the designated aisle-space. View the open Asset put away task and close it after specifying the aisle-space value to move the asset in the stockroom.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [enterprise asset put away, put away assets]
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Manage asset put away using the Enterprise Asset Workspace

Enable the Asset put away task explicitly for your stockroom to put away the assets from the receiving bay in the designated aisle-space. View the open Asset put away task and close it after specifying the aisle-space value to move the asset in the stockroom.

The Asset put away task enables you to track asset movement from the receiving bay of the inventory to the designated space within the stockroom. The Asset put away task confirms that when an asset is received in the inventory, you have filled the aisle-space information for it. An Asset put away task is automatically created in the Enterprise Asset Management when the following required business rules are met:

-   When an enterprise asset is created in the Enterprise Asset Management and the **Aisle-space** field value isn’t available, an Asset put away task is created. Open the Asset put away task and updated the **Drop off location** field value, to move the asset to designated aisle-space in the stockroom.

    **Note:** You can create an Asset put away task manually for the in stock assets in the inventory. For more information about manually creating an Asset put away task in the Enterprise Asset Management, see [Create an Asset put away task in the Enterprise Asset Workspace](../task/create-asset-put-away-task-eam.md).

-   When the **Stockroom** field is updated for an enterprise asset in the [Asset Details](../reference/asset-fields-eam.md) form, an Asset put away task is created. Open the Asset put away task and update the **Drop off location** field value, to move the asset to the designated aisle-space in the stockroom.

**Note:** You can create the Asset put away task for a stockroom only if the stockroom is enabled to perform warehouse tasks. For more information about enabling the feature, see [Enable the asset put away task for your stockroom in the Enterprise Asset Workspace](../task/enable-putaway-task-for-stockroom-eam.md).

In the Enterprise Asset Workspace, the inventory users can perform the following actions:

-   Create an Asset put away task manually for the in stock assets. For more information, see [Create an Asset put away task in the Enterprise Asset Workspace](../task/create-asset-put-away-task-eam.md).
-   View the open put away tasks related to the inventory and stockroom. For more information, see [View open put away tasks for your stockroom in the Enterprise Asset Workspace](../task/view-open-putaway-tasks-eam.md).
-   Update the **Drop off location** field for the open task in the Put away form and close it. For more information, see [Close an Asset put away task in the Enterprise Asset Workspace](../task/close-put-away-task-eam.md).

Using the ServiceNow Agent application, you can scan the in stock assets in the inventory and put away them in the scanned drop-off location. After the asset is placed in the drop-off location within the stockroom, you can close the Asset put away task. For more information on the mobile experience for Asset put away task, see [Manage enterprise asset put away using the ServiceNow Agent application](manage-asset-put-away-eam-mobile-agent.md).

-   **[Enable the asset put away task for your stockroom in the Enterprise Asset Workspace](../task/enable-putaway-task-for-stockroom-eam.md)**  
Enable the Asset put away feature for your stockroom so that the Asset put away task is automatically created to track asset movement.
-   **[View open put away tasks for your stockroom in the Enterprise Asset Workspace](../task/view-open-putaway-tasks-eam.md)**  
View the open put away tasks for your stockroom in the Enterprise Asset Workspace to get the details of the tasks that need action.
-   **[Create an Asset put away task in the Enterprise Asset Workspace](../task/create-asset-put-away-task-eam.md)**  
Create an Asset put away task manually for the In stock assets in the Enterprise Asset Workspace to track the movement of assets within the stockroom.
-   **[Close an Asset put away task in the Enterprise Asset Workspace](../task/close-put-away-task-eam.md)**  
Add the asset drop-off location for an open Asset put away task and close it in the Enterprise Asset Workspace.

**Parent Topic:**[Create and manage enterprise asset inventory](managing-enterprise-asset-inventory.md)

