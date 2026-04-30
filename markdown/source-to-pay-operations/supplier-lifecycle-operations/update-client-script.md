---
title: Update the field names in the UX client script
description: Update the field names in the UX client script to match the custom field names in the custom API response.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring a custom API to dynamically fetch supplier news, News Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Update the field names in the UX client script

Update the field names in the UX client script to match the custom field names in the custom API response.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_ux_client_script.list`.

2.  In the UX Client Scripts form, in the **Name** search field, search for the Set 'news' activity state.

3.  Select the **Set 'news activity' section state** client script.

4.  Edit the **Script** field to update the field names so that they match the field names in the custom API response.

    For example, in your custom API response, if the **name** field entry is **title**, and the **description** field entry is **summary**, then you must update the field names accordingly in the script.

    ![UX client script.](../image/ux-client-script.png)

5.  Select **Update**.


**Parent Topic:**[Configuring a custom API to dynamically fetch supplier news](../concept/config-supplier-news-api.md)

**Previous topic:**[Add and configure the Get News data resource in UI Builder](add-config-news-data-resource.md)

**Next topic:**[Relish Integration for Supplier Lifecycle Operations](../concept/relish-slo-connector.md)

**Related topics**  


[Create a REST message for a custom API](create-custom-api-rest.md)

[Add and configure the Get News data resource in UI Builder](add-config-news-data-resource.md)

