---
title: Response time indicator icon
description: A response time indicator icon may appear at the bottom right of forms and in the list view in the classic environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Response time indicator icon

A response time indicator icon may appear at the bottom right of forms and in the list view in the classic environment.

Hovering over or selecting the icon \(\) provides the processing time, including the total time and the time for each step, for a completed transaction .

The following example shows detail provided when hovering over the icon.

![Response time](../image/ResponseTime2.png "Response time")

The response time text is:

```
Response time(ms): 1051, Network: 1, server: 844, browser: 206
```

In this example, the transaction took the following amount of processing time.

-   1051 milliseconds total time
-   1 milliseconds moving data across the network
-   844 milliseconds on the server
-   206 milliseconds in the browser, rendering the HTML and parsing and executing JavaScript

Select the icon to see more details for the response time indicator.

![Response time indicator expanded](../image/ResponseTimeExpanded.png "Response time indicator expanded")

Administrators can disable the response time by setting the **glide.ui.response\_time** property to **false**.

**Parent Topic:**[User interface configuration](../../../administer/core-configuration/concept/p_NavigationAndUIConfiguration.md)

