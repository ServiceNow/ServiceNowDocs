---
title: Self-Service performance
description: Use the Self-Service performance dashboard page to view self-service performance indicators of Now Assist experiences like Now Assist in Virtual Agent, Now AssistService Portal, and Now Assist context menu that are active on the instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-11-22"
reading_time_minutes: 3
keywords: [Now Assist, Gen AI, Generative AI, Virtual Agent, Self-Service Performance, deflection, indicators]
breadcrumb: [Using Now Assist Analytics, Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Self-Service performance

Use the Self-Service performance dashboard page to view self-service performance indicators of Now Assist experiences like Now Assist in Virtual Agent, Now AssistService Portal, and Now Assist context menu that are active on the instance.

The Self-Service performance dashboard page contains indicators that help you analyze the deflection performance of Now Assist self-service experiences like Now Assist in Virtual Agent and Service Portal. Use the date range and feature filters to view deflection and self-service performance indicators for a certain period and Now Assist experience. The filter selection applies to all visualizations on the page. The default date range is 30 days.

![Self-Service performance indicators](../image/naa-self-service-performance.png)

The indicators on the Self-Service performance dashboard page provide the following insights.

-   Deflection rate based on the number of queries resolved by a Now Assist self-service capability, for example, Now Assist in Virtual Agent.
-   Breakdown of percentage of user queries responded to by Now Assist self-service capabilities.
-   Now Assist self-service capability that contributed to the most number of successful conversations, that is, conversations with feedback as Resolved.

## Deflection performance indicators

-   **Total number of queries**

    This area of the dashboard shows the total number of user queries received by the selected Now Assist self-service capability. In a conversation, when the user selects other list items such as **Show next answer** and **Show more results**, the user input is considered as part of the same query. When Now Assist in Virtual Agent detects an intent switch, for example, if the user types a different query or selects **Start a new conversation**, it's counted as a new query.

    ![Total number of queries indicator](../image/naa-total-number-of-queries.png "Total number of queries indicator")

-   **Total number of query responses**

    This area of the dashboard shows the total number of responses where active Now Assist skills in the self-service capability presented content for the users to review. The Now Assist skills in Virtual Agent include Now Assist Q&amp;A Genius Results, Now Assist Multi-Turn Catalog Ordering, and Now Assist Topics. If no content is presented in the response, the query is marked as No Response Provided.

    ![Total number of query responses indicator](../image/naa-total-number-of-query-responses.png "Total number of query responses indicator")

-   **Query resolution status**

    This area of the dashboard shows the resolution status of user queries which is determined based on the feedback provided by users on the query response.

    -   Resolved: Indicates that the user found the response to be useful and effective or the user didn't provide any feedback.
    -   Not Resolved: Indicates that the user didn't find the response presented by the Now Assist self-service capability to be useful and indicated this response through a negative feedback.
    ![Query resolution status indicator](../image/naa-query-resolution-status.png "Query resolution status indicator")

-   **Deflection rate**

    This area of the dashboard shows the percentage of user queries resolved by the Now Assist self-service capability. The deflection percentage is calculated using the following formula: \(Number of resolved queries/Total number of queries\) x 100.

    ![Deflection rate indicator](../image/naa-deflection-rate.png "Deflection rate indicator")


## Self-service indicators

-   **Requestor initiated events**

    This area of the dashboard shows a breakdown of the queries handled by the selected Now Assist self-service capability. For example, when you select Now Assist in Virtual Agent in the Feature dropdown, the indicator shows the number and percentage of queries handled by Now Assist in Virtual Agent. The indicator helps you understand which self-service capability has effectively handled user queries.

    ![Requestor initiated events indicator](../image/naa-req-events.png "Requestor initiated events indicator")

-   **Successful conversations by capability**

    This area of the dashboard shows the Now Assist self-service capabilities by the number of successful conversations they contributed to. Successful conversations are determined based on the feedback provided by the user on the query response.

    ![Successful conversations handled by Now Assist capability indicator](../image/naa-successful-conversation-by-capability.png "Successful conversations by capability")


**Parent Topic:**[Using Now Assist Analytics](using-now-assist-analytics.md)

