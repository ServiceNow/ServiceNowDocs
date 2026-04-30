---
title: PostgreSQL default checks and policies
description: Agent Client Collector provides the following default checks and policies for PostgreSQL health monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# PostgreSQL default checks and policies

Agent Client Collector provides the following default checks and policies for PostgreSQL health monitoring.

|Type|Check|Description|Command|
|----|-----|-----------|-------|
|Event|postgresql.check-alive|Triggers an alert on the status of the PostgreSQL database.|`commonchecks check-postgres-alive -d {{.labels.params_database}} -p {{.labels.params_port}} -H {{.labels.params_host}}`|
|Event|postgresql.check-connections|Triggers an alert on the total connection load on the PostgreSQL database, based on the configured threshold.|`commonchecks check-postgres-connections -d {{.labels.params_database}} -c {{.labels.params_critical}} -p {{.labels.params_port}} -H {{.labels.params_host}} -w {{.labels.params_warning}} -a {{.labels.params_use_percentage}}`|
|Metric|postgresql.metric-active-connections|Provides metrics on the total active connection on the PostgreSQL database.|`commonchecks metric-postgres-connections -p {{.labels.params_port}} -d {{.labels.params_database}} -H {{.labels.params_host}}`|
|Metric|postgresql.metric-dbsize|Provides metrics on the total size for each of the server's PostgreSQL databases.|`commonchecks metric-postgres-dbsize -d {{.labels.params_database}} -H {{.labels.params_host}} -p {{.labels.params_port}}`|
|Metric|postgresql.metric-locks|Provides metrics on the locks in the PostgreSQL database/tables.|`commonchecks metric-postgres-locks -p {{.labels.params_port}} -d {{.labels.params_database}} -H {{.labels.params_host}}`|
|Metric|postgresql.metric-relation-size|Provides metrics on the database table size on the server.|`commonchecks metric-postgres-relation-size -p {{.labels.params_port}} -l {{.labels.params_limit}} -H {{.labels.params_host}} -d {{.labels.params_database}}`|
|Metric|postgresql.metric-statsbgwriter|Provides metrics related to buffer allocations.|`commonchecks metric-postgres-statsbgwriter -p {{.labels.params_port}} -d {{.labels.params_database}} -H {{.labels.params_host}}`|
|Metric|postgresql.metric-statsdb|Provides metrics related to commits/ rollbacks/tuples transactions / deadlocks/query conflicts count.|`commonchecks metric-postgres-statsdb -d {{.labels.params_database}} -H {{.labels.params_host}} -p {{.labels.params_port}}`|
|Metric|postgresql.metric-statsio|Provides table based metrics related index reads/total hits to a table index.|`commonchecks metric-postgres-statsio -s {{.labels.params_scope}} -H {{.labels.params_host}} -p {{.labels.params_port}} -d {{.labels.params_database}}`|
|Metric|postgresql.metric-statstable|Provides metrics related to CRUD operations.|`commonchecks metric-postgres-statstable -d {{.labels.params_database}} -H {{.labels.params_host}} -s {{.labels.params_scope}} -p {{.labels.params_port}}`|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

