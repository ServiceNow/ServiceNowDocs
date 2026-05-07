---
title: Create a product offering for a remote catalog item
description: Create a product offering in a Service Exchange provider instance. When you publish the product offering, a remote record producer is created for the remote catalog item.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring Service Exchange Order Management for Providers, Order Management for providers with Service Exchange, Integrate, Sales Customer Relationship Management]
---

# Create a product offering for a remote catalog item

Create a product offering in a Service Exchange provider instance. When you publish the product offering, a remote record producer is created for the remote catalog item.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin or sn\_prd\_pm.product\_catalog\_manager

## About this task

When you're creating the product offering, use the **Distribution channel** field to set the channel to Service Exchange.

## Procedure

1.  In the CSM Configurable Workspace on the provider instance, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Offerings** &gt; **Product Offerings**.

3.  Select **New**.

    On the Details tab, fill in the fields.

<table id="table_us3_z1p_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-assigned number for the product offering.

</td></tr><tr><td>

Name

</td><td>

Alternative name for the product offering to help differentiate it from similar product names.

</td></tr><tr><td>

Display name

</td><td>

Name of the product offering that is added.

</td></tr><tr><td>

Offering type

</td><td>

Offering entity. Select one of the following types:-   Product: A product entity that an agent can add to an order using the CSM Configurable Workspace.
-   Entitlement: An entity such as a warranty or subscription that can be added to an order by an agent.


</td></tr><tr><td>

Offering sub-type

</td><td>

Type of entitlement:-   Warranty
-   Extended warranty
-   License
-   Subscription


</td></tr><tr><td>

Sellable

</td><td>

Option indicating that the product offering can be sold as a standalone item. If not selected, the product offering can be sold as part of bundle but not as a standalone item.**Note:** If you're using the Service Exchange Order Management for Providers application, select this option for a product offering. Only sellable product offers create remote catalog items. Offers with bundled configurations are not supported.

</td></tr><tr><td>

Description

</td><td>

Short description of the product offering. The description helps the order agent understand the product when placing an order.

</td></tr><tr><td>

Start date

</td><td>

Date and time that the product offering is available for Sales Customer Relationship Management applications. Select the Calendar icon ![](../image/field-calendar.png) to choose the start date and time, then select **OK**.

</td></tr><tr><td>

End date

</td><td>

Date and time that the product offering is deleted from Sales Customer Relationship Management applications. Select the Calendar icon ![](../image/field-calendar.png) to choose the end date and time, then select **OK**.

</td></tr><tr><td>

State

</td><td>

State of the product offering. States include In Draft, Published, Retired, and Archived. You can update product offerings In Draft state.

</td></tr><tr><td>

Distribution channel

</td><td>

Option to set and lock in a distribution channel. For example, you can specify web as a channel. You can specify multiple channels. **Note:** If you're using the Service Exchange Order Management for Providers application, enter Service Exchange as the channel.

</td></tr><tr><td>

Owner

</td><td>

Person responsible for the product offering.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

</td></tr><tr><td>

Product specification

</td><td>

Product specification to associate with the product offering. It provides a functional view of a product offering that drives order fulfillment.**Note:** Only published specifications appear.

</td></tr><tr><td>

Product model

</td><td>

Name of the product model.

</td></tr><tr><td>

Copy child specification characteristics

</td><td>

Option that when selected copies all child specification characteristics in a specification hierarchy. For example, if the product offer has an associated product specification, selecting this option indicates that the characteristics are inherited from the child specifications in addition to the parent specification.

</td></tr><tr><td>

Pricing method

</td><td>

Pricing method for the product:-   One-time: A single fee for the product.
-   Recurring: A fee that occurs at scheduled intervals. You can set the periodicity for a recurring fee.
**Note:** Pricing information is not visible on the consumer instance. If a default or other price list is configured for an offer, the price is calculated and updated only on the provider instance.

</td></tr><tr><td>

Periodicity

</td><td>

Recurring pricing: Monthly or annually.

</td></tr><tr><td>

Monthly recurring charges

</td><td>

Charges that recur every month. Monthly recurring charges are supported for backward compatibility. Use price lists to define prices.

</td></tr><tr><td>

Non recurring charges

</td><td>

Charges that are applied once. Supported for backward compatibility. Use price lists to define prices.

</td></tr><tr><td>

Create contract

</td><td>

Option that indicates to agents that entitlement contracts can be added to the product order. If selected, service contracts are created after order fulfillment. Used when entitlements are managed as contracts.

</td></tr><tr><td>

Contract term

</td><td>

Length of the contract:-   12 months
-   24 months
-   36 months
-   48 months
-   60 months


</td></tr><tr><td>

Version

</td><td>

Version number that is assigned to this product offering version.

</td></tr><tr><td>

Initial version

</td><td>

Name of the product offering at the time you created the initial version.

</td></tr><tr><td>

Previous version

</td><td>

Name of the previous version of the product offering, For example:-   When you create the initial version of the product offering \(for example, version 1\), this field is empty.
-   When you create a version \(version 2\) with a slightly different name, the name of the product offering at its initial creation appears here.
-   When you create a subsequent version \(version 3\), the name of the product offering as it was at version 2 appears here.
 You can't change this field.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Add additional characteristics to your product offering, if needed.

6.  Add product visuals to your product offering.

    1.  In the Product Visuals tab, select **New**.

    2.  Enter a name for the visual.

    3.  To select an image file to upload, select **Click to add**.

    4.  To set your image as the primary image for the product, select **Set Primary**

        **Note:** You can add multiple images for products, but the service catalog only supports one image per product when it is published to the service catalog.

7.  When you finish creating the product offering version, select one of the following actions.

<table id="choicetable_dt3_z1p_ccc"><thead><tr><th align="left" id="d43606e536">

Action

</th><th align="left" id="d43606e539">

Description

</th></tr></thead><tbody><tr><td id="d43606e545">

**Publish**

</td><td>

Publish the draft product offering so that you can use it in a product catalog:-   When you publish it, its state changes from Draft to Published.
-   After you publish a product offering, you can't change or delete it, unless you create a version for it.


</td></tr><tr><td id="d43606e563">

**Update**

</td><td>

Update the product offering with the new data that you added, but don't publish it for use in a product catalog.

</td></tr><tr><td id="d43606e572">

**Copy**

</td><td>

Copy the data in this product offering so that you can create a product offering from it. For example, you can use the Copy function if you want to create a base version product offering that is similar to Premium SD-WAN Offering v3, but with a separate version track.

 When you use the Copy function, it creates a base version product offering and sets the values in these fields:

-   **Version**: 1 \(base version\)
-   **Initial Version**: Premium SD-WAN Offering v3
-   **Previous Version**: blank


</td></tr></tbody>
</table>
## What to do next

[Associate consumer criteria to a remote record producer](associate-criteria-remote-catalog.md) for this remote catalog item.

