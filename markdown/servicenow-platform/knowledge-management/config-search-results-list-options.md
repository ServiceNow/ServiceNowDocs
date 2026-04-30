---
title: Configure search results list widget instance options
description: Configure widget instance options for the results list widget on the Knowledge Management Service Portal search results page.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure search results list widget instance options

Configure widget instance options for the results list widget on the Knowledge Management Service Portal search results page.

## Before you begin

Role required: sp\_admin or admin

## About this task

The search results page uses the Knowledge Result widget to provide display options for the returned list of results. Use the widget instance options to customize the display options.

## Procedure

1.  Navigate to the Knowledge Management Service Portal search results page.

2.  Control + right-click the list of returned search results.

3.  Click **Instance Options**.

4.  Configure the desired settings for the results list widget.

<table id="table_y2w_rhj_tz"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Glyph

</td><td>

An icon that appears in the search bar.

</td></tr><tr><td>

CSS

</td><td>

Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://www.servicenow.com/docs/access?context=scss-primer&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Show Relevancy Score

</td><td>

Shows how relevant each search result is based on the search term. The default setting uses the system property.

</td></tr><tr><td>

Breadcrumb: Hide Categories

</td><td>

Hides the category in the breadcrumb that appears below the article short description in the results list. The default setting uses the system property.

</td></tr><tr><td>

Breadcrumb: Knowledge Base Separator

</td><td>

The character used as a separator between the knowledge base and the category in the breadcrumb.

</td></tr><tr><td>

Breadcrumb: Category Separator

</td><td>

The character used as a separator between categories in the breadcrumb.

</td></tr><tr><td>

Default Sort Order

</td><td>

The default sort order for the list of returned results. The default sort order is **sys\_view\_count:desc**, which sorts the results by the number of views in descending order.

</td></tr><tr><td>

How to Display Attachments in Knowledge Search Results

</td><td>

How attachments are shown in the list of returned results. The default uses the system property.

</td></tr><tr><td>

Label for Show Pinned Articles Link

</td><td>

The text used for the pinned articles link.

</td></tr><tr><td>

Table

</td><td>

The table that stores the information returned in the search results.

</td></tr><tr><td>

Knowledge Secondary Fields

</td><td>

Fields that display additional information for each article in the search results.

</td></tr><tr><td>

Show Secondary Fields Label

</td><td>

Enable this check box to display the field labels for the additional information displayed for each result.

</td></tr><tr><td>

Pagination Type

</td><td>

Controls how additional knowledge article search results are displayed.-   **Standard Pagination:** displays the search results in multiple pages.
-   **Infinite Scroll:** displays the search results while scrolling.
 The default pagination type is set to **Infinite Scroll**.

</td></tr><tr><td>

Maximum no. of articles displayed per page with standard pagination

</td><td>

The maximum number of items included in a page when the search results list is displayed using standard pagination.

</td></tr><tr><td>

Maximum no. of articles displayed after first fetch during infinite scroll

</td><td>

The maximum number of items included when the search results list is first displayed using infinite scroll.

</td></tr><tr><td>

Maximum no. of articles displayed at subsequent fetches during infinite scroll

</td><td>

The maximum number of items included when the search results list updates as the user scrolls to the bottom.

</td></tr><tr><td>

No. of links in pagination bar

</td><td>

The number of links displayed in the pagination bar.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

