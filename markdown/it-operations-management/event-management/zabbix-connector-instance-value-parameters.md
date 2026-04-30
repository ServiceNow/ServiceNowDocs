---
title: Zabbix connector instance value parameters
description: The following table displays the Zabbix connector instance value parameters that you can fill in, as needed, when creating a Zabbix connector instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Zabbix connector instance value parameters

The following table displays the Zabbix connector instance value parameters that you can fill in, as needed, when creating a Zabbix connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_endpoint\_suffix

</td><td>

Set this value based on your Zabbix server web interface installation: [https://www.zabbix.com/documentation/current/en/manual/installation/frontend\#welcome-screen](https://www.zabbix.com/documentation/current/en/manual/installation/frontend#welcome-screen)

 Default value: /zabbix/api\_jsonrpc.php \[For Apache Server\]

</td></tr><tr><td>

debug

</td><td>

Set to **true** to enable debug logs.

 Default value: false

</td></tr><tr><td>

enable\_batch\_processing

</td><td>

If batch processing is enabled, metrics details are fetched in batch with 1000 \(can be altered by setting appropriate value to - 'max\_hosts\_per\_batch' parameter\) hosts per batch.Default value: false

</td></tr><tr><td>

groupids

</td><td>

Provide the host group IDs. These IDs will be used to fetch metrics from the hosts attached to the specified groups. This applies only if `enable_batch_processing` is set to true.

</td></tr><tr><td>

logPayloadForDebug

</td><td>

Determines whether to print the raw log payload. Set to **true** only for debugging purposes, as printing the raw payload quickly fills up the MID Server logs.

 Default value: false

</td></tr><tr><td>

max\_fetch\_interval\_min

</td><td>

Configured from the 'max\_fetch\_interval\_min' parameter: If the time exceeds 'max\_fetch\_interval\_min', fetching starts from 'max\_fetch\_interval\_min' before the current time; for an INITIAL run without 'lastMetricSignature', the time is set to 'max\_fetch\_interval\_min' before the current time.Default value: 180 minutes

</td></tr><tr><td>

max\_hosts\_per\_batch

</td><td>

If batch processing is enabled, metrics details are fetched in batch with 1000 \(can be altered by setting appropriate value to - 'max\_hosts\_per\_batch' parameter\) hosts per batch.Default value: 1000

</td></tr><tr><td>

offset\_min

</td><td>

Specifies the time offset in minutes for adjusting the fetch start time relative to the current time.Default: 5 minutes

</td></tr><tr><td>

port

</td><td>

Port number for the Zabbix server to connect to.Default value: empty

</td></tr><tr><td>

protocol

</td><td>

Protocol to use when connecting to the Zabbix server.Default value: http

</td></tr><tr><td>

with\_triggers

</td><td>

It will fetch the trigger information.Default value: false

</td></tr></tbody>
</table>**Note:** When monitoring a large number of hosts in Zabbix, fetching massive metric data can impact performance and cause API timeouts; enabling batch processing \(enable\_batch\_processing = true\) mitigates this by fetching metrics in batches \(default: 1000 hosts, configurable via **max\_hosts\_per\_batch**\), though it increases network calls and must be used when monitoring 10,000+ hosts or facing performance issues.

**Parent Topic:**[Event Management reference](event-management-reference.md)

