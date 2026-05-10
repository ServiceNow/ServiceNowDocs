---
title: SC Category Page widget
description: Lists the catalog items available within a certain category. Categories are determined within the Service Catalog module. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# SC Category Page widget

Lists the catalog items available within a certain category. Categories are determined within the Service Catalog module. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

**Note:** Catalog items are sorted in ascending order by their **Order** value. If catalog items have the same order, they are sorted by the **Name** field.

![Service Catalog Category page widget](../image/WidgetSCCategoryPage.png "SC Category Page widget")

## Instance options

<table id="table_ebt_135_b1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Click event name

</td><td>

The name of the event that is emitted when a user clicks a catalog item.You can override the default behavior when clicking on a catalog item by providing a different event name. This would be in a situation where you embedded the category page in another widget.

The default value is `$sp.cat_item_list.click`.

</td></tr><tr><td>

Number of items to display per page

</td><td>

Number of items to display in the category page.**Note:** When defining the number of items to be displayed, consider the item data such as images and long descriptions. A large number may slow down the page performance.

</td></tr><tr><td>

Show items from Child Categories

</td><td>

Displays items in the child categories along with those in the parent category.**Note:** If the **Category Layout** instance options is set to `Flat` in the SC Categories widget, then set this instance option to `False`.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog widgets](sc-widgets.md)

**Related topics**  


[Catalog Content widget](catalog-content-widget.md)

[Catalog Homepage Search widget](cat-homepage-search-widget.md)

[Recent &amp; Popular Items widget](recent-and-popular-items-widget.md)

[Request Fields widget](request-fields-widget.md)

[Requested Items widget](requested-items-widget.md)

[Requests and Approvals widget](requests-and-approvals-widget.md)

[SC Catalog Item widget](sc-catalog-item-widget.md)

[SC Categories widget](sc-categories-widget.md)

[SC Order Guide widget](sc-order-guide-widget.md)

[SC Popular Items widget](sc-popular-items.md)

[SC Save Bundles widget](save-bundles-widget.md)

[SC Saved Carts widget](saved-cart-widget.md)

[SC Scroll to top widget](sc-scroll-to-top.md)

[SC Shopping Cart widget](sc-shopping-cart.md)

[SP Variable Editor widget](variable-editor-widget.md)

[SC Wish List Cart widget](sc-wish-list.md)

[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

