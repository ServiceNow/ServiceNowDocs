---
title: Response time indicator
description: A response time indicator may appear at the bottom right of forms and in the list view for List v2.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Response time indicator

A response time indicator may appear at the bottom right of forms and in the list view for List v2.

This indicator provides the processing time, including the total time and the time for each step, for a completed transaction. In List v3, the administrator can add the glide.ui.list\_v3.client.timings.roles to allow specified roles to see the response time.

The following example shows the response time for retrieving a filtered v2 list in a demo instance.

![Response time](../image/ResponseTime2.png "Response time in v2 lists")

The response time text is:

```
Response time(ms): 985, Network: 22, server: 849, browser: 114
```

In this example, the transaction took the following amount of processing time.

-   985 milliseconds total time
-   22 milliseconds moving data across the network
-   849 milliseconds on the server
-   114 milliseconds in the browser, rendering the HTML and parsing and executing JavaScript

Use the expand option to see more details for the response time indicator.

![Response time indicator expanded](../image/ResponseTimeExpanded.png "Response time indicator expanded")

In List v3, the response time appears on the lower left for users whose role is specified in the system property.

![Response time in List v3](../../using-lists-v3/image/Listv3-response-time.png "Response time in v3 lists")

Response time appears on most pages. However, it does not appear for simple operations, such as paging through a set of records or changing the sort order of a list, or for the first transaction in a session.

To hide the response time in List v2 or forms, click the clock icon. Click the clock icon again to show the response time.

Point to the clock to view a tooltip with the response time.

To view a detailed breakdown of the browser processing time on forms, click **browser**.

![Details of response time](../image/ResponseTime1.png "Detailed response time information")

Administrators can disable the response time by setting the **glide.ui.response\_time** property to **false**.

**Parent Topic:**[User interface configuration](../../../administer/core-configuration/concept/p_NavigationAndUIConfiguration.md)

