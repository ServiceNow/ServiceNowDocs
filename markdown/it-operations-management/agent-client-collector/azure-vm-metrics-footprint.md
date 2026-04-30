---
title: Azure virtual machine footprint
description: The following tables describe Azure virtual machine \(VM\) resource consumption in a Linux environment.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-10-14"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Azure virtual machine footprint

The following tables describe Azure virtual machine \(VM\) resource consumption in a Linux environment.

|Parameter|Value|
|---------|-----|
|Host spec|Ubuntu OS 20, 8 CPUs, 16GB RAM, 1000MB/s|
|Policy name|Azure VM metrics \(Linux proxy agent\)|
|Check name|Azure metrics collector|
|Number of VMs|10K|
|Number of checks|1|
|Number of metrics / minute|350K|
|Network utilization - Tx \(Agent &gt; MID\)|16 MB/s|
|Network utilization - Tx \(Agent &lt; MID\)|18 MB/s|
|Memory consumption|˜180MB|
|CPU of all checks|˜0%|
|Process CPU utilization|70%|
|Host CPU utilization|˜95%|

|Parameter|Value|
|---------|-----|
|Host spec|Ubuntu OS 20, 8 CPUs, 16GB RAM, 1000MB/s|
|Policy name|Azure VM metrics \(Linux proxy agent\)|
|Check name|Azure metrics collector|
|Number of VMs|10K|
|Number of checks|1|
|Number of metrics / minute|350K|
|Network utilization - Tx \(Agent &gt; MID\)|17 MB/s|
|Network utilization - Tx \(Agent &lt; MID\)|20 MB/s|
|Memory consumption|˜144MB|
|CPU of all checks|˜0%|
|Process CPU utilization|65%|
|Host CPU utilization|˜93%|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

