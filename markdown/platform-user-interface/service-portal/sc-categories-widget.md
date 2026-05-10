---
title: SC Categories widget
description: The SC Categories widget displays Service Catalog categories. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# SC Categories widget

The SC Categories widget displays Service Catalog categories. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The system renders the categories available in this widget from the Categories table in Service Catalog \[sc\_category\].

![Screenshot for the SC Categories widget](../../../product/service-catalog-management/image/CategoryWidget.png "SC Categories widget")

If you associate your portal with multiple catalogs, then the SC Categories widget also includes a menu to select which catalog to browse.

![Menu to select a catalog](../../../product/service-catalog-management/image/sc-categories-menu.png)

For more information on associating your portal with catalogs, see [Configure a catalog in Service Portal](../task/associate-portal-catalog.md).

## Instance options

<table id="table_dlx_rw4_zz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Page

</td><td>

Defines what page opens when a user clicks a category. By default, this option redirects to the page for the selected category.

</td></tr><tr><td>

Number of categories to load

</td><td>

Specifies the number of categories displayed in the **Categories** pane. By default, ten categories are displayed. If there are additional categories, the **Show All** option is available.

</td></tr><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Bootstrap color

</td><td>

Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.

</td></tr><tr><td>

Category Layout

</td><td>

Select a flat or nested layout. A flat layout shows all of the available categories. A nested layout shows only the parent categories. Use a nested layout if you have a large number of categories to prevent an unnecessarily long list. Click ![Plus sign icon](../image/Expand.png) that appears next to a category with nested topics to expand the sub-categories.The widget only supports three levels of nesting. After level four, categories appear in the flat view.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Hide at XS

</td><td>

Hides the categories option on small screens, for example, on smart phones. The default is set to false.

</td></tr><tr><td>

Omit badges

</td><td>

Show or hide the number of items included in each category.

</td></tr><tr><td>

Check canView per item

</td><td>

Verifies with each item that the user has the right roles to view the catalog item.

</td></tr></tbody>
</table>**Note:** If a category contains more than 200 items, update the following instance options on this widget for better performance:

-   Category Layout: Flat
-   Omit badges: True
-   Check canView per item: False

**Parent Topic:**[Service Catalog widgets](sc-widgets.md)

**Related topics**  


[Catalog Content widget](catalog-content-widget.md)

[Catalog Homepage Search widget](cat-homepage-search-widget.md)

[Recent &amp; Popular Items widget](recent-and-popular-items-widget.md)

[Request Fields widget](request-fields-widget.md)

[Requested Items widget](requested-items-widget.md)

[Requests and Approvals widget](requests-and-approvals-widget.md)

[SC Catalog Item widget](sc-catalog-item-widget.md)

[SC Category Page widget](sc-category-page-widget.md)

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

[Access Service Catalog categories in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/access-categories-portal.md)

