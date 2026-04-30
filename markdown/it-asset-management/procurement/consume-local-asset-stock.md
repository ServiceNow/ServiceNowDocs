---
title: Source requests from local stockrooms
description: Get visibility into local stockrooms at the time of sourcing requests.
locale: en-US
release: zurich
product: Procurement
classification: procurement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Sourcing items in a service catalog request, Procurement, IT Asset Management]
---

# Source requests from local stockrooms

Get visibility into local stockrooms at the time of sourcing requests.

## Before you begin

You can source a request by using assets from the requester's local stockroom.

-   If stock is available in the local stockroom, the asset is reserved and follows the fulfillment task to source the request.
-   If the requester's location is supported by another stockroom as part of service locations, the asset can also be sourced from this stockroom.
-   If stock in the local stockroom is unavailable, you can get the assets transferred from other stockrooms or create a purchase order.

 

The Workflow Studio application is used to create the Asset Local Stock subflow to take you through the process of using assets from your local stockroom to source your request. As the subflow takes you through the various stages, the asset details are automatically updated. You can open the Asset Local Stock subflow to view the status of the stages in the subflow.

**Note:** Use decision tables to customize the Asset Local Stock subflow. For more details, see [Hardware Asset Management flow customization](../../hardware-asset-management/concept/readily-available-dec-tables-ham.md).

Role required:

-   procurement\_user or procurement\_admin
-   inventory\_user or inventory\_admin

## Procedure

1.  Log in with credentials for the role of procurement\_user or procurement\_admin.

2.  Navigate to **All** &gt; **Service Catalog** and select **Hardware**.

3.  Select the hardware item that you want to source and select **Order Now**

    Your request is submitted and the Order Status form layout appears.

4.  Select the request number.

5.  On the Request form layout, select the **Catalog Tasks** related list to view the sourcing task for the request.

6.  Select the sourcing task and select **Source Request**.

    ![Source request](../image/consumestock.png)

    The Sourcing form shows the following hardware sourcing request details:

    -   **Total requested**- Quantity of the hardware requested.
    -   **Requested for**- Name of the person for whom the hardware is requested.
    -   Location- Place where the hardware should be deployed.
    If the Source Request functionality or button isn't functioning as expected, confirm that the catalog task has both the **Parent** and **Request** fields populated. For more information, see [View and edit a catalog task](t_ViewAndEditACatalogTask.md). The Request ID, which is required for the Source Request page to function correctly is derived from the Parent field of the catalog task. If the Parent field is missing and the catalog task was created using Flow Designer, refer to the relevant [Set Parent field when creating Catalog Task from Flow Designer](https://support.servicenow.com/kb?sys_kb_id=1df9d8bc93a82ad07c79b36d6cba1058&id=kb_article_view) for further details.

7.  Select **Consume** to source the available stock from the local stockroom and from the stockroom that supports your location.

    If stock isn’t available in your local stockroomand the stockroom that supports your location, select **Transfer** or **Purchase** to source the request via a transfer order or a purchase order. If you create a transfer order and want the local stockroom to be included in the list of stockrooms to choose from, the admin must turn on the `glide.asset.procurement.sourcing.local_stock_transfer` property.

8.  Select **Source Stockroom** to select the stockroom from where you want to source the assets.

    If your location is associated with a stockroom as a service location, you can source from this stockroom along with the local stockroom. Service location capabilities enable a single stockroom to support multiple locations and consume the local stock efficiently. For more information on Service locations, see [Associate a stockroom with service locations](../../hardware-asset-management/task/associate-stockroom-with-service-locations.md).

    If the Asset pick task is enabled for the source stockroom, then this task is added to the Hardware Asset Refresh Request and Hardware Asset Request flows.

9.  In the **Consume Quantity** field, specify the quantity of assets that you want to consume from the stockroom that you selected.

10. Select **Reserved for** to specify a user for whom you want to source the request.

11. To source from multiple stockrooms, repeat steps 7–9.

12. Select **Submit**.

    A consume asset task is created. Assets are selected from the stockrooms and are reserved for the user who you selected in the **Reserved for** list. The state of the selected asset moves to in stock and the substate to reserved.

13. Log in with credentials for the role of inventory\_admin or inventory\_user.

14. Select the **Requested Items** related list and then select the request item.

15. Select the **Asset Tasks** related list and then select a task to select and assign an asset to the sourcing task.

    The Consume Asset Task form layout appears in the Asset Tasks module. Based on the type of asset \(hardware or consumable\) that is being sourced, fields in the form layout differ. The Assets Tasks module lists all the asset task records.

16. Change that you need and then close the task when you’re done.

    -   For hardware assets: Assets are auto-assigned to sourcing tasks but you can change an asset by selecting the **Asset** list. After you’re done, select **Close Task**.
    -   For consumable assets: The model for the asset appears on the form layout instead of the asset. Select **Close Task** or **Consume and Close**. If you select **Consume and Close**, the reserved asset is automatically picked up and assigned to the user. If you select **Close Task**, you must go to the Consumable form layout and assign an asset to the user manually.

**Parent Topic:**[Sourcing items in a service catalog request](../concept/c_SourcingRequestItems.md)

**Related topics**  


[Create a purchase order from a request](t_CreatingPurchOrderFromRequest.md)

[Create a transfer order from a request](t_CreatingTransferOrderFromReq.md)

[Add an assignment from a request](t_AddingAssignmentsFromReq.md)

