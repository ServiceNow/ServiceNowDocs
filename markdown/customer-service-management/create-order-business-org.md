---
title: Create an order for business organizations
description: Begin the ordering process in Order Management for business organizations by selecting a customer account or consumer and entering the required information to create a product order.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order Management for business location, Integration with Sales Customer Relationship Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create an order for business organizations

Begin the ordering process in Order Management for business organizations by selecting a customer account or consumer and entering the required information to create a product order.

## Before you begin

Plugins required:

-   sn\_bus\_org\_orm

Roles required:

-   sn\_bus\_org\_orm.org\_b2b\_sales\_rep,
-   sn\_bus\_org\_orm.org\_b2c\_ sales\_rep,
-   sn\_bus\_org\_orm.org\_sales\_mgr,
-   sn\_bus\_org\_orm.org\_relationship\_mgr, or
-   sn\_bus\_loc.org\_sales\_mgr

-   Confirm that the Business Function is set to Sales and the Business Organization is active.

## About this task

When you start an order, a pop-up prompts you to enter details. The pop-up window adapts based on your role. Either the **Account** or **Consumer** field appears.

-   If you have a B2B role, you can create orders for customer accounts.
-   If you have a B2C role, you can create orders for consumers.

    **Note:** Managers can also view child business locations and onboard agents to a business location.


## Procedure

1.  In the Configurable Workspace, select the List view.

2.  Navigate to **Customer Orders** &gt; **All** and select **New**.

    The Create a new order pop-up opens.

    ![create a new order](../image/create-order-business-org.png "Create a new order")

3.  On the Create a new order pop-up, create an order for either an account or consumer.

<table id="choicetable_wss_lcm_11c"><thead><tr><th align="left" id="d265286e151">

To

</th><th align="left" id="d265286e154">

Description

</th></tr></thead><tbody><tr><td id="d265286e160">

**Create an order for an account**

</td><td>

1.  Select **Account**.
2.  Enter the following:
    -   **Order Type**: Order type can be service or customer.
    -   **Contact**: Name of the primary customer contact.
    -   **Order action**: Select the type of order action.


</td></tr><tr><td id="d265286e198">

**Create an order for a consumer**

</td><td>

1.  Select the **Consumer** name.
2.  Enter the following:
    -   **Order Type**: Order type can be service or customer.
    -   **Order action**: Select the type of order action.


</td></tr></tbody>
</table>4.  In **Order action**, select **Add**.

5.  Select the **Channel partner**.

    -   The Channel Partner field is available only when the Order Management for Business Location store app \(sn\_bus\_org\_orm\) is installed.
    -   The field is automatically prefilled if the agent is assigned to a single business location.

        **Note:** If the agent is assigned to multiple business locations, the field remains empty and must be selected manually.

    -   The field is also prefilled when an **Account** or **Consumer** is selected, based on its associated Channel Partner.
6.  Select **Create**.


## Result

The order is started and the Order Catalog opens.

