---
title: MSSQL default checks and policies
description: The Agent Client Collector provides the following default checks and policies for MSSQL Metrics monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# MSSQL default checks and policies

The Agent Client Collector provides the following default checks and policies for MSSQL Metrics monitoring.

<table id="table_rgw_psy_vrb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.metrics-mssql-query

</td><td>

Generic MSSQL query class which accepts a query and dumps metrics.

</td><td>

winchecks metrics-mssql-query \(options\)-d, --database DATABASE Database schema to connect to \(required\)

 -q ,--query The query to execute, should return a list metric name and value, for example SELECT METRIC\_NAME, VALUE FROM GV$SYSMETRIC

 -h, --host HOST Host name to connect to, defaults to localhost

 -r, --port PORT Port to connect to, defaults to 1433

 -s, --scheme SCHEME Metric naming scheme, text to prepend to .$parent.$child,

 **Usage Example**

 `.winchecks metrics-mssql-query -d master -H localhost -p 1437 -q "select name,size from sys.database_files"`

</td><td>

Custom metrics defined in the parameters, which also contain value and timestamp.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

