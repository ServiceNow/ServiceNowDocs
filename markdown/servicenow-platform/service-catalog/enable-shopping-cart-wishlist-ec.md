---
title: Enable Shopping Cart and Add to Wish List options in Employee Center
description: Modify the Main Menu configuration of the Employee Center to provide the Shopping Cart and Add to Wish List options while requesting catalog items.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Catalog in Employee Center portal, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable Shopping Cart and Add to Wish List options in Employee Center

Modify the Main Menu configuration of the Employee Center to provide the Shopping Cart and Add to Wish List options while requesting catalog items.

## Before you begin

Enable the wish list feature for catalog. For information about enabling the wish list, see [Saving catalog items to a wish list](../concept/catalog-items-wishlist.md).

Role required: admin

## About this task

The Shopping Cart and Add to Wish List menu options that are available by default on the Service Portal are not available in the Employee Center. You must enable these options in the Employee Center to allow employees to add catalog items to the Shopping Cart and Wish List.

If these features are not required, then consider disabling these options in Service Catalog for a seamless experience in the Employee Center. To enable or disable the shopping cart option in Service Catalog follow the first three steps mentioned in the [Enable the Shopping Cart Widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/enable-shopping-cart.md) topic and for information on enabling or disabling the Wish list option in Service Catalog, see [Saving catalog items to a wish list](../concept/catalog-items-wishlist.md) topic.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Search for and select **Employee Center**.

3.  If you are prompted with the message `To edit this record click here`, then click **here**.

4.  Open the **Main menu** by clicking the preview this record icon \(![Preview this record icon](../image/preview_record.png)\).

5.  Change the values for **enable\_cart** and **enable\_wishlist** to **True**.

    ```
    {
    	"enable_cart":{
    		"displayValue":"true",
    		"value":true
    	},
    	"auto_update_cart":{
    		"displayValue":"true",
    		"value":true
    	},
    	"exclude_search_on_homepage":{
    		"displayValue":"true",
    		"value":true
    	},
    	"enable_wishlist":{
    		"displayValue":"true",
    "value":true
    ```

6.  Click **Update**.


## Result

The Shopping Cart and Add to Wish List options appear on the Employee Center.

**Parent Topic:**[Service Catalog in Employee Center portal](../concept/service-catalog-in-ec.md)

