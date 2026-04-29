---
title: Dynatrace connector instance value parameters
description: The following table displays the Dynatrace connector instance value parameters that you can fill in, as needed, when creating a Dynatrace connector instance.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Dynatrace connector instance value parameters

The following table displays the Dynatrace connector instance value parameters that you can fill in, as needed, when creating a Dynatrace connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BaseApiPath

</td><td>

Custom base path for Dynatrace API calls. If your Dynatrace instance uses a different path than the default `/api/v2/metrics`, enter the custom path to ensure successful collection of metrics.

</td></tr><tr><td>

debug

</td><td>

Set to **true** to enable debug logs.Default: false

</td></tr><tr><td>

initialSyncInMins

</td><td>

Number of minutes before the current time that the initial metric collection runs. For example, if the value is 15, the connector fetches metrics from the past 15 minutes.Default: 15

</td></tr><tr><td>

logPayload

</td><td>

Determines whether to print the raw log payload. Set to **true** only for debugging purposes, as printing the raw payload quickly fills up the MID Server logs.Default: false

</td></tr><tr><td>

maxMetricsPerQuery

</td><td>

Maximum number of metric ids to query per API call to Dynatrace. The value cannot exceed 32, the maximum limit allowed by Dynatrace.Default: 32

</td></tr><tr><td>

pageSize

</td><td>

Maximum number of records to return in an API response from Dynatrace.Default: 500

</td></tr><tr><td>

port

</td><td>

Port number for the Dynatrace server to connect to.empty

</td></tr><tr><td>

protocol

</td><td>

Protocol to use when connecting to the Dynatrace server.Default: https

</td></tr><tr><td>

throttleApiCalls

</td><td>

Determines whether throttling is enabled. When enabled \(**true**\), a limit is set on the number of API calls to Dynatrace per minute.Default: false

</td></tr><tr><td>

requestPerMinute

</td><td>

The limit on number of API calls to Dynatrace per minute. Relevant only when **throttleApiCalls** = **true**.Default: 1000

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

