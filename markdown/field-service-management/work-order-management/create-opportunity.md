---
title: Create a sales opportunity
description: Create sales opportunities for services, products, or assets identified during field service visits using the ServiceNow Agent application.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Create a sales opportunity

Create sales opportunities for services, products, or assets identified during field service visits using the ServiceNow Agent application.

## Before you begin

Role required: wm\_technician\_sales\_write

## About this task

-   Technician driven sales with the Field Service \(com.snc.fsm\_technician\_sales\) plugin and the Opportunity Management store application \(com.sn\_l2c\_oppty\_mgmt\) must be installed.
-   With the `wm_technician_sales_write` role, you can create opportunities before starting a task or while the task is in progress.

## Procedure

1.  Open the ServiceNow Agent application.

2.  Create a sales opportunity.

<table id="choicetable_z2w_ytf_ytb"><thead><tr><th align="left" id="d82958e105">

From

</th><th align="left" id="d82958e108">

Do this

</th></tr></thead><tbody><tr><td id="d82958e114">

**My Work**

</td><td>

1.  Tap **My Work**.
2.  In the **My Tasks** section, select the relevant work order task.
3.  Tap Overflow action ![overflow action icon](../image/more_actions1.png) icon.
4.  Tap **Create opportunity**.


</td></tr><tr><td id="d82958e153">

**My Work**

</td><td>

1.  Tap **My Work**.
2.  In the **My Tasks** section, select the relevant work order task.
3.  In the **Related** tab, tap **Create opportunity**.


</td></tr><tr><td id="d82958e186">

**Sales**

</td><td>

1.  Tap **Sales**.
2.  Tap **Create opportunity**.


</td></tr></tbody>
</table>    When the **Create Opportunity** form appears, a few fields will be auto-populated.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Short Description|Enter a brief description of the opportunity.|
    |Work order task|Work order task number is auto-populated if the opportunity is based on the work order task. This field becomes optional to create an opportunity without a work order task.|
    |Account|Enter customer account reference.|
    |Contact|Enter the customer contact reference.|
    |Sales cycle type|Enter the type of sales cycle \(e.g., Newcust, Renew, Upsell\). The default value is Upsell.|
    |Stage|Enter the stage of the opportunity \(e.g., Qualify, Develop, Propose, Negotiate, Closed-Won, Closed-Lost\). The default value is Qualify.|
    |Rating|Set the rating \(e.g., Hot for top rating\). The default value is Hot.|
    |Calling allowed|Option to allow calls. By default, the option is enabled.|
    |Email allowed|Option to allow emails. By default, the option is enabled.|
    |Sharing allowed|Option to allow share. By default, the option is enabled.|

4.  Tap **Submit**.

    The opportunity is created and appears in the **Sales** tab. If associated with a work order task, it also appears in the **Related** tab.

5.  Add a product to the opportunity.

    1.  Tap **Add line** on the created opportunity.

    2.  In the **Product offering** field, select the product.

    3.  In the **Quantity** field, enter the quantity.

    4.  In the **Unit of measure**, select the unit.

    5.  Tap **Submit**.

        The product line item is added to the opportunity.


## Result

Tap the opportunity in the **Related** tab to view the details and **Activity** stream of the line items.

