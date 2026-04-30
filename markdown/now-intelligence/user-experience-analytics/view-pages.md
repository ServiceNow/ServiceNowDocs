---
title: Web pages
description: The Pages module for UI Analysis on the User Experience Analytics dashboard shows analytics specific to pages on the web-based UI. View user action, performance, and navigation details for each web page.See user actions, performance and navigation analytics for each page.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [UI analysis, Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Web pages

The Pages module for UI Analysis on the User Experience Analytics dashboard shows analytics specific to pages on the web-based UI. View user action, performance, and navigation details for each web page.

![Pages module.](../image/pages-module.png)

<table id="table_zxj_x2s_gwb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page name

</td><td>

Name of the selected page. To change the name of a page, click the edit icon ![](../image/edit-icon.png).

</td></tr><tr><td>

Sessions

</td><td>

Shows the number of sessions contained on the specified page. If a page was opened more than once during a session, it's only counted once.

</td></tr><tr><td>

Average Duration

</td><td>

Shows the average time spent on the page. Also, the percentage of time spent on the page relative to the average time spent throughout the app during sessions.

</td></tr><tr><td>

Avg Page Load Time

</td><td>

Shows the average time it takes to load the page, based on the number of times the page is viewed.

</td></tr><tr><td>

**Performance graph**

</td><td>

Displays the daily performance trend of selected trace types in a graphical representation. From the menu arrow, select one of the following trace types: Client Time, Network Time, Server Time, and Page Load Time.

 When the necessary data is available, the performance graph for the selected trace type displays trend lines for the full page load and the client page load.

-   Full Page Load – Time needed to render the page by re-downloading the whole web document.
-   Client Page Load - Time needed to render the page by only downloading the net new content. For example, client-side routing.

 ![Performance graph.](../image/performance-graph.png)

</td></tr><tr><td>

Page Load Time

</td><td>

Overall time to deliver the page by subtracting the time the user requests the page from the time the page is fully rendered in the browser.

</td></tr><tr><td>

Server Time

</td><td>

Time the server takes to process the transaction.

</td></tr><tr><td>

Network Time

</td><td>

Time the network takes to process the request. Calculated by subtracting the time of the user's request, from the time the page starts loading in the browser, and then subtracting the server processing time.

</td></tr><tr><td>

Client Time

</td><td>

Time the browser takes to deliver the page by subtracting the time the page is fully rendered from the time the page starts loading in the browser.

</td></tr><tr><td colspan="2">

**Navigation**

</td></tr><tr><td>

Previous page

</td><td>

Shows the top pages from which users arrived to the selected page. Also, the percentage of sessions arriving from each page relative to the total number of navigations to it. Rare actions may be omitted.

</td></tr><tr><td>

Next page

</td><td>

Shows the top pages to which users arrived from the selected page. Also, the percentage of sessions navigating to each page relative to the total number of navigations from it.

</td></tr></tbody>
</table>## View web page analytics

See user actions, performance and navigation analytics for each page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **UI Analysis** &gt; **Pages**.

2.  Scroll the pages list, or enter text in the **Search** field to locate and select a page.


