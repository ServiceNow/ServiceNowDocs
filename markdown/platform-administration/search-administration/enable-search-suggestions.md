---
title: Enable and disable Search Suggestions in Zing
description: Enable the Search Suggestions application to improve the Zing search user experience.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing displays search suggestions as users enter search terms, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable and disable Search Suggestions in Zing

Enable the Search Suggestions application to improve the Zing search user experience.

## Before you begin

ServiceNow personnel installed and activated the com.glide.search.suggestions plugin.

Role required: admin

## About this task

The Search Suggestions application is available on new instances by default. On upgraded instances, Search Suggestions is enabled for Now Mobile and disabled for Service Portal by default.

The following system properties enable and disable Search Suggestions:

-   **glide.search.suggestions.enabled**: Set to **true** \(default\) to enable Search Suggestions in Zing, or set to **false** to disable Search Suggestions in Zing.
-   **glide.service\_portal.search\_as\_you\_type\_behavior**: Select **Suggestions** or **Typeahead** functionality in the Service Portal.

On new instances, the first parameter is set to **true** and the second is set to **Suggestions**. In upgraded instances, the parameters are set to whatever was previously enabled.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  To switch between Search Suggestions and type-ahead functionality in Service Portal, follow these steps.

    1.  In the **Name** search column, enter **glide.service\_portal.search\_as\_you\_type\_behavior**.

    2.  On the System Property page, in the **Value** field, enter `Suggestions` to enable Search Suggestions, or `Typeahead` to enable type-ahead functionality.

        You can only enter one of these options.

3.  To turn Search Suggestions on or off globally, follow these steps.

    1.  In the **Name** search column, enter **glide.search.suggestions.enabled**.

    2.  In the **Value** field, double-click the value and select **true** to enable suggestions, or **false** to disable Search Suggestions globally.


**Parent Topic:**[Zing displays search suggestions as users enter search terms](../concept/search-suggestions-zing.md)

**Related topics**  


[Set the maximum number of search suggestions Zing displays](set-max-num-of-suggestions.md)

