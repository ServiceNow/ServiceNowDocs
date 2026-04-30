---
title: API analytics properties
description: Certain properties control the behavior of API analytics.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Analyze REST and SOAP API usage, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# API analytics properties

Certain properties control the behavior of API analytics.

<table id="table_w3z_qgz_qw"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.api.stats.enabled

</td><td>

When true, enables the collection of API usage statistics. When false, no analytics are collected even for domains on the inclusion list.-   Type: true \| false
-   Default value: true
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr><tr><td>

com.glide.api.stats.max\_bytes\_nursery\_size

</td><td>

The maximum amount of memory, in bytes, used to store transaction data before it is written to the log. Transaction data is written to the log regularly based on the value of **com.glide.api.stats.persist\_interval**.

 If a large volume of transactions exceeds this memory limit before the log is written, some transactions may not be logged. The event api.stats.cache.size.reached is fired if this limit is reached.

This property value must be between 1 and 3 megabytes.-   Type: integer
-   Default value: 3145728
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr><tr><td>

com.glide.api.stats.persist\_interval

</td><td>

The frequency, in seconds, for writing transactions stored in memory to the log. This property value must be between 30 and 120 seconds.-   Type: integer
-   Default value: 60
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr><tr><td>

com.glide.api.stats.daily\_ limit

</td><td>

The daily limit of requestor stats records per instance node. As soon is the value is reached, data is no longer aggregated and stored for that day. The event api.stats.requestor.daily.limit.reached is fired if this limit is reached.-   Type: integer
-   Default value: 20000
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.api.stats.debug

</td><td>

When true, enables debug logging for API stats.-   Type: true \| false
-   Default value: false
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Analyze REST and SOAP API usage](../concept/c_APIAnalytics.md)

