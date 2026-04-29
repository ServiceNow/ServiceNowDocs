---
title: Asset life-cycle automation
description: Automate the update of your asset records throughout its life cycle and remove the effort of manually maintaining asset accuracy.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset life-cycle automation

Automate the update of your asset records throughout its life cycle and remove the effort of manually maintaining asset accuracy.

Assets must be updated and tracked from the time they’re purchased until they’re disposed. The automation process starts from the time that you request an asset through determining if the asset is in stock or if it must be purchased. If it's in stock, then the asset is transferred through the transfer order workflow. If the asset must be bought, then the purchase order workflow is triggered. The automated workflows take away the need to update manually each asset record or the associated configuration item \(CI\). After the workflow is complete, the asset records or CIs are automatically updated.

**Note:** The automated workflow isn't triggered for excluded assets. You must manually update your asset records or CIs for the excluded assets.

You can [create bulk stock orders](../task/create-inventory-stock-order.md) for hardware assets for your stockrooms. You can specify the model and the exact quantity you need. After the item is procured or transferred, the workflow is complete.

You can also [create disposal orders](../task/create-disposal-order.md) for hardware and consumable assets. This workflow guides you through five asset disposal tasks. These tasks involve the planning, scheduling, verification, departure, and the final confirmation of the disposed assets. Closing a task completes the task and creates the next task in the workflow.

For example, Verify is the first task in the asset disposal workflow. After you complete and close the Verify task, the Schedule pickup task is automatically created. This process continues until you close all the tasks required for disposing the asset. For information, see [Hardware disposal order stages](../reference/hardware-disposal-stages.md).

## Asset tasks

Asset tasks are provided for deploy, replace or swap, or retirement operations for your assets. These tasks automatically update the CI/asset record on the completion of these operations.

If an asset is being deployed, replaced, or retired via an incident, change request or a field service work order, the CI/asset record is automatically updated along with the related records for the CI/asset. For example, you have a change ticket to retire a server. After the change is implemented, the Change Management application triggers the retire asset event. The retire task is triggered and updates the following:

-   CI
-   related asset record
-   software allocations
-   maintenance contracts

The data accuracy is improved by reducing the need for manual intervention to update records.

When an asset is retired or swapped via an incident, the Stockroom field is populated based on the location of the asset. If there isn't any stockroom in the location of the asset, then the Stockroom field isn't populated. However, if the asset location is supported by multiple stockrooms as part of service locations, then the Stockroom field is automatically populated with details of the supporting stockroom based on the priority. For more details on service locations, see [Associate a stockroom with service locations](../task/associate-stockroom-with-service-locations.md).

This table lists the asset tasks available in each application.

<table id="table_z4y_rvb_zkb"><thead><tr><th>

Application

</th><th>

Asset Tasks

</th></tr></thead><tbody><tr><td>

Incident Management

</td><td>

-   Update/Repair
-   Swap
-   Retire

 **Note:** By default, asset action is required for closing incidents. If you don’t want to enforce any asset action for the closure of an incident, you can set the value of the system property **sn\_hamp.enable\_asset\_action\_validation\_incident** to **false**. For more details see, the [Not able to resolve incident or change request after installing HAMP - mandatory field Asset action \[KB1695540\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695540) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Change Management

</td><td>

-   Deploy
-   Retire

 **Note:** By default, asset action is required for closing change requests. If you don’t want to enforce any asset action for the closure of a change request, you can set the value of the system property **sn\_hamp.enable\_asset\_action\_validation\_change\_request** to **false**. For more details see, the [Not able to resolve incident or change request after installing HAMP - mandatory field Asset action \[KB1695540\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695540) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Field Service Management

</td><td>

Deploy

</td></tr></tbody>
</table>