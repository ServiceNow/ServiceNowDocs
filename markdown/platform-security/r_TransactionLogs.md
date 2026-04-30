---
title: Transaction logs
description: The transaction log records browser activity for an instance. To aid in debugging of system issues, you can filter transaction logs by application scope, limiting transactions that appear to only those transactions originating in specific scopes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-26"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Transaction logs

The transaction log records browser activity for an instance. To aid in debugging of system issues, you can filter transaction logs by application scope, limiting transactions that appear to only those transactions originating in specific scopes.

**Note:** Background and scheduler transactions are logged only when their execution time exceeds 1000ms. For a complete list of logged transactions, see [KB0778299](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0778299).

Access the transaction logs by navigating to **All** &gt; **System Logs** &gt; **Transactions**. The transaction log provides the following information for all activities.

|Field|Description|
|-----|-----------|
|Created|Date and time of the application action for the locale of the machine running the instance.|
|Type|Type of recorded transaction.|
|Created by|User who created this activity.|
|Origin application|Application scope the transaction originated in. Global appears if the transaction originated in the global scope.|
|Response time|Round trip response time for the application request, in milliseconds.|
|Network time|Latency time of the network response after the application request is made, in milliseconds.|
|Output length|Size of the output string sent by the instance to the application, in bytes.|
|SQL count|Number of SQL server commands executed for this activity.|
|Business rule count|Number of business rules executed for this activity.|
|Business rule time|Elapsed time for the execution of the business rules for this activity.|
|URL|Application or module connected to by the client application.|
|System ID|System generated identifier of the client instance making the request. This ID is used for cluster environments in which several instances \(nodes\) communicate with the database.|
|IP address|IP address of the client making the request.|
|GZipped|Indication of whether a compressed Web page was requested by the application.|
|Protocol|HTTP protocol used by the application for this instance.|

