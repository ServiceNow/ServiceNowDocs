---
title: SC Order Guide widget
description: Use this widget \(widget-sc-order-guide-v2\) to request an order guide, that is, a single service catalog request for several catalog items with a specific purpose. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# SC Order Guide widget

Use this widget \(widget-sc-order-guide-v2\) to request an order guide, that is, a single service catalog request for several catalog items with a specific purpose. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

Configure [order guides](https://www.servicenow.com/docs/access?context=c_ServiceCatalogOrderGuides&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) using the Service Catalog in the platform UI by navigating to **Service Catalog** &gt; **Catalog Definitions** &gt; **Order Guides**.

The order guide form comprises the following sections:

## Describe Needs

This section displays the following that are associated with the order guide:

-   Image
-   Description
-   Variables

## Choose Options

This section displays a list of catalog items included in the order guide based on the information provided in the **Describe Needs** section and the rule base configured for the order guide. Each catalog item is displayed with its name and description on an accordion.

Each accordion displays:

-   **Options**, if a catalog item has fields that need user inputs.

    **Note:** If the fields are mandatory, a red asterisk is displayed beside **Options**.

-   A toggle to include the catalog item in the order guide request. You can make it mandatory to include all items in the order guide request by not displaying the toggle. You can make it optional to include items in the order guide request by displaying the toggle. To display the toggle for each catalog item of the order guide, select the **Show Include Toggle \(Service Portal\)** check box while configuring the order guide. For more information, see [Create an order guide](https://www.servicenow.com/docs/access?context=t_CreateAnOrderGuide&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) .

    **Note:** When an item is excluded from the order guide request, the item is not editable and the corresponding mandatory field restrictions are ignored.


## Summary

This section provides a summary of the order guide that you can review before requesting the order guide.

## Instance options

Use the widget instance options to customize the settings for the SC Order Guide widget. To customize the settings for this widget, press the Ctrl key, click on the widget, and select **Instance Options**.

<table id="order-guide-instance-options"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Title

</td><td>

Name of the order guide.

</td></tr><tr><td>

Bootstrap Color

</td><td>

Color of the widget based on the selections made in the Branding Editor.

</td></tr><tr><td>

Enable Show More/Less for Item description on Mobile

</td><td>

Enables the **Show more** or **Show less** options for the description of the order guide or the associated catalog items in the mobile view. By default, the **Show more** option is available. -   Click **Show more** to display the entire description.
-   Click **Show less** to display only 150 characters of the description.

 **Note:** This instance option is applicable for the description of the order guide in the **Describe Needs** section, and the description of the associated catalog items in the **Choose Options** section.

</td></tr><tr><td>

Compact Mode

</td><td>

Displays the widget in the compact mode when configured for smaller real estates \(less than 6\*6\).

</td></tr><tr><td>

Hide Delivery Time

</td><td>

Hides the delivery time for each catalog item in the accordion. It is not applicable for the order guide summary page and the delivery time is never displayed on the summary page.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

Show Add to Cart

</td><td>

Option to display the **Add to Cart** button on the order guide summary page.

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

[SC Category Page widget](sc-category-page-widget.md)

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

[Request an order guide from Service Portal](https://www.servicenow.com/docs/access?context=request-order-guide-portal&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Configure order guide widgets](https://www.servicenow.com/docs/access?context=service-catalog-cart-widgets&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

