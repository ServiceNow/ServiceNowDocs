---
title: Empty state display
description: Use an empty state to indicate to your users that the displayed page does not contain data. You can add an image, text, and buttons to direct users to perform an action, view a particular screen, or review specific information.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile app components, Building mobile apps, Mobile Platform]
---

# Empty state display

Use an empty state to indicate to your users that the displayed page does not contain data. You can add an image, text, and buttons to direct users to perform an action, view a particular screen, or review specific information.

In some situations, such as the first time a user accesses a page or if no relevant items are listed on a page, data might not be displayed. You can configure a default empty state to be displayed in those situations. You can customize additional empty states for particular lists and screens. If an empty state is not defined for specific lists and screens, the default empty state is used.

## Empty state display hierarchy  

The default empty state is triggered for all screens and segments without an associated empty state. An empty state defined for a specific screen takes priority over the default empty state. An empty state defined for embedded lists takes priority over an empty state defined for a screen.

**Note:** There is a separate default empty state for search results. You can also define an empty state if no search results are listed, after a navigation tab is selected.

<table id="table_shj_3dy_24b"><tbody><tr><td>

![Default empty state.](../image/empty-state-default.png "Default empty state")

</td><td>

![Configured empty state with an image, a line of text and two buttons.](../image/empty-state-real.png "Configured empty state")

</td></tr></tbody>
</table>## Empty state structure

You can define up to one image element, two text elements, and three button elements within a single empty state display. The elements are displayed in the vertical alignment in the order image, text, and then button. The following graphic shows the element order with its corresponding element name. Unused elements are not displayed in the empty state.

![Empty state with predefined system names used in configuration.](../image/empty-state-element-callout.png "Empty state with predefined system names used in configuration")

