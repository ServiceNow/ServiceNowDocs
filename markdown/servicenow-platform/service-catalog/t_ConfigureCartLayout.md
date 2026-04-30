---
title: Configure the cart layout
description: Configure cart layout records to define functionality for widgets or screens in the shopping cart.When you enable cart layouts, service catalog properties are impacted. Consider the possible outcomes and alter the settings or properties to achieve the cart layout and functionality you require.Configure macros that define functionality for elements within each widget or screen.Create macros for cart layout records using Jelly scripts to define customized behavior and display within a widget or screen.Set fields in the Catalog Item form to configure the cart layout for specific items.Service catalog enables you to use additional methods to configure cart behavior or layouts, which override cart layout record settings.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Cart layout, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the cart layout

Configure cart layout records to define functionality for widgets or screens in the shopping cart.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Select a widget or screen.

    -   [Cart widgets](service-catalog-cart-widgets.md#): Item Ordering Widget, Shopping Cart Widget, or Item Ordering Widget \(Order Guide\)
    -   [Preview screens](service-catalog-screens.md#): Cart Preview Screen, Cart Preview Screen \(Two Step\), Cart Preview Screen \(Wish List\), or Cart Preview Screen \(Classic Mobile\)
    -   [Order status screens](service-catalog-status-screens.md#): Order Status Screen or Order, Status Screen \(Classic Mobile\)
3.  Update the **Title** field to change the title that appears on the widget.

4.  Leave the default **Target** value.

    Do not change this value because it identifies the cart element being defined.

5.  Update the other sections of the cart layout record, as required.

    The availability of these sections varies for each widget and screen record.

    -   In the **Components** section, select the components to display, such as delivery times, item descriptions, and prices.
    -   In the **Columns** section, select which columns to display, such as the item description column, delivery time column, or price column.
    -   In the **Buttons** section, select the buttons to display, such as **Add to Cart**, **Edit Cart**, and **Delete Item**.
    -   In the **Button Labels** section, enter new labels to replace the default button labels.

        A new label is used on all screens that the button appears on. For example, the **Continue Shopping** button is used on several screens, so changing its label affects all those screens.

6.  If required, configure the widget and column macros.

7.  Save the record, and then test the results of your configuration by ordering items from your service catalog.

    Some settings and properties in your instance can override or affect your cart layout.


**Parent Topic:**[Cart layout](../concept/c_ConfigureCartLayout.md)

## Cart layout considerations

When you enable cart layouts, service catalog properties are impacted. Consider the possible outcomes and alter the settings or properties to achieve the cart layout and functionality you require.

Some of these properties are impacted when you use cart layouts. For example, with the order status screen, the **When to show prices and sub-totals on the Service Catalog Cart** \(glide.sc.price.display\) property overrides cart layout settings for displaying prices.

<table id="table_fvh_2rd_cr"><thead><tr><th>

Property

</th><th>

Impact

</th></tr></thead><tbody><tr><td>

Allow ESS users the option to cancel their requests from the checkout screen.\[glide.sc.checkout.cancel\]

</td><td>

Overridden when the **Cancel Request** check box in cart layout settings is selected. If this check box is selected, the **Cancel** button is displayed even if the property is set to **No**.

</td></tr><tr><td>

Enable cloning requests during checkout.\[glide.sc.allow.checkout.clone\]

</td><td>

Not used \(deprecated\) if cart layouts are enabled. Replaced by the **Clone Checkout**check box in cart layout settings.The **Clone Checkout** check box is cleared by default for new instances. For upgraded instances, the check box is set to the existing value of the glide.sc.allow.checkout.clone property.

</td></tr><tr><td>

List of roles \(comma-separated\) that can use the quantity selector in the shopping cart\[glide.sc.allow.quantity\]

</td><td>

Overrides any relevant cart layout settings.

</td></tr><tr><td>

Show the request item number for each line item on the checkout screen \(default false\).\[glide.sc.checkout.request.number\]

</td><td>

Not used \(deprecated\) if cart layouts are enabled. Replaced by the **Request Item Number column** check box in cart layout settings.

</td></tr><tr><td>

Show the 'Back to Catalog' button on the two-step checkout screen.\[glide.sc.checkout.twostep.back\]

</td><td>

Not used \(deprecated\) if cart layouts are enabled. Replaced by the **Back to Catalog** check box in cart layout settings.

</td></tr><tr><td>

When to show prices and subtotals on the Service Catalog Cart.\[glide.sc.price.display\]

</td><td>

Overrides any relevant cart layout settings.

</td></tr></tbody>
</table>## Configure widget and column macros

Configure macros that define functionality for elements within each widget or screen.

### Before you begin

Role required: admin

### About this task

Some widgets or screens also have column macros that define the horizontal layout and configuration of shopping cart contents.

You can configure these macros to alter the display order of elements, or hide elements, within the widget or screen. You can also create new macros to implement any extra requirements.

### Procedure

1.  Navigate to **All** &gt; **Widget Macros** &gt; **Column Macros** related list.

2.  Click the order number entry of a macro to edit its display order, or to activate or deactivate it.

    ![Configure widgets and column macros.](../image/Service_Catalog_Cart_Layout_Widget_Macro-Editable-Details.png)

3.  Click **Update**.

4.  Click the **Widget / View Macro** entry of a macro to view its functionality settings.

    You cannot edit functionality settings for default macros, but these settings can be a useful reference for creating your own widget macros.


## Create macros for cart layout

Create macros for cart layout records using Jelly scripts to define customized behavior and display within a widget or screen.

### Before you begin

Role required: admin

### About this task

Macros that you create do not affect upgrades because customized widget functionality is isolated from general cart behavior.

### Procedure

1.  Open the relevant cart layout record.

2.  Navigate to **Widget Macros** or **Column Macro**related list.

3.  Click **New**.

4.  Enter details for the macro.

    |Field|Description|
    |-----|-----------|
    |Name|The name for the new macro.|
    |Active|A check box to indicate whether the macro is displayed or not.|
    |Description|A summary of how the macro is used.|
    |Active|A check box to indicate whether the macro is displayed or not.|
    |XML|The Jelly script to apply for your macro.|

5.  Save the macro record.


### Example

This example demonstrates the script to add a **Requested for reference** field as a widget macro to a cart layout record.

```
<?xml version="1.0" encoding="utf-8" ?>
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
    <j:set var="ref" value="sc_cart" />
    <j:set var="jvar_ref" value="${jvar_cart.getRequestedFor()}" />
    <j:set var="jvar_ref_display" value="${jvar_cart.getRequestedForDisplayName()}" />
    <tr>
        <td colspan="3">
            ${gs.getMessage('Requested for')}:
        </td>
    </tr>
    <tr>
        <td colspan="3" style="padding: 4px;">
            <g:catalog_requested_for />
        </td>
    </tr>
</j:jelly>
```

## Configure cart layout for specific items

Set fields in the Catalog Item form to configure the cart layout for specific items.

### Before you begin

Role required: admin

### About this task

Overrides any general [cart layout settings](t_ConfigureCartLayout.md#). For example, you can hide the price of an item by setting the **Omit price in cart** field to **true** for that item.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

2.  Select the catalog item.

3.  Configure the form to add both **Use cart layout** and any of the following item configuration fields you require:

    -   Omit price in cart
    -   No cart
    -   No order
    -   No order now
    -   No proceed checkout
    -   No quantity
4.  Clear the **Use cart layout** check box to display the configuration fields for that item.

5.  Set the item configuration field values as required.

    ![](../image/SC_ConfigCartLayoutSpec.png)

6.  Click **Update**.


## Override cart layouts for items

Service catalog enables you to use additional methods to configure cart behavior or layouts, which override cart layout record settings.

For example, your cart layout record settings can hide item prices, but you might decide to display the price of the **Sales Laptop**. In that case, you would set the relevant configuration values on that catalog item. Be aware of the impact of these additional methods, to ensure that your cart behaves in the way you want.

**Note:**

If you are [migrating to cart layouts](../concept/c_MigrateCartLayouts.md), you can have defined additional settings and properties that impact your cart layout settings.

