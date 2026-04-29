---
title: Network host availability check
description: Agent Client Collector provides the following default check for network ping monitoring. The check is available for both Windows and Linux.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Network host availability check

Agent Client Collector provides the following default check for network ping monitoring. The check is available for both Windows and Linux.

<table id="table_wf5_rkn_jdc"><thead><tr><th>

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

util.check-ping

</td><td>

Checks the network host availability via ICMP \(ping\) requests.

 Generates an OK event if the ping success ratio exceeds the Warning threshold \(-W, default 50%\).

 Generates a Warning event if the ping success ratio is between the warning threshold \(-W, default 50%\) and the critical threshold \(-C, default 20%\).

 Generates a Critical event if the ping success ratio falls below the critical threshold \(-C, default 20%\).

 A proxy agent is required.

</td><td>

`check-ping.rb -h <ip-address>` \(options\)`-h host`: Host to ping \(Required\). Default=&lt;localhost&gt;

`-c count`: Number of ping requests sent to the host. Default=1

`-T timeout`: The timeout \(in seconds\) for each ping request. If the timeout expires before a reply is received, the ping is considered failed. Default=5

`-6 ipv6`: Enables IPv6 pinging. Ping uses IPv4 when this flag is not used. Default=False

`-i interval`: Interval \(in seconds\) between each ping request. Default=1

`-W ratio`: The success ratio threshold for a Warning state. If the successful ping responses are below this ratio and above the -C ratio, the script returns a Warning. Default=0.5

`-C ratio`: The success ratio threshold for a Critical state. If the successful ping responses are below this ratio, the script returns a Critical failure. Default=0.2

`-r report`: Flag to append to the failure message of an MTR \(My Trace Route\) report if the ping fails. When MTR runs, a network diagnostic report generates. Default=false

</td><td>

 

</td><td>

```
ICMP ping unsuccessful for host: 192.168.1.1 (successful: 0/5)
```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

