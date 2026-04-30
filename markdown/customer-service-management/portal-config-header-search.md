---
title: Configure the search option for your portal header
description: Configure search feature to display search option on your portal.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Portal Polaris Header widget for your portal, Portal Polaris Header widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure the search option for your portal header

Configure search feature to display search option on your portal.

## Before you begin

The Portal Next Experience theme should have been activated.

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portal**.

2.  On the Service Portal page, search and select `Customer Support` in the Title column.

3.  On the Customer Support page, in the **Quick start config** field, modify the JSON as shown.

    ```
    "headerSearch": {
                    "display_search": true,
    "search_placeholder_text": "Search articles and request items",
    "exclude_search_for_pages": "csm_home_new"
    ```

4.  Modify the placeholder text.

    The default text is `Search articles and request items`.

5.  Select **Update**.


