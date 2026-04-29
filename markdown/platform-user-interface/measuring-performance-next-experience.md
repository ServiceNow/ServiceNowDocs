---
title: Measuring the performance of your instance in Next Experience
description: View the performance-based information, including the UI loading times, for any recently accessed Next Experience page by using the client interaction table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Measuring the performance of your instance in Next Experience

View the performance-based information, including the UI loading times, for any recently accessed Next Experience page by using the client interaction table.

## Key Benefits

-   Monitor your instance performance proactively and view this information for up to seven days.
-   Identify and investigate performance issues, such as slow UI load times.
-   View the server response times.

The following table lists the performance data that you can view in the client interaction table. You can find this table by navigating to **All** &gt; **System Logs** &gt; **Client Interactions**.

<table id="table_lzk_yvc_4bc"><thead><tr><th>

Header items

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time that the record was created.

</td></tr><tr><td>

Total UI Time

</td><td>

Time, in milliseconds, that the page takes to load.

</td></tr><tr><td>

Content Download Time

</td><td>

Time, in milliseconds, that the content takes to get from the server to the client.

</td></tr><tr><td>

UXF Screen Route

</td><td>

Route that is used to load the page for the given experience. For example, if you’re accessing the page from a list or form, Classic is displayed. If you’re accessing a workspace, the route that is defined in UI Builder is displayed.

</td></tr><tr><td>

Referrer

</td><td>

URL being accessed.

</td></tr><tr><td>

Application

</td><td>

Application that the URL belongs to.

</td></tr><tr><td>

Type

</td><td>

Interaction that is being measured. Type options include: -   PAGE\_LOAD: Indicates that the interaction was a full page load.
-   NAVIGATION: Indicates that the interaction was routed within a single page application.
-   IN-PAGE: Indicates the time that the interaction within the page has taken and is captured for limited interactions.

</td></tr><tr><td>

Interruption

</td><td>

Type of page load interruption and information about the type of interruption. If there was no interruption, the record displays none. The page load interruptions can impact the total UI time metric.

</td></tr><tr><td>

Name

</td><td>

Contextual information for in-page interactions.

</td></tr><tr><td>

Data

</td><td>

Contextual information for in-page interactions.

</td></tr></tbody>
</table>-   **[View the server response time](../task/view-server-response-time.md)**  
View the server response times that are associated with your Next Experience instance by using the client interaction table.

**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

