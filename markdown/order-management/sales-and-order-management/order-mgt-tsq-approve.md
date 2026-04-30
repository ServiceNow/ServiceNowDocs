---
title: Review and approve service qualification requests
description: Review and approve customer orders captured through the Technical Service Qualification API.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-15"
reading_time_minutes: 2
breadcrumb: [Service qualification requests, Managing service orders, Order Management, Use, Sales Customer Relationship Management]
---

# Review and approve service qualification requests

Review and approve customer orders captured through the Technical Service Qualification API.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_fulfilment\_manager, sn\_ind\_tmt\_orm.order\_fulfilment\_agent, sn\_ind\_tmt\_orm.service\_order\_manager, sn\_ind\_tmt\_orm.service\_order\_agent

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Service Orders** &gt; **All**.

4.  Select an order with the Order type as Service and Fulfillment type as Qualify.

5.  Select **Approve**.

    The State field changes to **In Progress** and order decomposition occurs and service orders are generated for each customer order line Item.

    **Note:** During order decomposition, only service orders are created, resource orders are not generated for service qualification requests.

6.  Navigate to the **Line Items** tab, select a parent line item in the list and select **Qualify Order**.

    **Note:** The **Qualify Order** option is available only on the top order line items in the hierarchy.

    -   The Result field is updated to **Pending** and the [Process Qualification Request subflow](../reference/order-mgt-tsq-subflow.md) subflow is launched. After the subflow has been executed, depending on the response from the external inventory system, the Customer Order Result field is updated to one of the following:
        -   Qualified: Requested service is available.
        -   Alternate: Requested service is not available but an alternate proposal is available.
        -   Unqualified: Requested service and alternate proposals are not available.
        -   None: If any errors occur during the execution, the result is updated to None.
    -   The following business rules are invoked to derive the result:

        -   Update Line Item Qualification Result: Propagates result from domain order to order line item.
        -   Update Qualification Result on Order: Propagates result from top order line items to the customer order.
        The Customer Order Result status is based on the status of the domain order and order line items. If the order line items have different or mixed results, the Result status is derived as follows:

        |Domain order|Order line item result|
        |------------|----------------------|
        |All domain orders are set to Qualified.|Qualified|
        |All domain orders are set to Alternate.|Alternate|
        |All domain orders are set to Unqualified|Unqualified|
        |All domain orders are set to None|None|

        |Top Order Line Item|Customer Order Result|
        |-------------------|---------------------|
        |All top order line items are set to **Qualified**.|Qualified|
        |At least one top order line item is set **Alternate** and no items are set to **Unqualified**.|Alternate|
        |At least one top order line item is set to **Unqualified**|Unqualified|
        |At least one top order line item is set to **None**|None|

    **Manually updating the qualification request**

    You can manually update the Result field in two ways:

    -   Update the `qualificationresult`field inn the `api/sn_ord_qual_mgmt/qualification/checkServiceQualification/processResult` API for all the order line items.
    -   Update the Result field on the Domain Order, Order Line Item, and top Order Line Item forms. The Result field on the Customer Order is also updated.
    **Data model changes**

    The following forms have been updated to process service qualification requests:

    -   Customer order
        -   Result: Can be None, Qualified, Unqualified, Alternate, or Pending.
        -   Fulfillment code: Readonly field.
    -   Order line item

        Result: Can be None, Qualified, Unqualified, Alternate, or Pending.

    -   Domain order

        -   Result: Can be None, Qualified, Unqualified, Alternate, or Pending.
        -   Unavailability reason

**Parent Topic:**[Service qualification requests](../concept/order-mgt-tsq-about.md)

