---
title: HAProxy metrics
description: The following table lists the metrics that are gathered as output from HAProxy checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# HAProxy metrics

The following table lists the metrics that are gathered as output from HAProxy checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|haproxy.frontend.session\_current \(featured metric\)| |count|The current number of sessions being used to issue requests.|
|haproxy.frontend.session\_total \(featured metric\)| |count|Total number of sessions|
|haproxy.frontend.bytes\_in \(featured metric\)| |count|The total number of bytes recieved by the server in the last second from the client.|
|haproxy.frontend.bytes\_out \(featured metric\)| |count|The total number of bytes sent by the server in the last second.|
|haproxy.frontend.connection\_errors \(featured metric\)| |count|The number of requests that encountered an error trying to connect to a server.|
|haproxy.frontend.warning\_retries| |count|The number of times a connection to a server was retried.|
|haproxy.frontend.warning\_redispatched| |count|The number of times a request was redispatched to another server.|
|haproxy.frontend.response\_1xx| |count|HAProxy exposes the number of responses by HTTP status code - 1xx|
|haproxy.frontend.response\_2xx| |count|HAProxy exposes the number of responses by HTTP status code - 2xx|
|haproxy.frontend.response\_3xx| |count|HAProxy exposes the number of responses by HTTP status code - 3xx|
|haproxy.frontend.response\_4xx| |count|HAProxy exposes the number of responses by HTTP status code - 4xx|
|haproxy.frontend.response\_5xx| |count|HAProxy exposes the number of responses by HTTP status code - 5xx|
|haproxy.frontend.response\_other| |count|HAProxy exposes the number of responses by non-HTTP application|
|haproxy.frontend.queue\_time| |count|The average queue time over the last 1024 requests.|
|haproxy.frontend.connect\_time| |count|The average connect time over the last 1024 requests.|
|haproxy.frontend.response\_time \(featured metric\)| |count|The response time to the client|
|haproxy.frontend.average\_time \(featured metric\)| |count|The average time taken for the sessions.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|haproxy.backend.session\_current \(featured metric\)| |count|The current number of sessions being used to issue requests.|
|haproxy.backend.session\_total \(featured metric\)| |count|Total number of sessions|
|haproxy.backend.bytes\_in \(featured metric\)| |count|The total number of bytes recieved by the server in the last second from the client.|
|haproxy.backend.bytes\_out \(featured metric\)| |count|The total number of bytes sent by the server in the last second.|
|haproxy.backend.connection\_errors \(featured metric\)| |count|The number of requests that encountered an error trying to connect to a server.|
|haproxy.backend.warning\_retries| |count|The number of times a connection to a server was retried.|
|haproxy.backend.warning\_redispatched| |count|The number of times a request was redispatched to another server.|
|haproxy.backend.response\_1xx| |count|HAProxy exposes the number of responses by HTTP status code - 1xx|
|haproxy.backend.response\_2xx| |count|HAProxy exposes the number of responses by HTTP status code - 2xx|
|haproxy.backend.response\_3xx| |count|HAProxy exposes the number of responses by HTTP status code - 3xx|
|haproxy.backend.response\_4xx| |count|HAProxy exposes the number of responses by HTTP status code - 4xx|
|haproxy.backend.response\_5xx| |count|HAProxy exposes the number of responses by HTTP status code - 5xx|
|haproxy.backend.response\_other| |count|HAProxy exposes the number of responses by non-HTTP application|
|haproxy.backend.queue\_time| |count|The average queue time over the last 1024 requests.|
|haproxy.backend.connect\_time| |count|The average connect time over the last 1024 requests.|
|haproxy.backend.response\_time \(featured metric\)| |count|The response time to the client|
|haproxy.backend.average\_time \(featured metric\)| |count|The average time taken for the sessions.|
|haproxy.backend.num\_up| |count| |

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

