---
title: Windows metrics
description: The following table lists the metrics that are gathered as output from Windows checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Windows metrics

The following table lists the metrics that are gathered as output from Windows checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|Process.Status| | |Windows process status including CPU and memory data.|
|Process.CpuPercent| | |Percentage of CPU used by the process.|
|Process.Memory\(KB\)| |KB|Memory used by the given process.|
|cpu.queuelength \(featured metric\)| | |Processor queue length.|
|cpu.loadavgsec \(featured metric\)| | |Average CPU load per second.|
|disk.AvgDisksec/Read| |seconds|Average time of a read from the disk.|
|disk.AvgDisksec/Write| |seconds|Average time of a write to the disk.|
|disk.DiskReadBytes/sec| |byte/sec|Rate at which bytes are transferred from the disk during read operations.|
|disk.DiskWriteBytes/sec| |byte/sec|Rate at which bytes are transferred to the disk during write operations.|
|disk\_usage.avail\(GB\)| |GB|Disk available.|
|disk\_usage.used\(GB\)| |GB|Disk used.|
|disk\_usage.total\(GB\)| |GB|Disk total.|
|disk\_usage.used\_percentage \(featured metric\)| | |Disk used in percentage.|
|mem.free\_physical\_percentage| | |Percent of free physical memory.|
|mem.free\_virtual\_percentage| | |Percent of free virtual memory.|
|ram.usage\_percentage \(featured metric\)| | |Percent of RAM used.|
|mem.free\_physical\(KB\)| |KB|Amount of free physical memory.|
|mem.total\_physical\(KB\)| |KB|Total physical memory.|
|mem.free\_virtual\(KB\)| |KB|Amount of free virtual memory.|
|mem.total\_virtual\(KB\)| |KB|Total virtual memory.|
|mem.available\(KB\)| |KB|Total amount of virtual memory available.|
|mem.total\_visible\(KB\)| |KB|Total amount of physical memory accessible to the operating system.|
|system.uptime\(Sec\)| |seconds|Duration that the system has been operational.|
|system.network.Bytes\_Received/sec \(featured metric\)| |byte/sec|Bytes received per second for active network adapters.|
|system.network.Bytes\_Sent/sec \(featured metric\)| |byte/sec|Bytes sent per second for active network adapters.|
|system.network.Bytes\_Total/sec \(featured metric\)| |byte/sec|Sum of the bytes received and sent per second.|
|system.network.Current\_Bandwidth| |bit/sec|Estimate of the network interface bandwidth.|
|system.network.Offloaded\_Connections| | |Number of IPv4 and IPv6 TCP connections currently handled by the TCP chimney offload capable network adapter.|
|system.network.Output\_Queue\_Length| | |Length of the output packet queue.|
|system.network.Packets/sec| | |Rate that packets are sent and received on the network.|
|system.network.Packets\_Outbound\_Discarded| | |Number of outbound packets that were discarded.|
|system.network.Packets\_Outbound\_Errors| | |Number of outbound packets that could not be sent becuase of errors.|
|system.network.Packets\_Received/sec| | |Rate that packets are received.|
|system.network.Packets\_Received\_Discarded| | |Number of inbound packets that were discarded.|
|system.network.Packets\_Received\_Errors| | |Number of inbound packets that could not be sent because of errors.|
|system.network.Packets\_Received\_Non-Unicast/sec| | |Rate that non-unicast \(subnet broadcast or subnet multicast packets\) are delivered to a higher-layer protocol.|
|system.network.Packets\_Received\_Unicast/sec| | |Rate that unicast \(subnet\) packets are delivered to a higher-layer protocol.|
|system.network.Packets\_Received\_Unknown| | |Number of packets that were received, but discarded, because of an unknown or unsupported protocol.|
|system.network.Packets\_Sent/sec| | |Rate that packets are sent.|
|system.network.Packets\_Sent\_Non-Unicast/sec| | |Rate that packets are requested for transmission to non-unicast \(subnet broadcast or subnet multicast\) addresses by higher-layer protocols. Includes packets that were discarded or not sent.|
|system.network.Packets\_Sent\_Unicast/sec| | |Rate that packets are requested to for transmission to subnet-unicast addresses by higher-layer protocols. Includes packets that were discarded or not sent.|
|system.network.TCP\_Active\_RSC\_Connections| | |Number of IPv4 and IPv6 TCP connections currently receiving large packets from the RSC-capable network adapter.|
|system.network.TCP\_RSC\_Average\_Packet\_Size| |byte|Average size of received packets across all TCP connections.|
|system.network.TCP\_RSC\_Coalesced\_Packets/sec| | |The large-packet receive rate across all TCP connections.|
|system.network.TCP\_RSC\_Exceptions/sec| | |The RSC exception rate for received packets across all TCP connections.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

