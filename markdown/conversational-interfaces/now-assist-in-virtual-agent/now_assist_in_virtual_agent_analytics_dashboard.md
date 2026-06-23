---
title: Analyzing Now Assist in Virtual Agent
description: Use the Now Assist in Virtual Agent Analytics dashboard to monitor the performance of Now Assist in Virtual Agent as a self-service deflection mechanism.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/conversational-interfaces/now-assist-in-virtual-agent/now\_assist\_in\_virtual\_agent\_analytics\_dashboard.html
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Now Assist in Virtual Agent, Conversational Interfaces]
---

# Analyzing Now Assist in Virtual Agent

Use the Now Assist in Virtual Agent Analytics dashboard to monitor the performance of Now Assist in Virtual Agent as a self-service deflection mechanism.

## Now Assist in Virtual Agent Analytics

The Now Assist in Virtual Agent Analytics dashboard provides indicators that you can use to track the effectiveness of Now Assist in Virtual Agent as a self-service deflection tool. The dashboard provides insights into the conversations so that you can see how well Now Assist in Virtual Agent understood and resolved user queries. The dashboard indicators, for example, reveal the following:

-   The number of user queries that Now Assist in Virtual Agent responded to from the total number of queries
-   Resolution status of user queries based on the feedback provided by the user
-   The deflection rate in a given period

The dashboard is built on the Platform Analytics experience. See [Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/now-intelligence/par-workspace.md) for more information.

To access the dashboard, navigate to **All** &gt; **Conversational Interfaces** &gt; **Analytics** &gt; **Now Assist in Virtual Agent**. You must have Virtual Agent Admin \[virtual\_Agent\_admin\] or Admin \[admin\] roles to access the dashboard.

\[Omitted image "navaa-dashboard.png"\] Alt text: Now Assist in the Virtual Agent Analytics dashboard.

## Dashboard indicators

-   **Total Number of Queries**

    This area of the dashboard shows the total number of user queries received by Now Assist in Virtual Agent. In a conversation, when the user selects other list items such as **Show next answer** and **Show more results**, the user input is considered as part of the same query. When Now Assist in Virtual Agent detects an intent switch, for example, if the user types a different query or selects **Start a new conversation**, it's counted as a new query.

    \[Omitted image "navaa-total-number-of-queries.png"\] Alt text: Total number of queries indicator.

-   **Total Number of Query Responses**

    This area of the dashboard shows the total number of responses where active Now Assist skills in Virtual Agent presented content for the users to review. The Now Assist skills in Virtual Agent include Now Assist Q&amp;A Genius Results, Now Assist Multi-Turn Catalog Ordering, and Now Assist Topics. If no content is presented in the response, the query is marked as No Response Provided.

    \[Omitted image "navaa-total-number-of-query-responses.png"\] Alt text: Total number of query responses indicator.

-   **Query Resolution Status**

    This area of the dashboard shows the resolution status of user queries that is determined based on the feedback provided by users on the query response.

    -   Resolved: Indicates that the user found the response to be useful and effective or the user didn't provide any feedback.
    -   Not Resolved: Indicates that the user didn't find the response presented by Now Assist in Virtual Agent to be useful and indicated this response through negative feedback.
    -   No Response Provided: Indicates that no response was presented to the user query.
    \[Omitted image "navaa-query-resolution-status.png"\] Alt text: Query resolution status indicator.

-   **Deflection Rate**

    This area of the dashboard shows the percentage of user queries resolved by Now Assist in Virtual Agent. The deflection percentage is calculated using the following formula: \(Number of resolved queries/Total number of query responses\) x 100.

    \[Omitted image "navaa-deflection-rate.png"\] Alt text: Deflection rate indicator.


