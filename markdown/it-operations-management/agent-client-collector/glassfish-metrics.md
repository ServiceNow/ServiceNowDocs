---
title: GlassFish metrics
description: The following table lists the metrics that are gathered as output from GlassFish checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# GlassFish metrics

The following table lists the metrics that are gathered as output from GlassFish checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfish.applications.\{Deployed Application\}.TotalServletsLoaded|Deployed Application|count|Total number of Servlets loaded so far.|
|glassfish.applications.\{Deployed Application\}.ServletProcessingTimes|Deployed Application|ms|Cumulative Servlet processing times.|
|glassfish.applications.\{Deployed Application\}.ActiveServletsLoaded|Deployed Application|count|Number of Servlets loaded.|
|glassfish.applications.\{Deployed Application\}.ExpiredSessionsTotal \(featured metric\)|Deployed Application|count|Total number of sessions expired so far.|
|glassfish.applications.\{Deployed Application\}.PassivatedSessionsTotal|Deployed Application|count|Total number of sessions passivated so far.|
|glassfish.applications.\{Deployed Application\}.ActivatedSessionsTotal|Deployed Application|count|Total number of sessions activatedso far.|
|glassfish.applications.\{Deployed Application\}.SessionsTotal|Deployed Application|count|Total number of sessions created so far.|
|glassfish.applications.\{Deployed Application\}.RejectedSessionsTotal \(featured metric\)|Deployed Application|count|Total number of sessions rejected so far.|
|glassfish.applications.\{Deployed Application\}.PersistedSessionsTotal|Deployed Application|count|Total number of sessions persisted so far.|
|glassfish.applications.\{Deployed Application\}.ActiveSessions \(featured metric\)|Deployed Application|count|Number of active sessions.|
|glassfish.applications.\{Deployed Application\}.RequestCount|Deployed Application|count|Cumulative number of requests processed so far|
|glassfish.applications.\{Deployed Application\}.MaxTime \(featured metric\)|Deployed Application|ms|Longest response time for a request; not a cumulative value, but the largest response time from among the response times.|
|glassfish.applications.\{Deployed Application\}.ErrorCount \(featured metric\)|Deployed Application|count|Cumulative value of the error count, with error count representing the number of cases where the response code was greater than or equal to 400.|
|glassfish.applications.\{Deployed Application\}.ProcessingTime|Deployed Application|ms|Average request processing time.|
|glassfish.applications.\{Deployed Application\}.TotalJspCount|Deployed Application|count|Total number of JSP pages loaded so far.|
|glassfish.applications.\{Deployed Application\}.JspCount|Deployed Application|count|Number of active JSP pages.|
|glassfish.applications.\{Deployed Application\}.JspErrorCount \(featured metric\)|Deployed Application|count|Total number of errors triggered by JSP page invocations.|
|glassfish.applications.\{Deployed Application\}.JspReloadedCount|Deployed Application|count|Total number of reloaded JSP pages.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfish.deployment.lifecycle.ActiveApplicationsDeployed \(featured metric\)| |count|Total number of applications deployed so far.|
|glassfish.deployment.lifecycle.TotalApplicationsDeployed \(featured metric\)| |count|Number of applications deployed.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfish.http-service.server.request.Count200| |count|Number of responses with a status code equal to 200.|
|glassfish.http-service.server.request.Count2xx| |count|Number of responses with a status code in the 2xx range.|
|glassfish.http-service.server.request.Count302| |count|Number of responses with a status code equal to 302.|
|glassfish.http-service.server.request.Count304| |count|Number of responses with a status code equal to 304.|
|glassfish.http-service.server.request.Count3xx| |count|Number of responses with a status code equal in the 3xx range.|
|glassfish.http-service.server.request.Count400| |count|Number of responses with a status code equal to 400.|
|glassfish.http-service.server.request.Count401| |count|Number of responses with a status code equal to 401.|
|glassfish.http-service.server.request.Count403| |count|Number of responses with a status code equal to 403.|
|glassfish.http-service.server.request.Count404| |count|Number of responses with a status code equal to 404.|
|glassfish.http-service.server.request.Count4xx| |count|Number of responses with a status code equal in the 4xx range.|
|glassfish.http-service.server.request.Count503| |count|Number of responses with a status code equal to 503.|
|glassfish.http-service.server.request.Count5xx| |count|Number of responses with a status code equal in the 5xx range.|
|glassfish.http-service.server.request.MaxTime| |ms|Longest response time for a request; not a cumulative value, but the largest response time from among the response times.|
|glassfish.http-service.server.request.CountBytesReceived \(featured metric\)| |count|Number of bytes received.|
|glassfish.http-service.server.request.CountBytesTransmitted \(featured metric\)| |count|Number of bytes transmitted.|
|glassfish.http-service.server.request.RequestCount \(featured metric\)| |count|Cumulative number of requests processed so far.|
|glassfish.http-service.server.request.CountOpenConnections| |count|Number of open connections.|
|glassfish.http-service.server.request.ProcessingTime \(featured metric\)| |ms|Average request processing time.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfish.jvm.garbage-collectors.Scavenge.CollectionCount| |count|Total number of collections that have occurred.|
|glassfish.jvm.garbage-collectors.Scavenge.CollectionTime| |ms|Approximate accumulated collection elapsed time in milliseconds.|
|glassfish.jvm.garbage-collectors.MarkSweepCompact.CollectionCount| |count|Total number of collections that have occurred.|
|glassfish.jvm.garbage-collectors.MarkSweepCompact.CollectionTime| |ms|Approximate accumulated collection elapsed time in milliseconds.|
|glassfish.jvm.memory.CommittedHeapSize| |bytes|Amount of memory in bytes that is committed for the Java virtual machine to use.|
|glassfish.jvm.memory.CommittedNonHeapSize| |bytes|Amount of memory in bytes that is committed for the Java virtual machine to use.|
|glassfish.jvm.memory.InitHeapSize| |bytes|Amount of memory in bytes that the Java virtual machine initially requests from the operating system for memory management.|
|glassfish.jvm.memory.InitNonHeapSize| |bytes|Amount of memory in bytes that the Java virtual machine initially requests from the operating system for memory management.|
|glassfish.jvm.memory.MaxHeapSize \(featured metric\)| |bytes|Maximum amount of memory in bytes that can be used for memory management.|
|glassfish.jvm.memory.MaxNonHeapSize| |bytes|Maximum amount of memory in bytes that can be used for memory management.|
|glassfish.jvm.memory.ObjectPendingFinalizationCount| |count|Approximate number of objects for which finalization is pending.|
|glassfish.jvm.memory.UsedHeapSize| |bytes|Amount of used memory in bytes.|
|glassfish.jvm.memory.UsedNonHeapSize| |bytes|Amount of used memory in bytes.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfish.transaction-service.ActiveCount \(featured metric\)| |count|Provides the number of transactions that are currently active.|
|glassfish.transaction-service.CommittedCount \(featured metric\)| |count|Provides the number of transactions that have been committed.|
|glassfish.transaction-service.RolledBackCount \(featured metric\)| |count|Provides the number of transactions that have been rolled back.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|glassfis.resources.\{PoolName\}.AverageConnWaitTime|PoolName|ms|Average wait-time-duration per successful connection request.|
|glassfis.resources.\{PoolName\}.ConnRequestWaitTime|PoolName|ms|The longest and shortest wait times of connection requests. The current value indicates the wait time of the last request that was serviced by the pool.|
|glassfis.resources.\{PoolName\}.NumConnAcquired|PoolName|count|Number of logical connections acquired from the pool.|
|glassfis.resources.\{PoolName\}.NumConnCreated|PoolName|count|The number of physical connections that were created since the last reset.|
|glassfis.resources.\{PoolName\}.NumConnDestroyed|PoolName|count|Number of physical connections that were destroyed since the last reset.|
|glassfis.resources.\{PoolName\}.NumConnfailedValidation|PoolName|count|The total number of connections in the connection pool that failed validation from the start time until the last sample time.|
|glassfis.resources.\{PoolName\}.NumConnFree|PoolName|count|The total number of free connections in the pool as of the last sampling.|
|glassfis.resources.\{PoolName\}.NumConnnotSuccessfullyMatched|PoolName|count|Number of connections rejected during matching.|
|glassfis.resources.\{PoolName\}.NumConnReleased|PoolName|count|Number of logical connections released to the pool.|
|glassfis.resources.\{PoolName\}.NumConnSuccessfullyMatched|PoolName|count|Number of connections successfully matched.|
|glassfis.resources.\{PoolName\}.NumConnTimedOut|PoolName|count|The total number of connections in the pool that timed out between the start time and the last sample time.|
|glassfis.resources.\{PoolName\}.NumConnUsed|PoolName|count|Provides connection usage statistics. The total number of connections that are currently being used, as well as information about the maximum number of connections that were used \(the high water mark\).|
|glassfis.resources.\{PoolName\}.NumPotentialConnLeak \(featured metric\)|PoolName|count|Number of potential connection leaks.|
|glassfis.resources.\{PoolName\}.WaitQueueLength \(featured metric\)|PoolName|count|Number of connection requests in the queue waiting to be serviced.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

