---
title: Synchronization properties for validating Agent Client Collector plugins
description: Use the following properties when synchronizing public certificates from the MID Server to the Agent Client Collector.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Synchronization properties for validating Agent Client Collector plugins

Use the following properties when synchronizing public certificates from the MID Server to the Agent Client Collector.

<table id="table_d4h_c23_rwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.acc.cert\_monitor\_disable

</td><td>

Ability to disable the monitor from synchronizing the public certificates.Default value: False

</td></tr><tr><td>

mid.acc.cert\_monitor\_interval

</td><td>

Interval \(in seconds\) at which the monitor synchronizes public certificates from a configured endpoint URL.Default value: 86400

</td></tr><tr><td>

mid.acc.cert\_monitor\_target\_url

</td><td>

Endpoint URL prefix \(minus the filename\) from which the monitor synchronizes public certificates.Default value: ServiceNow Install server

</td></tr><tr><td>

mid.acc.cert\_monitor\_target\_filename

</td><td>

Endpoint URL target filename from which the monitor synchronizes public certificates.Default value: SNCertificates.zip

</td></tr></tbody>
</table><table id="table_bgk_3tg_twb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fetch-certificates-from-mid

</td><td>

Status of whether the public certificates are retrieved from the MID Server for plugin asset validation. Default value: True

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

