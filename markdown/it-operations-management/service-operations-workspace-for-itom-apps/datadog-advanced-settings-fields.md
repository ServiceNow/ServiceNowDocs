---
title: Datadog advanced settings fields
description: Populate the Datadog advanced settings fields to define API paths, batching limits, host filters, sync duration, connection details, and debugging options. These values control how the pull connector retrieves and processes metrics and host data from Datadog, ensuring the connector runs with the desired scope and behavior.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Datadog advanced settings fields

Populate the Datadog advanced settings fields to define API paths, batching limits, host filters, sync duration, connection details, and debugging options. These values control how the pull connector retrieves and processes metrics and host data from Datadog, ensuring the connector runs with the desired scope and behavior.

<table id="table_cwg_vzv_mbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base API path

</td><td>

The specific API path for querying metrics.The default is `/api/v2/query/timeseries`.

</td></tr><tr><td>

Host API Path

</td><td>

The specific API path for retrieving the list of hosts.The default is `/api/v1/hosts`.

</td></tr><tr><td>

Host batch size

</td><td>

The number of hosts to retrieve in a single API call.The default is 500, and any value above 1000 is automatically capped at 1000.

</td></tr><tr><td>

Host filter

</td><td>

\(Optional\) A comma-separated list of regular expressions \(regex\) to filter for specific hosts to monitor. or example, ^prod-db-.\* is a regex pattern that means "match any host whose name starts with prod-db-".Example Use Case: To monitor only hosts starting with app-server- and the specific host critical-db-01, you would set the hostFilter to: ^app-server-.\*, ^critical-db-01$.

</td></tr><tr><td>

Initial sync in mins

</td><td>

Time, in minutes, that the system takes to complete the first synchronization of data with the Datadog Metrics API.For example, if the value is 15, the connector fetches metrics from the past 15 minutes. If the value is above 120, it is capped to 120.

Default: 15

</td></tr><tr><td>

Metric batch size

</td><td>

The number of metrics to query in a single API call.The default is 50, and any value above 50 is automatically capped at 50.

</td></tr><tr><td>

Port

</td><td>

Port number for the Datadog server to connect to.This is typically not needed when using https.

</td></tr><tr><td>

Protocol

</td><td>

The protocol for the connection.Default: https

</td></tr><tr><td>

Debugging

</td><td>

-   Debug: Provides detailed logs for troubleshooting.
-   Log payload: Displays raw log data. Use only for debugging, as it can quickly fill the MID Server logs.

</td></tr></tbody>
</table>To return to the procedure, see [Configure Datadog metric pull connector](../task/configure-datadog-metric-pull-connector.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

