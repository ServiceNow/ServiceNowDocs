---
title: Create a transfer order from a request
description: You can create a transfer order directly from a request to source hardware items and consumables from stockrooms.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Sourcing items in a service catalog request, Procurement, Asset Management, IT Service Management]
---

# Create a transfer order from a request

You can create a transfer order directly from a request to source hardware items and consumables from stockrooms.

## Before you begin

Role required: procurement\_admin or procurement\_user

**Important:** If the Field Service Management application is also activated on your ServiceNow instance, then a workflow in this application processes the transfer orders. For more information, see [Move an asset through the transfer process](https://www.servicenow.com/docs/access?context=create-transfer-order-line-task&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

## Procedure

1.  View procurement requests.

<table id="choicetable_ugf_l3l_4xb"><thead><tr><th align="left" id="d346718e68">

UI

</th><th align="left" id="d346718e71">

Action

</th></tr></thead><tbody><tr><td id="d346718e77">

**Core UI**

</td><td>

Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Requests**.

</td></tr><tr><td id="d346718e101">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.
2.  In the Procurement list, select **Requests**.


</td></tr></tbody>
</table>2.  Select a request that has been approved but not sourced.

    Check the **Request State** and **Sourced** columns.

3.  In the **Catalog Tasks** related list, select a sourcing task.

4.  Select **Source Request**.

    The Source Request or Sourcing page appears with a list of all the requested items.

5.  Create a transfer order.

    |UI|Action|
    |---|------|
    |**Core UI**|Select **Add Transfer Order**.|
    |**Hardware Asset Workspace**|Select **Transfer**.|

6.  On the Sourcing page of the Hardware Asset Workspace, select the **Source through distribution channel** check box to source the assets from the inbound distribution channels that support the destination stockrooms.

    **Note:** The **Source through distribution channel** check box that enables you to source through a distribution channel for Transfer orders appears only in the Hardware Asset Workspace. Your preference of selecting or clearing this check box is saved and is shown when you open the Sourcing page again.

    You can associate the location of the requester as a service location with multiple stockrooms for better location coverage. Also, these stockrooms can be associated with multiple inbound stockrooms or distribution channels for optimized transfer of assets between the stockrooms. Distribution channels enable you to source the assets from the stockrooms that you prefer for sourcing based on the rank that you provide to the stockrooms.

    For more information, see [Associate a stockroom with service locations](https://www.servicenow.com/docs/access?context=associate-stockroom-with-service-locations&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) and [Link stockrooms into a distribution channel](https://www.servicenow.com/docs/access?context=associate-stockroom-with-distribution-channels&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

7.  In the **Source stockroom** list, select a stockroom from which the hardware item should be sourced.

    **Note:** In the Hardware Asset Workspace, the Source stockroom list shows only the inbound distribution channels of the stockrooms that support the location of the requester under the following conditions:

    1.  When you’ve selected the **Source through distribution channel** option.
    2.  When the inbound distribution channels are added to the stockrooms that support the location of the requester.
8.  In the **Transfer Quantity** field, specify the quantity you want to transfer.

    The **In stock** column, displays the total stock available with the selected source stockroom.

9.  In the **Destination stockroom** list, select the destination to which the requested item or items should be delivered.

    **Note:** In the Hardware Asset Workspace, the Destination stockroom list shows only the stockroom that supports the location of the requester under the following conditions:

    1.  When you’ve selected the **Source through distribution channel** option.
    2.  When the location of the requester is added as a service location of one or more stockrooms.
10. Select **Submit**.

    A transfer order is created to move the item or items from the **Source stockroom** location to the **Destination stockroom** location. When you view the request, the **Sourced** check box is selected.


**Parent Topic:**[Sourcing items in a service catalog request](../concept/c_SourcingRequestItems.md)

**Related topics**  


[Create a purchase order from a request](t_CreatingPurchOrderFromRequest.md)

[Source requests from local stockrooms](consume-local-asset-stock.md)

[Add an assignment from a request](t_AddingAssignmentsFromReq.md)

[Manage transfer orders](https://www.servicenow.com/docs/access?context=c_TransferOrders&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)

