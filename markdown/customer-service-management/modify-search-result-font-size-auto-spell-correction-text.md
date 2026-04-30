---
title: Default font sizes for search result text in Engagement Messenger
description: Define normal and genius search result font sizes to change text appearance in Engagement Messenger on different devices.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Engagement Messenger, Set up Engagement Messenger, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Default font sizes for search result text in Engagement Messenger

Define normal and genius search result font sizes to change text appearance in Engagement Messenger on different devices.

**Note:** The ec\_admin role is required to change the default configuration.

<table id="table_mxg_gyz_m4b"><thead><tr><th>

Search type

</th><th>

Default configuration

</th></tr></thead><tbody><tr><td>

Normal search for Knowledge Base and Catalog

</td><td>

The default normal search result font size settings are:

-   Large for title
-   Medium for summary

 **Note:**

-   This setting for knowledge bases is located in the **em\_kb\_search\_template** template script.
-   This setting for Catalog is located in the **em\_catalog\_search\_template** template script.

 The default auto spell correction text font size is medium.

 **Note:** The default configuration is set in the Faceted Search widget.

</td></tr><tr><td>

Genius search for Knowledge Base and Catalog

</td><td>

The default genius search result font size settings are:

-   Small for identifier
-   Large for heading
-   Medium for summary

 **Note:**

-   This setting for knowledge bases is located in the **em\_qa\_genius\_results\_template** template script.
-   This setting for Catalog is located in the **em\_catalog\_genius\_results\_template** template script.

</td></tr></tbody>
</table>![Search results examples of normal search results, showing auto-spell correction, title text, and summary text.](../image/normal-search-result.jpg "Normal search result text appearance in Engagement Messenger")

![Genius search result with automatic font size adjustment for identifier text, heading text, and description text.](../image/genius-result.jpg "Genius search result text appearance in Engagement Messenger")

