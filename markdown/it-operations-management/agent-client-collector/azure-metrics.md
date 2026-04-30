---
title: Azure metrics
description: The following tables list and describe the metrics that are gathered as output from Azure checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Azure metrics

The following tables list and describe the metrics that are gathered as output from Azure checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

<table id="table_svt_2t2_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

apiserver\_current\_inflight\_requests\(Featured metric\)

</td><td>

Maximum number of currently used inflight requests on the API server per request kind in the past second.

</td></tr><tr><td>

cluster\_autoscaler\_cluster\_safe\_to\_autoscale

</td><td>

Determines whether cluster autoscaler takes action on the cluster.

</td></tr><tr><td>

cluster\_autoscaler\_scale\_down\_in\_cooldown

</td><td>

Determines if the scale down is in cooldown; no nodes are removed during this timeframe.

</td></tr><tr><td>

cluster\_autoscaler\_unschedulable\_pods\_count

</td><td>

Number of pods that are currently not able to be scheduled in the cluster.

</td></tr><tr><td>

kube\_node\_status\_allocatable\_cpu\_cores\(Featured metric\)

</td><td>

Total number of available CPU cores in a managed cluster.

</td></tr><tr><td>

kube\_node\_status\_allocatable\_memory\_bytes\(Featured metric\)

</td><td>

Total amount of available memory in a managed cluster.

</td></tr><tr><td>

kube\_node\_status\_condition\(Featured metric\)

</td><td>

Statuses for various node conditions.

</td></tr><tr><td>

kube\_pod\_status\_phase\(Featured metric\)

</td><td>

Number of pods by phase.

</td></tr><tr><td>

kube\_pod\_status\_ready\(Featured metric\)

</td><td>

Number of pods in Ready state.

</td></tr><tr><td>

node\_cpu\_usage\_millicores\(Featured metric\)

</td><td>

Aggregated measurement of CPU utilization in millicores across the cluster.

</td></tr><tr><td>

node\_cpu\_usage\_percentage\(Featured metric\)

</td><td>

Aggregated average CPU utilization measured in percentage across the cluster.

</td></tr><tr><td>

node\_disk\_usage\_bytes

</td><td>

Number of disk space bytes in use by device.

</td></tr><tr><td>

node\_disk\_usage\_percentage\(Featured metric\)

</td><td>

Percentage of disk space used by device.

</td></tr><tr><td>

node\_memory\_rss\_bytes

</td><td>

Number of container RSS memory bytes in use.

</td></tr><tr><td>

node\_memory\_rss\_percentage\(Featured metric\)

</td><td>

Percentage of container RSS memory in use.

</td></tr><tr><td>

node\_memory\_working\_set\_bytes

</td><td>

Number of container working set memory bytes in use.

</td></tr><tr><td>

node\_memory\_working\_set\_percentage\(Featured metric\)

</td><td>

Percentage of container working set memory in use.

</td></tr><tr><td>

node\_network\_in\_bytes\(Featured metric\)

</td><td>

Network received bytes.

</td></tr><tr><td>

node\_network\_out\_bytes\(Featured metric\)

</td><td>

Network transmitted bytes.

</td></tr></tbody>
</table><table id="table_oj5_sz2_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Percentage CPU\(Featured metric\)

</td><td>

The percentage of allocated compute units that are currently in use by the Virtual Machine\(s\).

</td></tr><tr><td>

CPU Credits Remaining

</td><td>

Total number of credits available to burst. Only available on B-series burstable VMs.

</td></tr><tr><td>

CPU Credits Consumed

</td><td>

Total number of credits consumed by the Virtual Machine. Only available on B-series burstable VM.

</td></tr></tbody>
</table><table id="table_dw3_lbf_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network In\(Featured metric\)

</td><td>

The number of billable bytes received on all network interfaces by the Virtual Machines \(Incoming Traffic\) \(Deprecated\).

</td></tr><tr><td>

Network Out\(Featured metric\)

</td><td>

The number of billable bytes out on all network interfaces by the Virtual Machines \(Outgoing Traffic\) \(Deprecated\).

</td></tr><tr><td>

Network In Total\(Featured metric\)

</td><td>

The number of bytes received on all network interfaces by the Virtual Machines \(Incoming Traffic\).

</td></tr><tr><td>

Network Out Total\(Featured metric\)

</td><td>

The number of bytes out on all network interfaces by the Virtual Machines \(Outgoing Traffic\).

</td></tr></tbody>
</table><table id="table_p2s_xbf_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disk Read Bytes\(Featured metric\)

</td><td>

Bytes read from disk during monitoring period.

</td></tr><tr><td>

Disk Write Bytes\(Featured metric\)

</td><td>

Bytes written to disk during monitoring period.

</td></tr><tr><td>

Disk Read Operations/Sec\(Featured metric\)

</td><td>

Disk Read IOPS.

</td></tr><tr><td>

Disk Write Operations/Sec\(Featured metric\)

</td><td>

Disk Write IOPS.

</td></tr><tr><td>

Data Disk Read Bytes/sec\(Featured metric\)

</td><td>

Bytes per second read from a single disk during monitoring period.

</td></tr><tr><td>

Data Disk Write Bytes/sec\(Featured metric\)

</td><td>

Bytes per second written to a single disk during monitoring period.

</td></tr><tr><td>

Data Disk Read Operations/Sec\(Featured metric\)

</td><td>

Read IOPS from a single disk during monitoring period.

</td></tr><tr><td>

Data Disk Write Operations/Sec\(Featured metric\)

</td><td>

Write IOPS from a single disk during monitoring period.

</td></tr><tr><td>

Data Disk Bandwidth Consumed Percentage\(Featured metric\)

</td><td>

Percentage of data disk bandwidth consumed per minute.

</td></tr><tr><td>

Data Disk IOPS Consumed Percentage\(Featured metric\)

</td><td>

Percentage of data disk I/Os consumed per minute.

</td></tr><tr><td>

Data Disk Target Bandwidth\(Featured metric\)

</td><td>

Baseline bytes per second throughput Data Disk can achieve without bursting.

</td></tr><tr><td>

Data Disk Target IOPS\(Featured metric\)

</td><td>

Baseline IOPS Data Disk can achieve without bursting.

</td></tr><tr><td>

Data Disk Max Burst Bandwidth\(Featured metric\)

</td><td>

Maximum bytes per second throughput Data Disk can achieve with bursting.

</td></tr><tr><td>

Data Disk Max Burst IOPS\(Featured metric\)

</td><td>

Maximum IOPS Data Disk can achieve with bursting.

</td></tr><tr><td>

Data Disk Used Burst BPS Credits Percentage

</td><td>

Percentage of Data Disk burst bandwidth credits used so far.

</td></tr><tr><td>

Data Disk Used Burst IO Credits Percentage

</td><td>

Percentage of Data Disk burst I/O credits used so far.

</td></tr><tr><td>

Premium Data Disk Cache Read Hit\(Featured metric\)

</td><td>

Premium Data Disk Cache Read Hit.

</td></tr><tr><td>

Premium Data Disk Cache Read Miss\(Featured metric\)

</td><td>

Premium Data Disk Cache Read Miss.

</td></tr><tr><td>

Premium OS Disk Cache Read Hit\(Featured metric\)

</td><td>

Premium OS Disk Cache Read Hit.

</td></tr><tr><td>

Premium OS Disk Cache Read Miss\(Featured metric\)

</td><td>

Premium OS Disk Cache Read Miss.

</td></tr></tbody>
</table><table id="table_pdv_bcf_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inbound Flows\(Featured metric\)

</td><td>

Inbound Flows are number of current flows in the inbound direction \(traffic going into the VM\).

</td></tr><tr><td>

Outbound Flows\(Featured metric\)

</td><td>

Maximum creation rate of outbound flows \(traffic going out of the VM\).

</td></tr><tr><td>

Inbound Flows Maximum Creation Rate\(Featured metric\)

</td><td>

Maximum creation rate of inbound flows \(traffic going into the VM\).

</td></tr><tr><td>

Outbound Flows Maximum Creation Rate\(Featured metric\)

</td><td>

Maximum creation rate of outbound flows \(traffic going out of the VM\).

</td></tr></tbody>
</table><table id="table_evr_fcf_vrb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

VM Cached Bandwidth Consumed Percentage\(Featured metric\)

</td><td>

Percentage of cached disk bandwidth consumed by the VM.

</td></tr><tr><td>

VM Cached IOPS Consumed Percentage

</td><td>

Percentage of cached disk IOPS consumed by the VM.

</td></tr><tr><td>

VM Uncached Bandwidth Consumed Percentage\(Featured metric\)

</td><td>

Percentage of uncached disk bandwidth consumed by the VM.

</td></tr><tr><td>

VM Uncached Bandwidth Consumed Percentage

</td><td>

Percentage of uncached disk IOPS consumed by the VM.

</td></tr><tr><td>

Available Memory Byte\(Featured metric\)

</td><td>

Amount of physical memory, in bytes, immediately available for allocation to a process or for system use in the Virtual Machine.

</td></tr></tbody>
</table>|Metric name|Units|Description|
|-----------|-----|-----------|
|Percentage CPU \(featured metric\)|%|The percentage of allocated compute units that are currently in use by the Virtual Machine.|
|CPU Credits Remaining| |Number of earned CPU credits that have not been consumed by the Virtual Machine.|
|CPU Credits Consumed| |Total number of CPU credits that have been consumed by the Virtual Machine.|
|Network In| |Number of bytes received on all network interfaces by the instance.|
|Network Out| |Number of bytes sent out on all network interfaces by the instance.|
|Network In Total \(featured metric\)|Bytes|The number of bytes received on all network interfaces by the Virtual Machine\(s\) \(Incoming Traffic\).|
|Network Out Total \(featured metric\)|Bytes|The number of bytes out on all network interfaces by the Virtual Machine\(s\) \(Outgoing Traffic\).|
|Available Memory Bytes \(featured metric\)|Bytes|Amount of physical memory in bytes immediately available for allocation to a process or for system use in the Virtual Machine.|
|VM Cached Bandwidth Consumed Percentage| |Percentage of cached disk bandwidth consumed by the VM.|
|VM Cached IOPS Consumed Percentage| |Percentage of cached disk IOPS consumed by the VM.|
|VM Uncached Bandwidth Consumed Percentage| |Percentage of uncached disk bandwidth consumed by the VM.|
|VM Uncached IOPS Consumed Percentage| |Percentage of uncached disk IOPS consumed by the VM.|
|Disk Read Bytes \(featured metric\)|Bytes|Bytes read from disk during monitoring period.|
|Disk Write Bytes \(featured metric\)|Bytes|Bytes written to disk during monitoring period.|
|Disk Read Operations/Sec \(featured metric\)|CountPerSecond|Disk Read IOPS.|
|Disk Write Operations/Sec \(featured metric\)|CountPerSecond|Disk Write IOPS.|
|OS Disk Read Bytes/sec| |Bytes/Sec read from disk during monitoring period.|
|OS Disk Write Bytes/sec| |Bytes/Sec written to disk during monitoring period.|
|OS Disk Read Operations/Sec| |Read IOPS from disk during monitoring period.|
|OS Disk Write Operations/Sec| |Write IOPS from disk during monitoring period.|
|OS Disk Queue Depth| |Average number of read and write requests that were queued for the selected disk during the sample period.|
|OS Disk Bandwidth Consumed Percentage| |Percentage of data disk bandwidth consumed per minute.|
|OS Disk IOPS Consumed Percentage| |Percentage of data disk I/Os consumed per minute.|
|OS Disk Target Bandwidth| |Baseline bytes per second throughput data disk can achieve without bursting.|
|OS Disk Target IOPS| |Baseline IOPS data disk can achieve without bursting.|
|OS Disk Max Burst Bandwidth| |Maximum bytes per second throughput data disk can achieve with bursting.|
|OS Disk Max Burst IOPS| |Maximum IOPS data disk can achieve with bursting.|
|OS Disk Used Burst BPS Credits Percentage| |Percentage of data disk burst bandwidth credits used so far.|
|OS Disk Used Burst IO Credits Percentage| |Percentage of data disk burst I/O credits used so far.|
|Premium OS Disk Cache Read Hit| |Premium OS disk cache read hit.|
|Premium OS Disk Cache Read Miss| |Premium OS disk cache read miss.|
|Inbound Flows| |Number of current flows in the inbound direction \(traffic going into the VM\).|
|Outbound Flows| |Number of current flows in the inbound direction \(traffic going out of the VM\).|
|Inbound Flows Maximum Creation Rate| |Maximum creation rate of inbound flows \(traffic going into the VM\).|
|Outbound Flows Maximum Creation Rate| |Maximum creation rate of outbound flows \(traffic going out of the VM\).|

|Metric name|Units|Description|
|-----------|-----|-----------|
|AllocatedSnatPorts \(featured metric\)| |Total number of SNAT ports allocated within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|ByteCount \(featured metric\)|bytes|Total number of bytes transmitted within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|DipAvailability \(featured metric\)|count|Average load balancer health probe status per time duration.|
|BlockedCount \(featured metric\)| |Total number of packets transmitted within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|SnatConnectionCount \(featured metric\)|count|Total number of new SNAT connections created within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|SYNCount \(featured metric\)| |Total number of SYN packets transmitted within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|UsedSnatPorts \(featured metric\)| |Total number of SNAT ports used within the time period specified by the metric definition's **PT** \(Period of Time\) value.|
|VipAvailability \(featured metric\)|count|Average load balancer data path availability per time duration.|

|Metric name|Units|Description|
|-----------|-----|-----------|
|connectedclients| |Number of client connections to the cache.|
|totalcommandsprocessed| |Total number of commands processed by the cache server.|
|cachehits \(featured metric\)|count|Number of successful key lookups.|
|cachemisses \(featured metric\)|count|Number of failed key lookups.|
|cachemissrate| |Rate of failed key lookups.|
|getcommands| |Number of get operations from the cache.|
|setcommands \(featured metric\)|count|Number of set operations to the cache.|
|operationsPerSecond| |Number of instantaneous operations per second executed on the cache.|
|evictedkeys| |Number of items evicted from the cache.|
|totalkeys| |Number of keys in the cache.|
|expiredkeys| |Number of items expired from the cache.|
|usedmemory|bytes|Amount of cache memory used for key/value pairs in the cache.|
|usedmemoryRss|bytes|Amount of cache memory used during the specified reporting interval, including fragmentation and metadata|
|serverLoad \(featured metric\)|Percent|Percentage of cycles in which the Redis server is busy processing and not waiting idle for messages|
|cacheWrite \(featured metric\)|BytesPersSecond|Amount of data written to the cache.|
|cacheRead \(featured metric\)|BytesPerSecond|Amount of data read from the cache.|
|allConnectionsCreatedPerSecond| |Number of instantaneous connections created per second on the cache via port 6379 or 6380 \(SSL\).|
|allConnectionsClosedPerSecond| |Number of instantaneous connections closed per second on the cache via port 6379 or 6380 \(SSL\).|
|allconnectedclients \(featured metric\)|count|Number of currently connected clients to the system.|
|alltotalcommandsprocessed| |The cumulative count of all commands processed by the system.|
|alloperationsPerSecond| |Total number of operations \(such as read or write commands\) performed per second across all instances.|
|allusedmemory \(featured metric\)|bytes|Total amount of memory being used across the system.|
|allusedmemoryRss \(featured metric\)|bytes|The total Resident Set Size \(RSS\), which reflects the amount of memory physically present in RAM across all instances, including swap.|

|Metric name|Units|Description|
|-----------|-----|-----------|
|ApplicationGatewayTotalTime \(featured metric\)|MilliSeconds|Time that it takes for a request to be processed and its response to be sent.|
|AvgRequestCountPerHealthyHost| |Average request count per minute per healthy backend host in a pool.|
|AzwafBotProtectionMatches| |Matched Bot Rules.|
|AzwafCustomRuleMatches| |Matched Custom Rules.|
|AzwafSecRuleMatches| |Matched Managed Rules.|
|AzwafTotalRequests| |Total number of requests evaluated by WAF.|
|BackendConnectTime| |Time spent establishing a connection with a backend server.|
|BackendFirstByteResponseTime| |Time interval between start of establishing a connection to backend server and receiving the first byte of the response header, approximating processing time of backend server.|
|BackendLastByteResponseTime| |Time interval between start of establishing a connection to backend server and receiving the last byte of the response body.|
|BackendResponseStatus| |Number of HTTP response codes generated by the backend members. This does not include any response codes generated by the Application Gateway.|
|BlockedCount| |Total number of blocked operations or requests|
|BytesReceived \(featured metric\)|bytes|Total number of bytes received by the Application Gateway from the clients.|
|BytesSent \(featured metric\)|bytes|Total number of bytes sent by the Application Gateway to the clients.|
|CapacityUnits| |Capacity units consumed.|
|ClientRtt| |Round trip time between clients and Application Gateway. Indicates how long it takes to establish connections and return acknowledgments.|
|ComputeUnits| |Compute units consumed.|
|CpuUtilization| |Current CPU utilization of the Application Gateway.|
|CurrentConnections \(featured metric\)|count|Count of current connections established with Application Gateway.|
|EstimatedBilledCapacityUnits| |Estimated capacity units that will be charged.|
|FailedRequests \(featured metric\)|count|Count of failed requests that Application Gateway has served.|
|FixedBillableCapacityUnits| |Fixed Billable Capacity Units.|
|HealthyHostCount \(featured metric\)|count|Number of healthy backend hosts.|
|NewConnectionsPerSecond| |New connections per second established with Application Gateway.|
|ResponseStatus| |HTTP response status returned by Application Gateway.|
|Throughput \(featured metric\)|bytesPerSecond|Number of bytes per second the Application Gateway has served.|
|TotalRequests \(featured metric\)|count|Count of successful requests that Application Gateway has served.|
|UnhealthyHostCount \(featured metric\)|count|Number of unhealthy backend hosts.|

|Metric name|Units|Description|
|-----------|-----|-----------|
|Transactions \(featured metric\)|count|Total number of requests made to the storage account.|
|Ingress \(featured metric\)|bytes|Amount of ingress data. This number includes ingress from an external client into Azure Storage as well as ingress within Azure.|
|Egress \(featured metric\)|bytes|Amount of egress data. This number includes egress from an external client into Azure Storage as well as egress within Azure. As a result, this number does not reflect billable egress.|
|SuccessServerLatency \(featured metric\)|milliseconds|Average latency used by Azure Storage to process a successful request.|
|SuccessE2ELatency \(featured metric\)|milliseconds|The average end-to-end latency of successful requests made to a storage service or the specified API operation.|
|Availability \(featured metric\)|percent|The percentage of availability for the storage service or the specified API operation.|

<table id="table_atz_y2s_2sb"><thead><tr><th>

Metric Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Availability

</td><td>

Percentage of availability for the storage service or the specified API operation. Availability is calculated by taking the TotalBillableRequests value and dividing it by the number of applicable requests, including those that produced unexpected errors. All unexpected errors result in reduced availability for the storage service or the specified API operation.

</td></tr><tr><td>

BlobCapacity\(Featured metric\)

</td><td>

Amount of storage used by the storage account's Blob service, in bytes.

</td></tr><tr><td>

BlobCount

</td><td>

Number of Blobs in the storage account's Blob service

</td></tr><tr><td>

Container Count

</td><td>

Number of containers in the storage account's Blob service.

</td></tr><tr><td>

Egress\(Featured metric\)

</td><td>

Amount of Egress data, in bytes. Includes egress from an external client into Azure Storage as well as Egress within Azure. As a result, this number does not reflect billable Egress.

</td></tr><tr><td>

Index Capacity\(Featured metric\)

</td><td>

Amount of storage used by ADLS Gen2 \(Hierarchical\) Index, in bytes.

</td></tr><tr><td>

Ingress\(Featured metric\)

</td><td>

The amount of Ingress data, in bytes. Includes Ingress from an external client into Azure storage, as well as ingress within Azure.

</td></tr><tr><td>

SuccessE2ELatency\(Featured metric\)

</td><td>

End-to-end latency of successful requests made to a storage service or the specified API operation, in milliseconds. Includes the required processing time within Azure storage to read the request, send the response, and receive acknowledgment of the response.

</td></tr><tr><td>

SuccessServerLatency\(Featured metric\)

</td><td>

Latency used by Azure storage to process a successful request, in milliseconds. This value does not include the network latency specified in **SuccessE2ELatency**.

</td></tr><tr><td>

Transactions

</td><td>

Number of requests made to a storage service or the specified API operation. Includes successful and failed requests, as well as requests which produced errors. Use the **ResponseType** dimension for the number of different types of responses.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

