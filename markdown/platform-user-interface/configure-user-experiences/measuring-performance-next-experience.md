---
title: Instance performance in Next Experience
description: View the performance-based information, including the UI loading times, for any recently accessed Next Experience page by using the client interaction table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/measuring-performance-next-experience.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Instance performance in Next Experience

View the performance-based information, including the UI loading times, for any recently accessed Next Experience page by using the client interaction table.

## Key benefits

-   Monitor your instance performance and view this information for up to seven days.
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

Date and time that the interaction was recorded.

</td></tr><tr><td>

Total UI Time

</td><td>

Total time, in milliseconds, from when a user initiates an interaction, such as loading or navigating, until the UI is idle. Includes rendering and network request time, and may be affected by user interruptions.

</td></tr><tr><td>

Content Download Time

</td><td>

Total time, in milliseconds, spent downloading resources from the server during the interaction.

</td></tr><tr><td>

UXF Screen Route

</td><td>

Route that is used to load the page for the given experience. For example, if the page is accessed from a list or form, Classic is displayed. For a workspace, the route defined in UI Builder is displayed.

</td></tr><tr><td>

Referrer

</td><td>

URL that initiated the interaction.

</td></tr><tr><td>

Application

</td><td>

Application associated with the accessed URL.

</td></tr><tr><td>

Type

</td><td>

Interaction that is being measured. Type options include: -   `PAGE_LOAD`: A full page load.
-   `NAVIGATION`: Routing within a single page application.
-   `IN-PAGE`: Time taken for interactions within the page, captured for limited interaction types.

</td></tr><tr><td>

Interruption

</td><td>

Type of page load interruption and information about the type of interruption. If there was no interruption, the record displays **none**. The page load interruptions can impact the total UI time metric.

</td></tr><tr><td>

Name

</td><td>

Contextual label for in-page interactions.

</td></tr><tr><td>

Data

</td><td>

Additional contextual details for in-page interactions.

</td></tr></tbody>
</table>## UI timing metrics

-   **total\_ui\_time**: includes network request time and rendering time.
-   **fci\_time** \(First Component Interactable\): time when the user first interacts with the UI.
-   **ui\_time\_before\_load** and **ui\_time\_after\_load**: time before and after the application shell finishes loading. These values are not always populated.

## Network and download metrics

-   **network\_latency**: approximate network round-trip time using a cached static resource. Useful for comparing performance across regions.
-   **content\_download\_time**: total time spent downloading resources during the interaction.
-   **client\_cache\_hit\_rate**: percentage of requests served from the browser cache.

## Server and transaction metrics

-   **total\_response\_time**: total response time across all related transactions.
-   **total\_sql\_time** and **total\_sql\_count**: total time and number of SQL operations.
-   **total\_business\_rule\_time** and **count**: time and count of business rule execution.
-   **total\_txp\_time**: time spent actively processing transactions, excluding wait times.

## UX routing details

-   **ux\_screen\_route**: the route used to load the screen in Next Experience.
-   **ux\_screen\_fields** and **ux\_screen\_params**: required and optional parameters used to load the screen.

## Additional data

-   **linked\_txc\_metrics**: JSON payload containing detailed client-side transaction metrics.
-   **page\_variant\_sys\_id**: identifies the specific screen variant displayed to the user.

-   **[View the server response time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/view-server-response-time.md)**  
View the server response times that are associated with your Next Experience instance by using the client interaction table.

**Parent Topic:**[Configuring the Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/next-experience-ui-admin.md)

