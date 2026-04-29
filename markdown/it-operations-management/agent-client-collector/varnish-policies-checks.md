---
title: Varnish default checks and policies
description: Agent Client Collector provides the following default checks and policies for Varnish monitoring.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Varnish default checks and policies

Agent Client Collector provides the following default checks and policies for Varnish monitoring.

<table id="table_bbw_1tt_f5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.varnish.metrics-varnish

</td><td>

Collects Varnish metrics from the host.

</td><td>

`linuxchecks metrics-varnish (options)` where:

-   -t = fields List of required metrics, comma separated within ""
-   -v = varnishname The Varnish instance to retrieve data from.

</td><td>

```
hostname.MAIN_sess_conn 175 1649420020
hostname.MAIN_sess_drop 0 1649420020 
hostname.MAIN_client_req 173 1649420020
hostname.MAIN_cache_hit 0 1649420020 
hostname.MAIN_cache_hitpass 0 1649420020
hostname.MAIN_cache_miss 167 1649420020 
hostname.MAIN_backend_conn 0 1649420020
hostname.MAIN_backend_unhealthy 0 1649420020 
hostname.MAIN_backend_busy 0 1649420020
hostname.MAIN_backend_fail 171 1649420020 
hostname.MAIN_backend_reuse 0 1649420020
hostname.MAIN_backend_recycle 0 1649420020
hostname.MAIN_threads 200 1649420020
hostname.MAIN_threads_limited 0 1649420020
hostname.MAIN_threads_created 200 1649420020
hostname.MAIN_threads_failed 0 1649420020
hostname.MAIN_thread_queue_len 0 1649420020
hostname.MAIN_sess_queued 0 1649420020
hostname.MAIN_n_expired 167 1649420020
hostname.MAIN_n_lru_nuked 0 1649420020
hostname.MAIN_backend_req 0 1649420020

```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

