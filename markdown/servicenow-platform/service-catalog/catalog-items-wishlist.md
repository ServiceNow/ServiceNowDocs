---
title: Saving catalog items to a wish list
description: You can save catalog items to your wish list and visit them later to complete the ordering process.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Catalog for managers and end users, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Saving catalog items to a wish list

You can save catalog items to your wish list and visit them later to complete the ordering process.

For example, you need a laptop with specific software installed on it. Add the laptop to your wish list, then visit it when you have the complete software configuration list. Data you enter is saved when you add items to your wish list.

Users with catalog\_admin or admin role can enable/disable the wish list feature and [configure the wish list cart](../task/service-catalog-screens.md#) for end users. By default, the wish list is always disabled for a catalog.

To enable the wish list feature for catalog end users, select the check box for **Enable Wish List** in the [catalog record](c_MultipleServiceCatalogs.md#).

The wish list feature does not function if the property glide.ui.doctype is set to **false**.

![Catalog homepage displaying wish list feature](../image/WishListHeader.png "Catalog homepage displaying wish list feature")

**Note:** When the wish list feature is disabled for a catalog, any items in its wish list are deleted. The items in the wish list are retained only if the item is associated with another wish list-enabled catalog.

## Working with wish lists

To save an item to your wish list, click **Add to Wish List** on the catalog item page. A pop-up dialog informs you that the item is added to your wish list. Duplicate entries of an item are not added to your wish list. If you try to add an item that is already in your wish list, the latest entry of that item gets updated in the wish list.

![](../image/WishListPopUp.png "Wish list popup dialog")

To access your wish list of catalog items, click **View Wish List** on the popup dialog. You can also click the link to wish list items on the header. The [wish list cart](../task/service-catalog-screens.md#fig_jzm_byk_vw) allows you to update or delete wish list items.

To update a wish list item, go to wish list cart and click **View** for the item. Change the information, and then click **Update** to save the changes. To proceed with ordering the item, click **Add to Cart**. The item is removed from your wish list and added to the shopping cart for final checkout.

**Parent Topic:**[Service Catalog for managers and end users](c_UsingTheServiceCatalog.md)

