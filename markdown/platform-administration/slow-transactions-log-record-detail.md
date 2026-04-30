---
title: Slow transactions log record detail
description: As an administrator, you can use Slow Transactions logs to gain insight into how transactions are affecting platform performance. To aid in debugging, you can filter transaction log detail by application scope, limiting transactions to only those transactions originating in specific scopes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Stats Tools, System Diagnostics, Maintain and monitor, Administer]
---

# Slow transactions log record detail

As an administrator, you can use Slow Transactions logs to gain insight into how transactions are affecting platform performance. To aid in debugging, you can filter transaction log detail by application scope, limiting transactions to only those transactions originating in specific scopes.

|Field|Description|
|-----|-----------|
|Average execution time \(ms\)|Average duration to execute the transaction, in a single occurrence, in milliseconds.|
|Execution count|Number of similar occurrences that are aggregated.|
|Total execution time|Total sum of the execution times for the aggregated executions of the transaction.|
|Average client time \(ms\)|Average duration to execute the transaction on the client, in a single occurrence, in milliseconds.|
|Total client time \(ms\)|Total sum of the transaction execution times for the aggregated occurrences on the client, in milliseconds.|
|Origin application|Application scope the transaction originated in. Global appears if the transaction originated in the global scope.|
|Example type|Example transaction type executed.|
|Example processor|Example processor for an individual transaction.|

