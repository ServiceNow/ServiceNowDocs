---
title: SC Catalog Item widget
description: Use this widget \(widget-sc-cat-item-v2\) to view the information about a catalog item and order the item. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# SC Catalog Item widget

Use this widget \(widget-sc-cat-item-v2\) to view the information about a catalog item and order the item. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

Configure [catalog items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_IntroductionToCatalogItems.md) using the Service Catalog in the platform UI by navigating to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

Catalog variables determine what information your users are allowed to select from, for example, color, size, or price. For more information on defining the variables for a catalog item, see [Create a service catalog variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_CreateAVariableForACatalogItem.md).

## Instance options

Use the widget instance options to customize the settings for the SC Catalog Item widget. To customize the settings for this widget, press the Ctrl key, click on the widget, and select **Instance Options**.

<table id="cat-item-instance-options"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Bootstrap color

</td><td>

Color of the widget based on the selections made in the Branding Editor.

</td></tr><tr><td class="sub-head" colspan="2">

Other Options

</td></tr><tr><td>

Show Add Cart Button

</td><td>

Displays the **Add to Cart** button in the Order Item widget.

</td></tr><tr><td>

Show field validation messages

</td><td>

Displays the **Required information** section with mandatory fields whose values are not specified.

</td></tr><tr><td>

Show Add/Update Wish List buttons

</td><td>

Displays the **Add to Wish List** or the **Update Wish List** buttons in the Order Item widget.

</td></tr><tr><td>

Order Item Section on Top

</td><td>

Displays the Order Item widget to the right of the catalog item form. Else, the Order Item widget is displayed below the catalog item form.

</td></tr><tr><td>

Enable Show More/Less for Item description on Mobile

</td><td>

Enables the **Show more** or **Show less** options for the catalog item description in the mobile view. By default, the **Show more** option is available. -   Click **Show more** to display the entire description.
-   Click **Show less** to display only 150 characters of the description.

</td></tr></tbody>
</table>**Note:** For a record producer, you can edit the label of the **Submit** button by using the widget instance options.

For example, if you want to change the label to **Request**, press Ctrl+click on the catalog item widget, select **Instance in Page Editor**, and specify the following parameters in the **Additional options, JSON format** field.

```
"record_producer_label":{
			"value" : "Request"
		}
```

**Parent Topic:**[Service Catalog widgets](sc-widgets.md)

**Related topics**  


[Catalog Content widget](catalog-content-widget.md)

[Catalog Homepage Search widget](cat-homepage-search-widget.md)

[Recent &amp; Popular Items widget](recent-and-popular-items-widget.md)

[Request Fields widget](request-fields-widget.md)

[Requested Items widget](requested-items-widget.md)

[Requests and Approvals widget](requests-and-approvals-widget.md)

[SC Categories widget](sc-categories-widget.md)

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

[Request a catalog item from Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/request-cat-item-portal.md)

