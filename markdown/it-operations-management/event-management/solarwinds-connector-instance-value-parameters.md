---
title: Solarwinds connector instance value parameters
description: The following table displays the Solarwinds connector instance value parameters that you can fill in, as needed, when creating a Solarwinds connector instance.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Solarwinds connector instance value parameters

The following table displays the Solarwinds connector instance value parameters that you can fill in, as needed, when creating a Solarwinds connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

debug

</td><td>

Set to **true** to enable debug logs.

 Default value: false

</td></tr><tr><td>

max\_fetch\_interval\_in\_min

</td><td>

Number of minutes before the current time when the initial metric collection runs. For example, if the value is 180, the connector fetches metrics from the past 180 minutes.Default value: 180 minutes

</td></tr><tr><td>

logPayloadForDebug

</td><td>

Determines whether to print the raw log payload. Set to **true** only for debugging purposes, as printing the raw payload quickly fills up the MID Server logs.

 Default value: false

</td></tr><tr><td>

offset

</td><td>

Specifies the time offset in minutes for adjusting the fetch start time relative to the current time.Default: 0 minutes

</td></tr><tr><td>

Port

</td><td>

Port number for the Solarwinds server to connect to.Default value: 17774

</td></tr><tr><td>

protocol

</td><td>

Protocol to use when connecting to the Solarwinds server.Default value: https

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

