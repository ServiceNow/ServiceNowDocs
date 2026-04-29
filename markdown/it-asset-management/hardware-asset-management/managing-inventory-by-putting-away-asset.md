---
title: Managing inventory by putting away assets in the stockroom drop-off location
description: Use the Asset put away feature to track asset movement efficiently in the inventory.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [asset put away task, put away asset]
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Managing inventory by putting away assets in the stockroom drop-off location

Use the Asset put away feature to track asset movement efficiently in the inventory.

The Asset put away task enables you to track asset movement from the receiving bay of the inventory to the designated space within the stockroom. The Asset put away task confirms that when an asset is received in the inventory, you have filled the aisle-space information for it. An Asset put away task is automatically created in the Hardware Asset Workspace when the following required business rules are met:

-   When a hardware asset is created in the Hardware Asset Workspace and the **Aisle-space** field value isn’t available, an Asset put away task is created. Open the Asset put away task and updated the **Drop off location** field value, to move the asset to designated aisle-space in the stockroom.

    **Note:** You can create an Asset put away task manually for the in stock assets in the inventory. For more information about manually creating an Asset put away task in the Hardware Asset Workspace, see [Create an Asset put away task](../task/create-asset-put-away-task.md).

-   When the **Stockroom** field is updated for a hardware asset in the [Hardware Asset Details](../../asset-management/reference/asset-record-fields.md) form, an Asset put away task is created. Open the Asset put away task and update the **Drop off location** field value, to move the asset to the designated aisle-space in the stockroom.

**Note:** You can create the Asset put away task for a stockroom only if the stockroom is enabled to perform warehouse tasks. For more information about enabling the feature, see [Enable the asset put away task for your stockroom](../task/enable-putaway-task-for-stockroom-ham.md).

In the Hardware Asset Workspace, the inventory users can perform the following actions:

-   Create an Asset put away task manually for the in stock assets. For more information, see [Create an Asset put away task](../task/create-asset-put-away-task.md).
-   View the open put away tasks related to the inventory and stockroom. For more information, see [View open put away tasks for your stockroom](../task/view-open-putaway-tasks-ham.md).
-   Update the **Drop off location** field for the open task in the Put away form and close it. For more information, see [Close an Asset put away task](../task/close-put-away-task-ham.md).

Using the ServiceNow Agent application, you can scan the in stock assets in the inventory and put away them in the scanned drop-off location. After the asset is placed in the drop-off location within the stockroom, you can close the Asset put away task. For more information on the mobile experience for Asset put away task, see [Manage asset put away using the ServiceNow Agent application](manage-hardware-asset-put-away-ham-mobile-agent.md).

