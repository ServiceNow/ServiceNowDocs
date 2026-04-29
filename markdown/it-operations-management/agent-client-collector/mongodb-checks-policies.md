---
title: MongoDB default checks and policies
description: Agent Client Collector provides the following policies for MongoDB health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# MongoDB default checks and policies

Agent Client Collector provides the following policies for MongoDB health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for both Windows and Linux.

<table id="table_y3r_2qd_2tb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

app.mongodb.check-mongodb-alive

</td><td>

Monitors whether the MongoDB server is alive and creating alerts for the MongoDB server health status.

</td><td>

`commonchecks check-mongodb-alive -H db_host -p db_port` Where:

 -   `db_host` = Host where server is running.
-   `db_port` = Port to connect to the MongoDB server.

 Usage example: `command: commonchecks check-mongodb-alive -H 10.***.***.*** -p 27017`

</td><td>

`commonchecks check-mongodb -p {{.labels.params_port}} -H {{.labels.params_host}}`

</td><td>

`Check mongodb Alive OK`: Indicates that the server is in good health.

</td></tr><tr><td>

Event

</td><td>

app.mongodb.check-mongodb-metrics

</td><td>

Creates alerts for any of the MongoDB metrics, based on the threshold limit. To trigger the alerts for any MongoDB server metric, pass the whole metric name in the parameter.

</td><td>

`commonchecks check-mongodb-metrics -H Hostname -p port -w warning -c critical -d database -m MetricName` Where:

 -   `Hostname` = Host where server is running.
-   `port` = Port to connect to the MongoDB server.
-   `warning` = Warning threshold value.
-   `critical` = Critical threshold value.
-   `database` = Database name.
-   `MetricName` = Specific metric to monitor.

 Usage example: `command: commonchecks check-mongodb-alive -H 10.***.***.*** -p 27017`

</td><td>

`commonchecks check-mongodb-metrics -c {{.labels.params_critical}} -d {{.labels.params_database}} -w {{.labels.params_warning}} -H {{.labels.params_host}} -p {{.labels.params_port}} -m {{.labels.params_metric}}`

</td><td>

`Check mongodb Metrics OK`: Indicates that the `mongodb.connection.current` value is within the acceptable threshold.

</td></tr></tbody>
</table><table id="table_mqy_xzd_2tb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.mongodb.metrics-mongodb

</td><td>

Returns metrics of the MongoDB server and all databases.Sample metrics:

 -   `mongodb.connections.totalCreated`: Incoming connections
-   `mongodb.locks.Database.acquireCount_IX`: Intent Exclusive lock mode
-   `mongodb.locks.Database.acquireCount_X`: Exclusive lock mode
-   `mongodb.locks.Database.acquireCount_IS`: Intent shared lock mode

</td><td>

`commonchecks check-mongodb` Where:

 -   `host` = Hostname where the MongoDB server is running.
-   `port` = Port to connect to the MongoDB server.
-   `database` = Database name.

</td><td>

`commonchecks metrics-mongodb -p {{.labels.params_port}} -H {{.labels.params_host}} -d {{.labels.params_database}}`

</td><td>

`<hostname>.mongodb.connections.totalCreated 20632 1639498004`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

