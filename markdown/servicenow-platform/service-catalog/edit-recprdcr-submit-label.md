---
title: Edit the label of Submit button for a record producer
description: For a record producer submission experience that you can relate to, edit the label of the Submit button.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request experience in Now Mobile, Service Catalog in mobile, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit the label of Submit button for a record producer

For a record producer submission experience that you can relate to, edit the label of the **Submit** button.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Select the SC Catalog Item \(widget-sc-cat-item-v2\) widget.

3.  From the Instances related list, preview and open the instance for the ServiceNow NowMobile App – Catalog Screens and Applet Launcher application.

4.  In the **Additional options, JSON format** field, specify the **record\_producer\_label** parameter.

    For example, if you want to change the label to **Request**, press Ctrl+click on the catalog item widget, select **Instance in Page Editor**, and specify the following parameters in the **Additional options, JSON format** field.

    ```
    "record_producer_label":{
    			"value" : "Request"
    		}
    ```

5.  Click **Update**.


**Parent Topic:**[Request experience in Now Mobile](../concept/now-mobile-catalog.md)

**Related topics**  


[Configure catalogs](../../../administer/mobile-employee/task/configure-catalog.md)

[Browse catalog items using the catalog hierarchy](now-mob-browse-cat-item-catalog.md)

[Submit and track a request](../../../administer/mobile-employee/task/order-item.md)

[Create a quick action in your mobile applications](../../../administer/mobile-employee/task/sc-quick-action.md)

[Enable notifications in Now Mobile](enable-notification-mobile.md)

[Enable the cart in Now Mobile](enable-cart-mobile.md)

[Configure Now Mobile properties](config-now-mob-properties.md)

