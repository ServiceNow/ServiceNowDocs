---
title: Configure Now Mobile properties
description: Define the behavior of various catalog entities in Now Mobile.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Request experience in Now Mobile, Service Catalog in mobile, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Mobile properties

Define the behavior of various catalog entities in Now Mobile.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  On the Service Catalog Configuration form, select the **Mobile** section.

3.  Configure the required properties.

<table id="table_dld_pvm_fmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog category sort option in Now Mobile \(**glide.sc.mobile.category.order\_by**\)

</td><td>

Sort option for categories in Now Mobile.-   Title: Categories are sorted by their title. By default, categories are sorted alphabetically by their title.
-   Order: Categories are sorted by their order.


</td></tr><tr><td>

Include 'Desktop only' Items in Now Mobile \(**glide.sc.mobile.include\_desktop\_only\_items**\)

</td><td>

Option to include the catalog item with **Availability** set to `Desktop only` in Now Mobile.

</td></tr><tr><td>

Catalog item classes not available in Now Mobile \(comma separated list\) \(**glide.sc.mobile.item\_class\_not\_supported**\)

</td><td>

Catalog item types to exclude in Now Mobile. For example, `sc_cat_item_content, sc_cat_item_producer`

</td></tr><tr><td>

Experience for items not available in Now Mobile \(**glide.sc.mobile.unsupported\_discover**\)

</td><td>

Option to define the non-availability behavior of a catalog item. Possible options:-   Discoverable-show message that item is not viewable in Now mobile: Item is discoverable in the search and browse experience but not viewable.
-   Not discoverable-do not show in search and browse experience: Item is neither discoverable in the search and browse experience nor viewable.
 **Note:**

-   If AI Search is enabled for Now Mobile, this property is not applicable.
-   This property is supported only when one of the following properties are applicable:
    -   Include 'Desktop only' Items in NOW Mobile \(**glide.sc.mobile.include\_desktop\_only\_items**\)
    -   Catalog item classes not available in Now Mobile \(comma-separated list\) \(**glide.sc.mobile.item\_class\_not\_supported**\)


</td></tr><tr><td>

Primary color for buttons in the catalog request experience in Now Mobile \(**glide.sc.mobile.primary\_color**\). If Next Experience is turned on, the property will be ignored.

</td><td>

Color for buttons in the catalog request experience.

</td></tr></tbody>
</table>    **Important:** The following properties are interdependent.

    -   Include 'Desktop only' Items in NOW Mobile
    -   Catalog item classes not available in NOW Mobile \(comma separated list\)
    -   Experience for items not available in NOW Mobile
<table id="table_tqc_wjn_fmb"><thead><tr><th>

Availability value of the catalog item

</th><th>

Include 'Desktop only' Items in NOW Mobile \(true\)

</th><th>

Include 'Desktop only' Items in NOW Mobile \(false\) Desktop only

</th></tr></thead><tbody><tr><td>

Desktop only

</td><td>

Viewable in search and browse experience

</td><td>

-   If set as discoverable using the **Experience for items not available in NOW Mobile** property, viewable in search and browse experience, but not available when you click the item.
-   If set as not discoverable, not viewable in search and browse experience


</td></tr><tr><td>

Desktop and Classic Mobile

</td><td>

Always viewable in search and browse experience

</td><td>

Always viewable in search and browse experience

</td></tr><tr><td>

Classic Mobile only

</td><td>

Not viewable in search and browse experience

</td><td>

Not viewable in search and browse experience

</td></tr></tbody>
</table>    |Experience for items not available in NOW Mobile property value|Items excluded using the Catalog item classes not available in NOW Mobile \(comma separated list\) property|
    |---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
    |Discoverable-show message that item is not viewable in the mobile|Item types are viewable in search and browse experience, but not available when you click them.|
    |Not discoverable-do not show in search and browse experience\)|Item types do not appear in search and browse experiences|

4.  Click **Save**.


**Parent Topic:**[Request experience in Now Mobile](../concept/now-mobile-catalog.md)

**Related topics**  


[Configure catalogs](../../../administer/mobile-employee/task/configure-catalog.md)

[Browse catalog items using the catalog hierarchy](now-mob-browse-cat-item-catalog.md)

[Submit and track a request](../../../administer/mobile-employee/task/order-item.md)

[Create a quick action in your mobile applications](../../../administer/mobile-employee/task/sc-quick-action.md)

[Enable notifications in Now Mobile](enable-notification-mobile.md)

[Enable the cart in Now Mobile](enable-cart-mobile.md)

[Edit the label of Submit button for a record producer](edit-recprdcr-submit-label.md)

