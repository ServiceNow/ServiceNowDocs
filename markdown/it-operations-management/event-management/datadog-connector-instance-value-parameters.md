---
title: Datadog connector instance value parameters
description: The following table displays the Datadog connector instance value parameters that you can fill in, as needed, when creating a Datadog connector instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Datadog connector instance value parameters

The following table displays the Datadog connector instance value parameters that you can fill in, as needed, when creating a Datadog connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

application\_key

</td><td>

\(Mandatory\) Enter the Application Key generated from your Datadog account, used for authentication.

</td></tr><tr><td>

BaseApiPath

</td><td>

The specific API path for querying metrics. The default is `/api/v2/query/timeseries`.

</td></tr><tr><td>

debug

</td><td>

Set to true to enable detailed, high-level logging for this instance during troubleshooting.Default: false

</td></tr><tr><td>

hostApiPath

</td><td>

The specific API path for retrieving the list of hosts. The default is `/api/v1/hosts`.

</td></tr><tr><td>

hostBatchSize

</td><td>

The number of hosts to retrieve in a single API call. The default is 500, and any value above 1000 is automatically capped at 1000.

</td></tr><tr><td>

hostFilter

</td><td>

\(Optional\) A comma-separated list of regular expressions \(regex\) to filter for specific hosts to monitor. or example, ^prod-db-.\* is a regex pattern that means "match any host whose name starts with prod-db-".

 Example Use Case: To monitor only hosts starting with app-server- and the specific host critical-db-01, you would set the hostFilter to: ^app-server-.\*, ^critical-db-01$.

</td></tr><tr><td>

initialSyncInMins

</td><td>

For the first run of the instance, the number of minutes of historical data to retrieve.

 The default is 15, and any value above 120 is capped at 120.

</td></tr><tr><td>

logPayload

</td><td>

Set to true to log the full request and response bodies for deep debugging. Use with caution as it can generate very large logs.

</td></tr><tr><td>

metricBatchSize

</td><td>

The number of metrics to query in a single API call. The default is 50, and any value above 50 is automatically capped at 50.

</td></tr><tr><td>

port

</td><td>

Port number for the Datadog server to connect to.This is typically not needed when using https.

</td></tr><tr><td>

protocol

</td><td>

The protocol for the connection.Default: https

</td></tr></tbody>
</table>In the Connector Instance Metrics related list, specify which metrics to collect. To use all 23 out-of-the-box metrics, no action is needed.

To go back to the procedure page, see [Configure the Datadog metrics connector instance](../task/configure-datadog-connector.md).

**Parent Topic:**[Event Management reference](event-management-reference.md)

