---
title: Modify the News feed widget
description: The News feed widget displays articles on company news and announcements. All news, Other news, and Related news are instances of the News feed widget.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-20"
reading_time_minutes: 2
breadcrumb: [Configure employee communications widgets, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Modify the News feed widget

The News feed widget displays articles on company news and announcements. All news, Other news, and Related news are instances of the News feed widget.

## Before you begin

Role required: sp\_admin or admin

Learn more about the news widgets: [News articles](../concept/ec-news-articles.md)

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    The Employee Center home page is displayed.

2.  Press and hold the control key, right-select the News feed widget, and then select **Instance Options**.

3.  Configure the widget:

    **Note:** News can be directed to other widget instances, provided that the content is published within the News Feed widget. The targeted news will automatically appear on the designated widget, eliminating the task of configuring any content assigned to that widget.

<table id="table_lgk_4yj_crb"><thead><tr><th>

Widget option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Load Async

</td><td>

Loads widget data in the background. If you select this option, the Employee Center homepage will appear even if the News widget hasn't finished loading.

</td></tr><tr><td>

Show title

</td><td>

Option to display the news article header title

</td></tr><tr><td>

Title

</td><td>

Title of the widget

</td></tr><tr><td>

Show thumbnail

</td><td>

Displays a thumbnail image for each news article

</td></tr><tr><td>

Show sub-headline

</td><td>

Option to display the news article sub-headline

</td></tr><tr><td>

Inline loading

</td><td>

The article reading page \(cd\_news\_article\) enables employees to open other news articles from the Article detail page without refreshing the entire page.

 **Note:** This is only intended to be used on the article reading page.

</td></tr><tr><td>

Enable grid/list controls

</td><td>

Displays an option for the user to switch between a grid and list view of news articles

</td></tr><tr><td>

Default view

</td><td>

Sets the default view for news articles:-   **List**: Arranges articles in a vertical list.![News feed widget list view](../images/ec-news-widget-list.png)
-   **Grid**: Arranges articles in a grid with a maximum three articles per row.![News feed widget grid view](../images/ec-news-feed-widget-grid.png)


</td></tr><tr><td>

Show categories

</td><td>

Option to show or hide the assigned categories

</td></tr><tr><td>

Pagination type

</td><td>

How users navigate through news articles. The choices are:-   **Dotted**: Displays navigable dots representing each page of articles.
-   **Numbered**: Displays navigable page numbers.
-   **Call to action**: Displays a button with a call to action link. For example "View all news" which redirects users to the News Center page.
-   **Show more**: Displays a "Show more" button which reveals all the news articles when clicked.


</td></tr><tr><td>

Number of items per page

</td><td>

Maximum number of articles to display \(system maximum is 500 articles\)

</td></tr><tr><td>

Call to action: Text

</td><td>

Text for the call to action link. Select the **Call to action** layout to display this element.

</td></tr><tr><td>

Call to action: Page ID

</td><td>

The page where to redirect users who click on the call to action link

</td></tr><tr><td>

Default thumbnail image

</td><td>

Select an image to display when a news article doesn't have a thumbnail image

</td></tr><tr><td>

Empty state

</td><td>

Allows the widget to appear if there are no published news articles

</td></tr><tr><td>

Performance Indicator

</td><td>

Enables viewing of nested call insights for total load time in parent and child news feed widgets, allowing users to add and review detailed nested calls for featured news and event widgets.

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Configure employee communications widgets](../concept/employee-comms-widgets.md)

