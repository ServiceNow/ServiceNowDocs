---
title: Lead time calculations
description: Lead time \(in days\) of a supplier product consist of the time for sourcing, supplier onboarding, purchasing, and shipping for a supplier product, product model, or a product category. Each of these durations are used to calculate the total lead time which determines the number of days to execute a purchase order.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Setting up primary data for Shopping Hub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Lead time calculations

Lead time \(in days\) of a supplier product consist of the time for sourcing, supplier onboarding, purchasing, and shipping for a supplier product, product model, or a product category. Each of these durations are used to calculate the total lead time which determines the number of days to execute a purchase order.

## Supplier onboarding time

Supplier onboarding time indicated the average number of days to onboard a new supplier for a product of a category. The initial default value is 15 days, as defined in the sn\_shop.default.supplier.onboard.time property of the purchasing properties table.

When a purchase requisition is created for a supplier product, it can have a purchasing task of type supplier onboarding. Over time, as purchase requisitions are completed, the onboarding time for a supplier is updated automatically as follows:

For a product category: Supplier onboarding time = Sum \[Actual Duration of supplier tasks for purchase requisitions with purchase lines in a category\]/Number of Supplier onboarding tasks.

Example calculation of supplier onboarding time:

<table id="table_cfn_p5b_hlb"><tbody><tr><td class="sub-head">

Purchase Requisition A for Supplier A

</td><td class="sub-head">

Purchase Requisition B for Supplier B

</td><td class="sub-head">

Purchase Requisition C for Supplier C

</td></tr><tr><td>

-   Supplier Task = Onboarding; Actual duration = 13 days
-   Purchase line 1: Product Category = Hardware
-   Purchase line 2: Product Category = Software

</td><td>

-   Supplier Task = Onboarding; Actual duration = 15 days
-   Purchase line 3: Product Category = Hardware

</td><td>

-   Supplier Task = Onboarding; Actual duration = 21 days
-   Purchase line 4: Product Category = Software

</td></tr><tr><td class="sub-head" colspan="3">

Calculated supplier onboarding time in days

</td></tr><tr><td colspan="3">

-   Hardware product category = \(13+15\)/2 = 14
-   Software product category = \(13 + 21\)/2 = 17

 **Note:** If the calculation produces a decimal, always round up regardless of the value.

</td></tr></tbody>
</table>## Sourcing time

Sourcing time indicates the average number of days taken to source a product from a supplier, if sourcing is required for products of a category.

The initial default value is three days, as defined in the sn\_shop.default.sourcing.time property of the purchasing properties table. This value is updated over time, as sourcing requests for a supplier product are completed.

The sourcing time for a product category, product model, or supplier product is updated as follows:

1.  The actual duration values of all sourcing requests for supplier products are considered. An average of these values is calculated. This average is the new default sourcing time for this supplier product.
2.  When the sourcing time is updated for a supplier product, it is recalculated for the related product model as an average of the sourcing times of all its supplier products.
3.  When the sourcing time is updated for a product model, it is recalculated for the related product category as an average of the sourcing times of all its product models.

For any new product model, the sourcing time is the same as its referenced model category. For any new supplier product, the sourcing time is the same as its referenced product model.

**Note:**

-   If **Spend categorization** of a product category is **Not Addressable**, the sourcing time is always 0.
-   If the Purchase Line is of the state **Closed Canceled**, it indicates that sourcing did not occur for that purchase line. In this case, the average sourcing time of the supplier product is not updated.

Example calculation of sourcing time:

<table id="table_by1_tvb_hlb"><tbody><tr><td class="sub-head" colspan="3">

Sourcing Request A for MacBooks

</td></tr><tr><td colspan="3">

Actual duration = 16 days

</td></tr><tr><td>

Purchase line 1 – Reseller A MacBook -   Purchase requisition line \(PRL\) State = Closed Rejected
-   Product Model = MacBook
-   Product Category = Hardware

</td><td>

Purchase Line 2 – Reseller B MacBook -   PRL State = Pending Approval
-   Product Model = MacBook
-   Product Category = Hardware

</td><td>

Purchase Line 3 – Apple MacBook \(assume current sourcing time is 11 days\) -   PRL State = Closed Canceled
-   Product Model = MacBook
-   Product Category = Hardware

</td></tr><tr><td class="sub-head" colspan="3">

Sourcing Request B for Lenovo Think Pads

</td></tr><tr><td colspan="3">

Actual duration = 22 days

</td></tr><tr><td>

Purchase line 4 – Reseller A Lenovo Think Pad -   PRL State = Closed Rejected
-   Product Model = MacBook
-   Product Category = Hardware

</td><td colspan="2">

Purchase Line 5 – Reseller B Think Pad -   PRL State = Pending Approval
-   Product Model = MacBook
-   Product Category = Hardware

</td></tr><tr><td class="sub-head" colspan="3">

Calculated sourcing time in days

</td></tr><tr><td colspan="3">

-   Reseller A MacBook = 16
-   Reseller B MacBook = 16
-   Apple MacBook = 11
-   MacBook Product Model = \(16 + 16 + 11\)/3 = 15
-   Reseller A Lenovo ThinkPad = 22
-   Reseller B Lenovo ThinkPad = 22
-   Lenovo ThinkPad Product Model = \(22 + 22\)/2 = 22
-   Hardware Product Category = \(15 + 22\)/2 = 19

 **Note:** If the calculation produces a decimal, always round up regardless of the value.

</td></tr></tbody>
</table>## Purchasing time

Purchasing time indicates the average number of days taken to complete the purchase requisition workflow and create purchase orders for products in a category.

The initial default value is five days, as defined in the sn\_shop.default.purchasing.time property of the purchasing properties table. This value is updated over time, as purchase requisitions for a supplier product are completed.

The purchasing time for a product category, product model, or supplier product is updated as follows:

1.  The actual duration values to complete all purchase requisitions for supplier products are considered. An average of these values is calculated. This average is the new default purchasing time for this supplier product.
2.  When the purchasing time is updated for a supplier product, it is recalculated for the related product model as an average of the purchasing times of all its supplier products.
3.  When the purchasing time is updated for a product model, it is recalculated for the related product category as an average of the purchasing times of all its product models.

If the purchase requisition is of the Blanket order type, the purchase time for its purchase lines is not updated. Example calculation of purchasing time:

<table id="table_mdn_twb_hlb"><tbody><tr><td class="sub-head">

Purchase Requisition A for Reseller A

</td><td class="sub-head">

Purchase Requisition B for Reseller B

</td><td class="sub-head">

Purchase Requisition C for Reseller B

</td><td class="sub-head">

Purchase Requisition D for Reseller A

</td></tr><tr><td>

-   Actual duration = 16 days
-   Purchase line 1
    -   Supplier product = Reseller A Apple MacBook
    -   Product Model = MacBook
    -   Product Category = Hardware
-   Purchase line 2
    -   Supplier Product = Reseller A Office 365
    -   Product Model = Office 365
    -   Product Category = Software

</td><td>

-   Actual duration = 13 days
-   Purchase line 3
    -   Supplier Product = Reseller B MacBook
    -   Product Model = MacBook
    -   Product Category = Hardware

</td><td>

-   Actual duration 21 days
-   Purchase line 4
    -   Supplier Product = Reseller B Office 365
    -   Product Model = Office 365
    -   Product Category = Software

</td><td>

-   Actual duration = 7 days
-   Purchase line 5
    -   Supplier Product = Reseller A Lenovo ThinkPad
    -   Product Model = Lenovo ThinkPad
    -   Product Category = Hardware

</td></tr><tr><td class="sub-head" colspan="4">

Calculated purchasing time in days

</td></tr><tr><td colspan="4">

-   Reseller A MacBook = 16
-   Reseller B MacBook = 13
-   MacBook Product Model = \(16+13\)/2 = 15
-   Reseller A Lenovo Think Pad = 7
-   Lenovo Think Pad Product Model = 7
-   Hardware Product Category = \(15+7\)/2 = 11
-   Reseller A Office365 = 16
-   Reseller B Office365 = 21
-   Office 365 Product Model = \(21+16\)/2 = 19
-   Software product category = 19

 **Note:** If the calculation produces a decimal, always round up regardless of the value.

</td></tr></tbody>
</table>## Shipping time

Shipping time indicates the estimated number of days taken to ship a supplier product to a delivery location. This value is retrieved from the shipping time of a supplier.

Whenever the shipping time for a supplier is updated, the shipping times of all the supplier products belonging to that supplier reflect the same.

If the supplier product is created through a third-party integration, then the shipping time is updated from the values of the integration, and not from the supplier record.

**Note:** If the product type of the supplier product is **Service**, then the value of shipping time is always 0.

## Total lead time

Total lead time indicates the numbers of days taken to execute the purchase order of a supplier product and deliver it to the employee.

For a supplier product, the total lead time is calculated as:

-   If sourcing and supplier onboarding are required,

    Total lead time = \[Supplier onboarding time from the referenced product category\] + \[Sourcing time of the supplier product\] + \[Purchasing time for the supplier product\] + \[Shipping time of the supplier product\].

-   If sourcing is required but supplier onboarding is not required,

    Total lead time = \[Sourcing time of the supplier product\] + \[Purchasing time for the supplier product\] + \[Shipping time of the supplier product\].

-   If sourcing is not required and supplier onboarding is required,

    Total lead time = \[Supplier onboarding time from the referenced product category\] + \[Purchasing time for the supplier product\] + \[Shipping time of the supplier product\].

-   If sourcing and supplier onboarding are not required,

    Total lead time = \[Purchasing time for the supplier product\] + \[Shipping time of the supplier product\].


![Total lead time for a supplier product](../image/total-lead-time.png)

The total lead time of a supplier product is recalculated every time the values of the above fields on the supplier product form are updated.

**Note:** All the lead times are recalculated and refreshed after completion of each purchase requisition. For these calculations, only the purchase requisition data of the recent 12 months is considered.

**Parent Topic:**[Setting up primary data for Shopping Hub](set-up-master-data-shopping-hub.md)

