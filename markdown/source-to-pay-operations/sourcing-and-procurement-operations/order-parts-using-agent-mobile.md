---
title: Order parts you need using the Agent mobile application
description: Place an order for a part that you require to complete a particular work order task, from the Sourcing and Procurement Operations flow, using the Agent mobile application.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations integration with Field Service Management, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Order parts you need using the Agent mobile application

Place an order for a part that you require to complete a particular work order task, from the Sourcing and Procurement Operations flow, using the Agent mobile application.

## Before you begin

To successfully order a part, verify that the product models used by Field Service Management are aligned to the supplier products.

Role required: wm\_agent, wm\_dispatcher, fsm\_agent, or sn\_shop.shopper

## Procedure

1.  Log in to your instance in the Agent mobile application.

2.  From the **My Tasks** section, select the work order task you want to work with.

3.  Tap the **Parts** tab.

4.  From the **Part Requirements** section, select the part you need to complete your work order task.

5.  Tap **Order Part**.

6.  From the **Available to purchase** section, select the product you want to place an order for.

    This section displays all the supplier products that are associated with the product model of the part requirement.

    **Note:** Only products that have pricing available are displayed here. Also, all the criteria for products to be visible on Shopping Hub, such as shopping controls, are applied here as well.

    The quick checkout flow is triggered from Shopping Hub and the checkout details are auto-populated.

    **Note:** The **Quantity** and **Delivery date** fields are auto-populated from the part requirement, but are editable.

7.  Edit the checkout fields as required.

8.  Enter your reason for purchase in the **Purchase Reason** field.

9.  Tap **Complete Checkout**.

    A confirmation message stating that your purchase is successfully routed for approval, is displayed, along with the purchase requisition line number.

    **Note:** As an FSM agent, if you're unable to check out products in the PSM and FSM mobile experience Agent app, install the fix script after installing the fms-psm-mobile and spend-uib-portal applications. The fix script updates the quick checkout link to the correct MESP page.


## What to do next

On the order confirmation screen, tap **Return to work order task** if you want to go back to the work order task details screen.

**Parent Topic:**[Sourcing and Procurement Operations integration with Field Service Management](../concept/integration-psm-fsm.md)

