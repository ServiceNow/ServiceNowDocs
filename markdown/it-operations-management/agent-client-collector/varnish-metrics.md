---
title: Varnish metrics
description: The following table lists the metrics that are gathered as output from Varnish checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Varnish metrics

The following table lists the metrics that are gathered as output from Varnish checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|MAIN\_sess\_conn \(featured metric\)| |count|Cumulative number of accepted client connections by Varnish Cache.|
|MAIN\_sess\_drop \(featured metric\)| |count|Number of connections dropped due to a full queue.|
|MAIN\_client\_req \(featured metric\)| |count|Cumulative number of received client requests. Increments after a request is received, but before Varnish responds.|
|MAIN\_cache\_hit| |count|Cumulative number of times a file was served from Varnish’s cache.|
|MAIN\_cache\_hitpass| |count|Cumulative number of hits for a “pass” file.|
|MAIN\_cache\_miss| |count|Cumulative number of times a file was requested but was not in the cache, and was therefore requested from the backend.|
|MAIN\_backend\_conn| |count|Cumulative number of successful TCP connections to the backend.|
|MAIN\_backend\_unhealthy \(featured metric\)| |count|Cumulative number of backend connections which were not attempted because the backend has been marked as unhealthy.|
|MAIN\_backend\_busy| |count|Cumulative number of times the maximum amount of connections to the backend has been reached.|
|MAIN\_backend\_fail \(featured metric\)| |count|Cumulative number of failed connections to the backend.|
|MAIN\_backend\_reuse \(featured metric\)| |count|Cumulative number of connections that were reused from the keep-alive pool.|
|MAIN\_backend\_recycle| |count|Cumulative number of current backend connections which were put back to a pool of keep-alive connections and have not yet been used.|
|MAIN\_threads \(featured metric\)| |count|Number of threads in all pools.|
|MAIN\_threads\_limited| |count|Number of times a thread needed to be created but couldn't because varnishd maxed out its configured capacity for new threads.|
|MAIN\_threads\_created| |count|Number of times a thread has been created.|
|MAIN\_threads\_failed \(featured metric\)| |count|Number of times that Varnish unsuccessfully tried to create a thread.|
|MAIN\_thread\_queue\_len| |count|Current queue length: number of requests waiting on worker thread to become available.|
|MAIN\_sess\_queued| |count|Number of times Varnish has been out of threads and had to queue up a request.|
|MAIN\_n\_expired \(featured metric\)| |count|Cumulative number of expired objects for example due to TTL.|
|MAIN\_n\_lru\_nuked \(featured metric\)| |count|Least Recently Used Nuked Objects: Cumulative number of cached objects that Varnish has evicted from the cache because of a lack of space.|
|MAIN\_backend\_req \(featured metric\)| |count|Number of requests to the backend.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

