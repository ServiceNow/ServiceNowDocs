---
title: Discovery resource utilization
description: Standard transactions on Windows and UNIX generate various amounts of network traffic, depending on what is being discovered.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery resource utilization

Standard transactions on Windows and UNIX generate various amounts of network traffic, depending on what is being discovered.

These tables show the bandwidth consumption for each data flow segment of a typical discovery using probes and patterns over different operating systems.

|Device Type|MID &gt; Instance|Instance &gt; MID|MID &gt; Target|Target &gt; MID|Total|
|-----------|-----------------|-----------------|---------------|---------------|-----|
|Windows 2016|0.104966|0.101271|0.77739|2.364353|3.34798|
|Windows 2012|0.126327|0.07928|1.177146|3.70751|5.089804|
|Windows 2008|0.141816|0.104674|1.032673|3.594784|4.873947|
|Windows 10|0.091466|0.075601|0.642313|2.221103|3.030483|
|Linux CentOS|0.164232|0.111376|0.148742|0.690117|1.114467|
|Mac OSX|0.103707|0.068302|0.021681|0.461365|0.655055|
|HP-UX|0.120358|0.106676|0.042669|0.101149|0.370852|
|Solaris|0.130551|0.099414|0.060243|0.346605|0.636813|
|Cisco UCS Switch|0.029655|0.027465|0.094918|0.097444|0.249492|
|F5 Load Balancer|0.043935|0.03689|0.017179|0.012132|0.110136|
|A10 Load Balancer|0.046631|0.032266|0.018313|0.03182|0.12903|
|EMC Storage|0.4776|0.373828|1.215954|4.741926|6.809308|

The following table shows the bandwidth comparison between an initial discovery for three-tier applications and for each subsequent discovery. Bandwidth is broken up into the three tiers: UI \(Apache\), application \(Websphere\), and data \(Oracle\). This measures the total data transfer for each discovery run once for a device class.

|Device Type|MID &gt; Instance|Instance &gt; MID|MID &gt; Target|Target &gt; MID|Total|
|-----------|-----------------|-----------------|---------------|---------------|-----|
|Three-tier application - Initial discovery|0.712829|0.678862|7.084678|9.430181|17.90655|
|F5 Load Balancer| | | |0.017179|0.012132|
|Apache on Linux| | | |0.540161|1.107108|
|Websphere on Linux| | | |0.729403|1.165112|
|Oracle on Windows| | | |5.797935|7.145829|
| | | | | | |
|Three-tier application - subsequent discovery|0.150882|0.107409|2.536535|0.560122|3.354948|
|F5 load balancer| | | |0.001347|0.012132|
|Apache on Linux| | | |0.136366|0.79392|
|Websphere on Linux| | | |0.341042|0.11365|
|Oracle on Windows| | | |2.05778|0.354948|

This table shows discovery of different OS types using patterns. This measures, in megabytes, the total amount of data created and the total amount of data in subsequent scans for each device.

|Device| |MID &gt; Instance|Instance &gt; MID|MID &gt; Target|Target &gt; MID|Total|
|------|---|-----------------|-----------------|---------------|---------------|-----|
|Linux|Create|0.39|0.486|0.098|0.273|1.247|
| |Update|0.382|0.499|0.093|0.264|1.238|
|Windows Server|Create|0.289|0.316|5.628|8.508|14.741|
| |Update|0.273|0.306|5.621|8.458|14.658|
|Solaris|Create|1.222|1.4|0.383|0.917|3.922|
| |Update|1.24|1.42|.399|.675|3.734|
|HP-UX|Create|0.176|0.222|0.063|0.13|0.591|
| |Update|0.178|0.247|0.062|0.128|0.615|
|Citrix Netscaler|Create|0.424|1.919|0.019|0.042|2.404|
| |Update|0.355|0.619|0.016|0.041|1.031|
|F5|Create|0.087|0.135|0.026|0.047|0.295|
| |Update|0.132|0.171|0.026|0.047|0.376|
|L3 Switch|Create|0.172|0.125|0.282|0.478|1.057|
| |Update|0.178|0.126|0.282|0.479|1.065|

**Note:** These measurements were taken with base operating configurations. Your local system results may vary.

## CPU Usage examples

Examples from CPU Usage will vary among the matrix of thousands of combinations of Operating Systems, chip sets and specific loads for each system.

Your mix of these variables will determine your unique level of CPU consumption.

You can identify unique builds using internal templates and discover them by watching the performance impact, or lack of performance impact that your Discovery tool has on your system.

