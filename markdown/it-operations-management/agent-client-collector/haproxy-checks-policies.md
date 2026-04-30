---
title: HAProxy default checks and policies
description: Agent Client Collector provides the following default checks and policies for HAProxy monitoring.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# HAProxy default checks and policies

Agent Client Collector provides the following default checks and policies for HAProxy monitoring.

<table id="table_vzf_4m4_f5b"><thead><tr><th>

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

Event

</td><td>

check-haproxy

</td><td>

Retrieves the details of the HAProxy load balancer to determine whether it is running.

</td><td>

```
commonchecks    check-haproxy (options)
-h    host host
-P    port Port on which the HAProxy server is running
-A    all services all services
-q    Path on which HAProxy Stats URI is configured
-use ssl    ssl
```

 Usage example: `check-haproxy.rb -h localhost -P 8080 -A true -q stats -use_ssl false`

</td><td>

`CheckHAProxy OK: UP: 50% of 4 // services, DOWN: backend/nginx1[L4CON], backend/BACKEND`

</td></tr></tbody>
</table><table id="table_wkh_qp4_f5b"><thead><tr><th>

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

metrics-check-haproxy

</td><td>

Retrieves the HAProxy load balancer metrics to determine whether it is running.

</td><td>

```
commonchecks metrics-check-haproxy (options) 

-q host		Path on which HAProxy Stats URI is configured 

-P port		Port on which the HAProxy server is running 

-c host	       host name
```

 Usage example: `metrics-check-haproxy.rb -q stats -P 8080 -c localhost`

</td><td>

```
<hostname>.haproxy.frontend.session_current 0 1652265603
<hostname>.haproxy.frontend.session_total 0 1652265603
<hostname>.haproxy.backend.session_current 0 1652265603 
<hostname>.haproxy.backend.session_total 1 1652265603
```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

