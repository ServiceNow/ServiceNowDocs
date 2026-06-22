---
title: Select, review, revise, or request cancellation of a service order
description: Review the account, contact, pricing, and date details on a telecommunications service order to make sure that it is correct and complete. You can also revise or request a cancellation of the service order. OM revamp project - This topic has been removed from the SOM bundle on Oct 14, 2025.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-review-service-order-detail.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service orders for fulfillment, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Select, review, revise, or request cancellation of a service order

Review the account, contact, pricing, and date details on a telecommunications service order to make sure that it is correct and complete. You can also revise or request a cancellation of the service order.

## Before you begin

Role required: sn\_ind\_tmt\_orm.service\_order\_agent, sn\_ind\_tmt\_orm.service\_order\_manager

## Procedure

1.  Navigate to **All** &gt; **Service Order Management** &gt; **Workspace** &gt; **Configurable Workspace Home**.

    **Note:** If you aren't using configurable workspaces, navigate by using the following path:

    **Workspace Experience** &gt; **Workspaces** &gt; **Agent Workspace Home**.

    To learn more about migrating to configurable workspaces, see [Migrate to Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/migrate-to-configurable-workspace.md).

    If you have an assigned Service Order Manager or Service Order Agent role, the Service Order Management workspace appears. If the Service Order Management workspace doesn't appear, do the following actions:

    1.  From the Configuration Workspace Lists icon \[Omitted image "list-outline-24.svg"\] Alt text:, click **Service Orders**.
    2.  Do one of the following:

        -   To view all service orders, click **All**.
        -   To view only open, unfulfilled service orders, click **Open**.
        **Note:** To learn more about creating or updating service order details, see [Creating orders in Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/creating-orders-som.md).

    3.  Select the service order that you want to review, verify, and approve:
        -   To refresh the form, click the refresh icon \[Omitted image "form-refresh.png"\] Alt text:.
        -   To filter existing service orders, click the filter icon \[Omitted image "form-filter.png"\] Alt text:.
2.  Select the service order to review by clicking the appropriate tile.

3.  On the Customer Order form, review the order number, account, and contact information for the selected service order.

4.  To revise or request cancellation of the service order, perform one of the following actions.

<table id="choicetable_vdb_2cb_fqb"><thead><tr><th align="left" id="d40810e179">

Action

</th><th align="left" id="d40810e182">

Description

</th></tr></thead><tbody><tr><td id="d40810e188">

**Revise a customer or service order**

</td><td>

In the Customer Order form, do the following actions:1.  Click **Revise Order**.
2.  Make the required revisions to the order.
3.  When the Confirmation dialog appears, click **OK**, or click **Cancel** to skip the revision of the order.
**Note:** If the **PONR** option is selected, the **Revise Order** button is turned off because it is too far along in the process to revise.

When you revise an order, the following actions take place:

-   The **State** field changes to Revision Received.
-   The **Version** field increments to the next version number.
-   The **Revision Operation** field is set to Update.
-   If there are any associated order tasks, their state fields change to On Hold.


</td></tr><tr><td id="d40810e252">

**Revise a customer or service order line item**

</td><td>

In the Order Line Items form, do the following actions:1.  Using the check boxes to the left of the order lines, select those that require revision. To revise all order line items, select the check box to the left of the **Number** title. For example, if your order consists of four line items, you could select single individual line items, or all items for revision.
2.  Make the required revisions to the order line item.
3.  Click **Revise Order Line**.
4.  When the Confirmation dialog appears, click **OK**, or click **Cancel** to skip the revision of the order line item.
**Note:** If the **PONR** option is selected, the **Revise Order** button is turned off because it is too far along in the process to revise.

When you revise an order line item, the following actions take place:

-   The **State** field changes to Revision Received.
-   The **Version** field increments to the next version number.
-   The **Revision Operation** field is set to Update.
-   If there are any associated order tasks, their state fields change to On Hold.


</td></tr><tr><td id="d40810e322">

**Request cancellation of an entire customer or service order**

</td><td>

In the Customer Order form, do the following actions:1.  Click **Cancel Order**.
2.  When the Confirmation dialog appears, click **OK**, or click **Cancel** to skip the cancellation request.
**Note:** If the **PONR** option is selected, the **Cancel Order** button is turned off because it is too far along in the process to request a cancellation.

When you request an order cancellation, the following actions take place:

-   The **State** field changes to Assessing Cancellation.
-   The **Version** field increments to the next version number.
-   The **Revision Operation** field is set to Cancel.
-   Notification messages appear if there are any conditions that are preventing cancellation of the order. A designated manager must approve the order cancellation.
**Note:** To cancel an individual order line item, in the Order Line Item form, change the **State** field to Assess Cancellation.

</td></tr><tr><td id="d40810e389">

**Request cancellation of individual customer or service order line items**

</td><td>

In the Order Line Item form, do the following actions:1.  Click **Revise Order**.
2.  Make the required revisions to the order line item.
3.  When the Confirmation dialog appears, click **OK**, or click **Cancel** to skip the revision of the order line item.
4.  Click **Cancel Order Line Item**.
 **Note:** The **PONR** check box, which is located on the Customer Order and Order Line item forms, indicates the Point of No Return state for the order or order line item.

</td></tr></tbody>
</table>    **Note:** To learn more about inflight order changes, see [Managing inflight order changes and cancellation requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/inflight-order-change-mgt-overview.md).

5.  In the service order, make the required changes, and then select **Save**.


