---
title: Google Cloud Platform \(GCP\) metrics
description: The following table lists and describes the metrics that are gathered by the acc\_grp\_metrics\_list.json configuration data file. The file is uploaded to a check definition or check instance, and the metrics in the file are monitored by the check for its agent.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Google Cloud Platform \(GCP\) metrics

The following table lists and describes the metrics that are gathered by the **acc\_grp\_metrics\_list.json** configuration data file. The file is uploaded to a check definition or check instance, and the metrics in the file are monitored by the check for its agent.

<table id="table_ofv_4jy_khc"><thead><tr><th>

Metric name

</th><th>

Metric type

</th><th>

Service

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CPU utilization

</td><td>

appengine.googleapis.com/flex/cpu/utilization

</td><td rowspan="2" align="center">

app engine

</td><td>

Fractional utilization of allocated CPU across an App Engine flexible environment version.

</td></tr><tr><td>

Response count

</td><td>

appengine.googleapis.com/http/server/response\_count

</td><td>

Delta HTTP response count

</td></tr><tr><td>

Free disk space percent

</td><td>

file.googleapis.com/nfs/server/free\_bytes\_percent

</td><td align="center">

file

</td><td>

Free disk space as a percentage of the total space.

</td></tr><tr><td>

Circuit Operational Status

</td><td>

interconnect.googleapis.com/network/interconnect/link/operational

</td><td rowspan="2" align="center">

interconnect

</td><td>

Whether the operational status of the circuit is 'up'. This metric is specific to individual physical circuits

</td></tr><tr><td>

Operational Status

</td><td>

interconnect.googleapis.com/network/interconnect/operational

</td><td>

Whether the operational status of the interconnect is 'up'. This metric is specific to the aggregate LACP bundle.

</td></tr><tr><td>

Instance group size

</td><td>

compute.googleapis.com/instance\_group/size

</td><td rowspan="30" align="center">

compute

</td><td>

The number of VMs in the instance group.

</td></tr><tr><td>

CPU utilization

</td><td>

compute.googleapis.com/instance/cpu/utilization

</td><td>

Fractional utilization of allocated CPU on this instance. Values are typically numbers between 0.0 and 1.0 \(but can exceed 1.0\). Charts display the values as a percentage between 0% and 100% \(or more\).

</td></tr><tr><td>

CPU usage time

</td><td>

compute.googleapis.com/instance/cpu/usage\_time

</td><td>

Delta CPU usage time in seconds. Cumulative CPU usage time since instance start.

</td></tr><tr><td>

CPU scheduler wait time

</td><td>

compute.googleapis.com/instance/cpu/scheduler\_wait\_time

</td><td>

Wait time is the time a vCPU is runnable but not scheduled to run by the hypervisor.

</td></tr><tr><td>

CPU reserved cores

</td><td>

compute.googleapis.com/instance/cpu/reserved\_cores

</td><td>

Number of cores reserved for the instance.

</td></tr><tr><td>

Disk queue length

</td><td>

compute.googleapis.com/guest/disk/queue\_length

</td><td>

Number of requests waiting to be handled by the disk.

</td></tr><tr><td>

Uptime

</td><td>

compute.googleapis.com/instance/uptime

</td><td>

Delta of how long the VM has been running, measured in seconds.For availability monitoring, use uptime checks instead.

</td></tr><tr><td>

Disk read bytes

</td><td>

compute.googleapis.com/instance/disk/read\_bytes\_count

</td><td>

Delta count of bytes read from disk.

</td></tr><tr><td>

Disk max read operations

</td><td>

compute.googleapis.com/instance/disk/max\_read\_ops\_count

</td><td>

Maximum number of read operations that can be performed per second.

</td></tr><tr><td>

Disk write bytes

</td><td>

compute.googleapis.com/instance/disk/write\_bytes\_count

</td><td>

Delta count of bytes written to disk.

</td></tr><tr><td>

Disk max write operations

</td><td>

compute.googleapis.com/instance/disk/max\_write\_ops\_count

</td><td>

Maximum number of write operations that can be performed per second.

</td></tr><tr><td>

Disk read operations

</td><td>

compute.googleapis.com/instance/disk/read\_ops\_count

</td><td>

Delta count of disk read IO operations.

</td></tr><tr><td>

Disk write operations

</td><td>

compute.googleapis.com/instance/disk/write\_ops\_count

</td><td>

Delta count of disk write IO operations.

</td></tr><tr><td>

Memory balloon RAM size

</td><td>

compute.googleapis.com/instance/memory/balloon/ram\_size

</td><td>

The total amount of memory allocated to the guest's balloon driver in bytes. Memory ballooning enables the hypervisor to reclaim memory from the guest VM.

</td></tr><tr><td>

Memory balloon RAM used

</td><td>

compute.googleapis.com/instance/memory/balloon/ram\_used

</td><td>

Memory currently used by the guest RAM, excluding memory used by the balloon itself, measured in bytes.

</td></tr><tr><td>

Memory swap in

</td><td>

compute.googleapis.com/instance/memory/balloon/swap\_in\_bytes\_count

</td><td>

The amount of memory \(in bytes\) swapped in from disk to memory.

</td></tr><tr><td>

Memory swap out

</td><td>

compute.googleapis.com/instance/memory/balloon/swap\_out\_bytes\_count

</td><td>

The amount of memory \(in bytes\) swapped out from memory to disk.

</td></tr><tr><td>

Network received bytes

</td><td>

compute.googleapis.com/instance/network/received\_bytes\_count

</td><td>

Delta count of bytes received from the network.

</td></tr><tr><td>

Network sent bytes

</td><td>

compute.googleapis.com/instance/network/sent\_bytes\_count

</td><td>

Delta count of bytes sent over the network.

</td></tr><tr><td>

Network received packets

</td><td>

compute.googleapis.com/instance/network/received\_packets\_count

</td><td>

Delta count of packets received from the network.

</td></tr><tr><td>

Network sent packets

</td><td>

compute.googleapis.com/instance/network/sent\_packets\_count

</td><td>

Delta count of packets sent over the network.

</td></tr><tr><td>

Anonymous memory used

</td><td>

compute.googleapis.com/guest/memory/anonymous\_used

</td><td>

Anonymous memory usage in bytes. Anonymous memory represents memory that is not backed by a file.

</td></tr><tr><td>

Memory bytes used

</td><td>

compute.googleapis.com/guest/memory/bytes\_used

</td><td>

Total memory usage in bytes.

</td></tr><tr><td>

Dirty memory used

</td><td>

compute.googleapis.com/guest/memory/dirty\_used

</td><td>

Dirty memory usage in bytes. Dirty pages are pages in memory that have been modified but not yet written to disk.

</td></tr><tr><td>

Page cache used

</td><td>

compute.googleapis.com/guest/memory/page\_cache\_used

</td><td>

Page cache memory usage in bytes. Page cache is used to cache file data.

</td></tr><tr><td>

Unevictable memory used

</td><td>

compute.googleapis.com/guest/memory/unevictable\_used

</td><td>

Unevictable memory usage in bytes. Unevictable memory is memory that cannot be swapped out.

</td></tr><tr><td>

Disk operation bytes

</td><td>

compute.googleapis.com/guest/disk/operation\_bytes\_count

</td><td>

Delta count of bytes transferred in disk operations.

</td></tr><tr><td>

System problem state

</td><td>

compute.googleapis.com/guest/system/problem\_state

</td><td>

Indicates whether the system is experiencing problems. 1 means there is a problem, 0 means no problem.

</td></tr><tr><td>

System uptime

</td><td>

compute.googleapis.com/guest/system/uptime

</td><td>

Delta of system uptime in seconds.

</td></tr><tr><td>

System problem count

</td><td>

compute.googleapis.com/guest/system/problem\_count

</td><td>

Delta count of system problems detected.

</td></tr><tr><td>

CPU limit utilization

</td><td>

kubernetes.io/anthos/container/cpu/limit\_utilization

</td><td rowspan="2" align="center">

anthos

</td><td>

The fraction of the CPU limit that is currently in use on the instance.

</td></tr><tr><td>

Memory limit utilization

</td><td>

kubernetes.io/anthos/container/memory/limit\_utilization

</td><td>

The fraction of the memory limit that is currently in use on the instance.

</td></tr><tr><td>

Executions

</td><td>

cloudfunctions.googleapis.com/function/execution\_count

</td><td align="center">

cloudfunctions

</td><td>

Count of function executions broken down by status.

</td></tr><tr><td>

Tunnel established

</td><td>

n.googleapis.com/tunnel\_established

</td><td align="center">

vpn

</td><td>

Indicates successful tunnel establishment if &gt; 0.

</td></tr><tr><td>

RTT latencies per internal TCP/UDP load balancer

</td><td>

loadbalancing.googleapis.com/l3/internal/rtt\_latencies

</td><td align="center">

loadbalancing

</td><td>

A distribution of RTT measured over TCP connections for internal TCP/UDP load balancer flows.

</td></tr><tr><td>

Unacked messages by region

</td><td>

pubsub.googleapis.com/subscription/num\_unacked\_messages\_by\_region

</td><td align="center">

pubsub

</td><td>

Number of unacknowledged messages in a subscription, broken down by Cloud region.

</td></tr><tr><td>

Disabled for network

</td><td>

firebasedatabase.googleapis.com/network/disabled\_for\_overages

</td><td rowspan="3" align="center">

firebasedatabase

</td><td>

Indicates if the Firebase database has been disabled for network overages.

</td></tr><tr><td>

Disabled for storage

</td><td>

firebasedatabase.googleapis.com/storage/disabled\_for\_overages

</td><td>

Indicates if the Firebase database has been disabled for storage overages.

</td></tr><tr><td>

Database load

</td><td>

firebasedatabase.googleapis.com/io/database\_load

</td><td>

Fraction of database load, grouped by type.

</td></tr><tr><td>

CPU utilization

</td><td>

cloudsql.googleapis.com/database/cpu/utilization

</td><td rowspan="5" align="center">

cloudsql

</td><td>

Current CPU utilization represented as a percentage of the reserved CPU that is currently in use.

</td></tr><tr><td>

Disk utilization

</td><td>

cloudsql.googleapis.com/database/disk/utilization

</td><td>

The fraction of the disk quota that is currently in use.

</td></tr><tr><td>

Instance state

</td><td>

cloudsql.googleapis.com/database/instance\_state

</td><td>

The current serving state of the Cloud SQL instance.

</td></tr><tr><td>

Memory utilization

</td><td>

cloudsql.googleapis.com/database/memory/utilization

</td><td>

The fraction of the memory quota that is currently in use.

</td></tr><tr><td>

Server up

</td><td>

cloudsql.googleapis.com/database/up

</td><td>

Indicates if the server is up.

</td></tr><tr><td>

CPU utilization by priority

</td><td>

spanner.googleapis.com/instance/cpu/utilization\_by\_priority

</td><td rowspan="3" align="center">

spanner

</td><td>

Percent utilization of provisioned CPU, by priority.

</td></tr><tr><td>

Smoothed CPU utilization

</td><td>

spanner.googleapis.com/instance/cpu/smoothed\_utilization

</td><td>

24-hour smoothed utilization of provisioned CPU.

</td></tr><tr><td>

Storage used

</td><td>

spanner.googleapis.com/instance/storage/used\_bytes

</td><td>

Storage used in bytes. Sampled every 60 seconds.

</td></tr><tr><td>

CPU usage percent

</td><td>

memcache.googleapis.com/node/cpu/utilization

</td><td rowspan="2" align="center">

memcache

</td><td>

CPU usage percent by Memcached node.

</td></tr><tr><td>

Cache memory usage

</td><td>

memcache.googleapis.com/node/cachememory

</td><td>

Bytes allotted for the Memcached cache in this node, grouped by whether that memory is used.

</td></tr><tr><td>

Used memory

</td><td>

redis.googleapis.com/redis.googleapis.com/stats/memory/usage\_ratio

</td><td rowspan="2" align="center">

redis

</td><td>

Total number of bytes allocated by Redis.

</td></tr><tr><td>

Memory usage ratio

</td><td>

redis.googleapis.com/stats/memory/usage\_ratio

</td><td>

Memory usage as a ratio of maximum memory.

</td></tr><tr><td>

CPU load

</td><td>

bigtable.googleapis.com/cluster\_cpu\_load

</td><td rowspan="3" align="center">

bigtable

</td><td>

CPU load of a cluster.

</td></tr><tr><td>

Disk load

</td><td>

bigtable.googleapis.com/cluster\_disk\_load

</td><td>

Utilization of HDD disks in a cluster.

</td></tr><tr><td>

Storage utilization

</td><td>

bigtable.googleapis.com/cluster\_storage\_utilization

</td><td>

Storage used as a fraction of total storage capacity.

</td></tr><tr><td>

HDFS storage utilization

</td><td>

dataproc.googleapis.com/cluster/hdfs/storage\_utilization

</td><td rowspan="2" align="center">

dataproc

</td><td>

The percentage of HDFS storage currently used.

</td></tr><tr><td>

Unhealthy HDFS blocks by status

</td><td>

dataproc.googleapis.com/hdfs/unhealthy\_blocks

</td><td>

Indicates the number of unhealthy blocks inside the cluster.

</td></tr><tr><td>

Processes

</td><td>

agent.googleapis.com/processes/count\_by\_state

</td><td rowspan="2" align="center">

processes

</td><td>

Count of processes in the given state. Relevant for Linux only.

</td></tr><tr><td>

Process CPU

</td><td>

agent.googleapis.com/processes/cpu\_time

</td><td>

Time taken by CPU to complete a given process.

</td></tr><tr><td>

TCP connections

</td><td>

agent.googleapis.com/processes/network

</td><td align="center">

network

</td><td>

Current count of TCP connections.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

