---
title: Configure Service Catalog preview screens
description: You can configure shopping cart preview screens for the one-step and two-step carts, for the wish list, and for the Classic Mobile app.Using Service Catalog, customize the cart preview screen for wish list items.Using Service Catalog, customize the shopping cart screen that is displayed on mobile devices.Using Service Catalog, customize the shopping cart display screen for a one-step checkout process.Using Service Catalog, customize the shopping cart display screen for a two-step checkout process.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Cart layout, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Catalog preview screens

You can configure shopping cart preview screens for the one-step and two-step carts, for the wish list, and for the Classic Mobile app.

**Parent Topic:**[Cart layout](../concept/c_ConfigureCartLayout.md)

## Configure the wish list screen

Using Service Catalog, customize the cart preview screen for wish list items.

### Before you begin

Role required: admin, catalog\_admin

### About this task

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Open the **Cart Preview Screen \(Wish List\)** record.

3.  You can add/remove components, columns, buttons, and rename labels.

    For more information, see [Configure cart layout](t_ConfigureCartLayout.md#).

4.  Click **Update**.

    ![](../image/WishlistCartPreview.png "Cart preview screen for wish list items")


## Configure Classic Mobile shopping cart screen

Using Service Catalog, customize the shopping cart screen that is displayed on mobile devices.

### Before you begin

**Important:**

Mobile Classic Is Deprecated!

The App Has Been Removed From The Stores And Can No Longer Be Activated. We Are Not Offering Enhancements, Bug Fixes, Or Support For The App. See ServiceNow Classic Mobile App Deprecation Effective September 15, 2022.

Role required: admin, catalog\_admin

### About this task

The shopping cart on Classic Mobile devices always uses a two-step checkout process. You cannot modify widget macros or button labels on Classic Mobile devices.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Open the **Cart Preview Screen \(Classic Mobile\)** record.

3.  You can add/remove components and buttons.

4.  Click **Update**.

    ![Default mobile shopping cart screen](../image/Service_Catalog_Mobile_Shipping_Cart_View.png "Shopping cart screen on Classic Mobile")


## Configure a one-step shopping cart screen

Using Service Catalog, customize the shopping cart display screen for a one-step checkout process.

### Before you begin

Role required: admin, catalog\_admin

### About this task

One-step checkout is the default checkout process for catalog items.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Open the **Cart Preview Screen** record.

3.  You can add/remove components, columns, buttons, and rename title and button labels.

    See [Configure cart layout](t_ConfigureCartLayout.md#).

4.  Click **Update**.

    ![](../image/1StepCheckoutScreen.png "Shopping cart screen displayed for default one-step checkout process")


## Configure a two-step shopping cart screen

Using Service Catalog, customize the shopping cart display screen for a two-step checkout process.

### Before you begin

Role required: admin, catalog\_admin

### About this task

Changes made to the two-step record are visible only if the [two-step checkout process is enabled](../concept/c_EnableATwoStepCheckout.md#) in properties. By default, catalog items use a one-step checkout process.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**.

2.  Open the **Cart Preview Screen \(Two Step\)** record.

3.  You can add/remove components, columns, buttons, and rename title and button labels.

    For more information, see [Configure cart layout](t_ConfigureCartLayout.md#).

    In the **Components** tab, both **Shipping Location** and **Shipping Address** are not supported simultaneously. Deselect the selected component to select the other component.

    If you enable **Shipping Address** in the **Components** tab, the editable **Shipping address** field is displayed in the cart preview screen. If you enable **Shipping Location** in the **Components** tab, the editable **Shipping location** field and a read-only **Shipping address** field are displayed in the cart preview screen.

4.  Click **Update**.

    ![Shopping cart preview screen for a two-step checkout process when shipping address in enabled.](../image/ShpngAdrssCartPrevw.png "Shopping cart preview screen for a two-step checkout process when shipping address in enabled")

    ![Shopping cart preview screen for a two-step checkout process when shipping location in enabled.](../image/ShpngLoctnCartPrevw.png "Shopping cart preview screen for a two-step checkout process when shipping location in enabled")


