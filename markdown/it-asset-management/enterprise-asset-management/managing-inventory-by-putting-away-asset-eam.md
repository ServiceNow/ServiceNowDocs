---
title: Managing inventory by putting away enterprise assets in the stockroom drop-off location
description: Use the Asset put away feature to track asset movement efficiently in the inventory.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-06-18"
reading_time_minutes: 3
keywords: [asset put away task, put away asset]
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Managing inventory by putting away enterprise assets in the stockroom drop-off location

Use the Asset put away feature to track asset movement efficiently in the inventory.

**Important:** The Asset put away feature is available with Enterprise Asset Management version 9.0 onwards.

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

