---
title: Windows default checks and policies
description: Agent Client Collector provides the following default checks and policies for Windows health monitoring.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Windows default checks and policies

Agent Client Collector provides the following default checks and policies for Windows health monitoring.

## Windows event monitoring checks

<table id="table_vbt_vyk_zcc"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage and Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

os.windows.check-event-log-count

</td><td>

Measures the Windows event log against parameter thresholds and returns a CRITICAL\\WARNING\\OK event.Provides information on the number of events that have occurred within a specified duration for a single log file and a single ID. Also indicates the filters to be applied to retrieve events for a specific single-valued windows event level and provider name.

Retrieving events from multiple log files is not supported. The number of events is provided, without details of each and every event.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the event log count matching the pattern is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the event log count matching the pattern is above the CRITICAL parameter value specified in the check parameter.
-   -l log\_file - The log file to be monitored. Name of the file is written in double quotation marks.
-   -r regex\_pattern - The regex pattern which filters out the description in the event log. Written in double quotation marks.
-   -e event level - Specifies the severity level of the event. Possible values: Information, Verbose, Critical, Warning, Error.
-   -i id - Unique event ID
-   -d duration\_hour - The duration of time, in hours, in which you want to retrieve events from the Windows event log. Decimal points can be used; for example, 30 minutes - 0.5.
-   -p provider\_name - Source of the event, written in double quotation marks.

 Usage example: `winchecks check-windows-event-log -w 5 -c 10 -e "Information" -l "Application" -d 24`

</td><td>

Check Event Log OK: The Event Log that matches the pattern is &lt;matched count&gt;

</td></tr><tr><td>

os.windows.check-event-log-details

</td><td>

Collects and filters Windows Event logs based on the `duration_hour`, `event_log_level` and `log_file` values.

 Retrieves and filters Windows event logs according to the provided parameters. It returns details about the events with CRITICAL, WARNING, or OK status, based on the specified severity level.

</td><td>

Usage:

-   -d duration\_hour - Duration \(in hours\) from the current time to filter events \(Default: 24\).
-   -e event\_log\_level - Filter the events based on the event level. Possible values are: Information, Verbose, Critical, Warning, Error. Multiple values are comma-separated \(Default: Information\). For example: Information, Warning
-   -i id - Filters events based on the specified event IDs. For multiple IDs, values are comma-separated and enclosed in double quotation marks. For example: "1257, 1001"
-   -l log\_file - Specifies the log file name to filter events. The name of the file is written in double quotation marks. Supports creating custom files and multiple values are comma-separated. \(Default: Application\). For example: "Application, System"
-   -p provider\_name - The name of the event provider, enclosed in double quotation marks.
-   -r regex\_pattern - Filters events by matching the event message with the specified pattern. Value must be enclosed in double quotation marks.
-   -s servicenow\_event\_severity - Creates a servicenow event with the value given in this parameter. Possible values are: Critical, Warning and OK.

 Usage example: `winchecks check-windows-event-log-details -d 24 -l Application -e Warning -r "*" -s Warning`

</td><td>

Check Event Log Details WARNING:

 Type: Information, Category: Application, Machine: ws19-inc0061393.LOCAL.LAB, Event\_ID: 1704, Message: Security policy in the Group policy objects has been applied successfully., TimeCreated: 10/14/2024 12:09:35 AM.

 Type: Information, Category: Application, Machine: ws19-inc0061393.LOCAL.LAB, Event\_ID: 16384, Message: Successfully scheduled Software Protection service for restart at 2124-09-20T06:25:44Z. Reason: Rules Engine, TimeCreated: 10/13/2024 11:25:44 PM.

 Type: Information, Category: Application, Machine: ws19-inc0061393.LOCAL.LAB, Event\_ID: 16394, Message: Offline downlevel migration succeeded., TimeCreated: 10/13/2024 11:24:19 PM.

 Type: Information, Category: Application, Machine: ws19-inc0061393.LOCAL.LAB, Event\_ID: 8224, Message: The VSS service is shutting down due to idle timeout., TimeCreated: 10/13/2024 11:51:36 AM.

</td></tr><tr><td>

os.windows.check-processor-queue-length

</td><td>

Measures the process queue length against thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the processor queue length count matching the pattern is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the processor queue length count matching the pattern is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-processor-queue-length -w 5 -c 10`

</td><td>

Processor Queue Length OK: The Processor Queue length is 0.00

</td></tr><tr><td>

os.windows.check-system-cpu-load

</td><td>

Checks CPU Load by using typeperf. Measures the CPU load against configured thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the CPU load count matching the pattern is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the CPU load count matching the pattern is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-cpu-load -w 85 -c 95`

</td><td>

CPU Load OK: The total CPU utilization is 26.92%

</td></tr><tr><td>

os.windows.check-system-disk

</td><td>

Measures the free physical memory against thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the event log percentage matching the pattern is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the event log percentage matching the pattern is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-disk -w 85 -c 95`

</td><td>

Disk Usage Check OK: The disk usage is %

</td></tr><tr><td>

os.windows.check-system-memory-percent

</td><td>

Collects the RAM usage. Measures the memory usage against configured thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:-   -w warning - Triggers a WARNING event if the memory use percentage matching the pattern is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the memory use percentage matching the pattern is above the CRITICAL parameter value specified in the check parameter.

Usage example: `winchecks check-windows-ram -w 85 -c 95`

</td><td>

RAM Usage OK: The total memory utilization is 84%

</td></tr><tr><td>

os.windows.check-system-process

</td><td>

Query running processes to find running processes that match the given arguments \(pattern, name, both pattern and name. At least one must be given\). Measures the running processes against configured thresholds and filters, returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -n name - Process executable name to check the process execution.
-   -p pattern - Pattern \(sub string\) to search for in the command that invoked the process. Produces valid results only if the user running the Agent owns the queried process has view permissions for the queried process.
-   -w warnover - Triggers a WARNING status if the query returns more processes than those specified by the argument.
-   -W warnunder - Triggers a WARNING status if the query returns fewer processes than those specified by the argument.
-   -c critover - Triggers a CRITICAL event if the query returns more processes than those specified by the argument.
-   -C critunder - Triggers a CRITICAL event if the query returns fewer processes than those specified by the argument.

 Usage example: `winchecks check-windows-processes -n explorer`

</td><td>

Check Process OK:

 OK Found 1 matching running processes named explorer

</td></tr><tr><td>

os.windows.check-directory

</td><td>

Verifies whether a Windows directory exists.

</td><td>

Usage: -d --directory Path to the relevant directory; use '\\' for separation.

 Usage example: `winchecks check-windows-directory -d dir_path`

</td><td>

Check Directory OK: The directory 'C:/Users/Public' exists

</td></tr><tr><td>

os.windows.check-pagefile

</td><td>

Collects the **Pagefile** usage and compares it against the WARNING and CRITICAL thresholds.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the **Pagefile** usage is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the **Pagefile** usage is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-pagefile -w 75 -c 85`

</td><td>

Check Windows Page File OK: Page file usage at 31.63%

</td></tr><tr><td>

os.windows.check-free-physical-memory

</td><td>

Measures the free physical memory against configured thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the free physical memory is under the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the free physical memory is under the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-free-physical-memory -w 10 -c 5`

</td><td>

Free Physical Memory OK: The Free Physical Memory is 20.25%

</td></tr><tr><td>

os.windows.check-free-virtual-memory

</td><td>

Measures the free virtual memory against configured thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -w warning - Triggers a WARNING event if the free virtual memory is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the free virtual memory is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-free-virtual-memory -w 10 -c 5`

</td><td>

Free Virtual Memory OK: The Free Virtual Memory is 25.66%

</td></tr><tr><td>

os.windows.check-process-cpu

</td><td>

Processes CPU usage against configured thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -p processname - Process name to collect CPU usage.
-   -w warning - Triggers a WARNING event if the CPU usage is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the CPU usage is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-process-cpu-p acc -c 95 -w 85`

</td><td>

Check Process CPU OK: Process CPU usage is 0.0000%

</td></tr><tr><td>

os.windows.check-process-memory

</td><td>

Processes memory usage against thresholds and returns a CRITICAL\\WARNING\\OK event according to the thresholds given in the accompanying parameters.

</td><td>

Usage:

-   -p processname - Process name to collect memory usage.
-   -w warning - Triggers a WARNING event if the process memory usage is above the WARNING parameter value specified in the check parameter.
-   -c critical - Triggers a CRITICAL event if the process memory usage is above the CRITICAL parameter value specified in the check parameter.

 Usage example: `winchecks check-windows-process-memory-p acc -c 95 -w 85`

</td><td>

Check Process Memory OK: Process Memory usage is 0.0149%

</td></tr></tbody>
</table>## Windows metric monitoring checks

<table id="table_e11_mc1_ktb"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage and Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

os.windows.check-processor-queue-length

</td><td>

Measures the processor queue length.

</td><td>

Usage: -s scheme - Replaces output's hostname + process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-processor-queue-length --scheme hostname.proc`

</td><td>

win2019-dc-64bit.cpu.queuelength 0.00 1645371109

</td></tr><tr><td>

os.windows.check-system-cpu-load

</td><td>

Collects average CPU load per second.

</td><td>

Usage: -s scheme - Replaces output's hostname + process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-cpu-load -scheme hostname.proc`

</td><td>

win2019-dc-64bit.cpu.loadavgsec 15.07 1645371561

</td></tr><tr><td>

os.windows.check-system-cpu

</td><td>

Collects the CPU core metric.

</td><td>

Usage: -s , scheme Replaces output's hostname+process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-cpu -scheme hostname.proc`

</td><td>

win2019-dc-64bit.cpu.cpu0.cores 2 1645371681

</td></tr><tr><td>

os.windows.check-system-disk-usage

</td><td>

Collects the following disk usage metrics usage:

-   total in GB
-   usage in GB
-   avail in GB
-   used percentage

</td><td>

Usage:

-   -i , ignore\_mnt: Comma separated list of mount points to ignore \(:C\)
-   -I, include\_mnt: Comma separated list of mount points to include.
-   —scheme, scheme: Replaces output's hostname+process with the given value \(example: hostname.process\).

 Usage example: `command: winchecks metric-windows-disk-usage-scheme hostname.proc`

</td><td>

win2019-dc-64bit.disk\_usage.disk\_C.total\(GB\) 99.40 1645371774

 win2019-dc-64bit.disk\_usage.disk\_C.used\(GB\) 50.72 1645371774

 win2019-dc-64bit.disk\_usage.disk\_C.avail\(GB\) 48.68 1645371774

 win2019-dc-64bit.disk\_usage.disk\_C.used\_percentage 51.02 1645371774

</td></tr><tr><td>

os.windows.check-system-memory-percent

</td><td>

Collects RAM percentage usage, Free Physical Memory percentage and Free Virtual Memory percentage.

</td><td>

Usage: -s, scheme - Replaces output's hostname+process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-disk-usage-scheme hostname.proc`

</td><td>

win2019-dc-64bit.mem.free\_physical\_percentage 13.30 1645371856

 win2019-dc-64bit.mem.free\_virtual\_percentage 13.93 1645371856

 win2019-dc-64bit.ram.usage\_percentage 86.07 1645371856

</td></tr><tr><td>

os.windows.check-system-network

</td><td>

Collects the following active network adapter metrics:-   Total bytes per sec
-   Packets/sec
-   Packets Received per sec
-   Packets Sent per sec
-   Current Bandwidth
-   Bytes Received per sec
-   Packets Received Unicast per sec
-   Packets Received Non-Unicast per sec
-   Packets Received Discarded
-   Packets ReceivedErrors
-   Packets Received Unknown
-   Bytes sent per sec
-   Packets sent unicast per sec
-   Packets sent non-unicast per sec
-   Packets outbound discarded
-   Packets outbound errors
-   Output queue length
-   Offloaded connections
-   TCP Active RSC Connections
-   TCP RSC Coalesced Packets per sec
-   TCP RSC Exceptions per sec
-   TCP RSC Average Packet Size


</td><td>

Usage: -s scheme: Replaces output's hostname + process with the given value \(example: hostname.process\)

 Usage name: `command: winchecks metric-windows-network --scheme hostname.proc`

</td><td>

win2019-dc-64bit.system.network.Network\_Interface\(Intel\[R\]\_82574L\_Gigabit\_Network\_Connection\).&lt;metric name&gt;&lt;metric value&gt;Bytes\_Total/sec 98742.67 1645372042

 For example: win2019-dc-64bit.system.network.Network\_Interface\(Intel\[R\]\_82574L\_Gigabit\_Network\_Connection\).Bytes\_Total/sec 98742.67 1645372042

</td></tr><tr><td>

os.windows.check-system-uptime

</td><td>

Collects system uptime.

</td><td>

Usage: -s, scheme - Replaces output's hostname+process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-uptime --scheme hostname.proc`

</td><td>

win2019-dc-64bit.system.uptime\(sec\) 4614142.06 1645372124

</td></tr><tr><td>

os.windows.check-system-disk

</td><td>

Collects the following disk metrics:-   AvgDiskSecPerRead
-   AvgDiskSecPerWrite
-   DiskReadBytesPerSec
-   DiskWriteBytesPerSec

</td><td>

Usage:

 -   -i, ignore\_mnt - Comma separated list of mount points to ignore \(:C\)
-   -I, include\_mnt - Comma separated list of mount points to include.
-   —scheme, scheme - Replaces output's hostname+process with the given value \(example: hostname.process\).

 Usage example: `command: winchecks metric-windows-disk`

</td><td>

win2019-dc-64bit.disk.\_total.AvgDisksec/Read 0.000000 1645372198

 win2019-dc-64bit.disk.\_total.AvgDisksec/Write 0.000608 1645372198

 win2019-dc-64bit.disk.\_total.DiskReadBytes/sec 0.000000 1645372198

 win2019-dc-64bit.disk.\_total.DiskWriteBytes/sec 34941.692255 1645372198

 win2019-dc-64bit.disk.C.AvgDisksec/Read 0.000000 1645372200

 win2019-dc-64bit.disk.C.AvgDisksec/Write 0.000000 1645372200

 win2019-dc-64bit.disk.C.DiskReadBytes/sec 0.000000 1645372200

 win2019-dc-64bit.disk.C.DiskWriteBytes/sec 0.000000 1645372200

</td></tr><tr><td>

os.windows.check-system-memory

</td><td>

Collects the following disk metrics:-   FreePhysicalMemory
-   TotalPhysicalMemory
-   FreeVirtualMemory
-   TotalVirtualMemorySize
-   AvailableMemory
-   TotalVisibleMemorySize

</td><td>

Usage: -s, scheme - Replaces output's hostname+process with the given value \(example: hostname.process\)

 Usage example: `command: winchecks metric-windows-memory --scheme hostname.proc`

</td><td>

win2019-dc-64bit.mem.free\_physical\(KB\) 1175440.00 1645372274

 win2019-dc-64bit.mem.total\_physical\(KB\) 8588898304.00 1645372274

 win2019-dc-64bit.mem.free\_virtual\(KB\) 1747636.00 1645372274

 win2019-dc-64bit.mem.total\_virtual\(KB\) 12263156.00 1645372274

 win2019-dc-64bit.mem.available\(KB\) 1202032640.00 1645372274

 win2019-dc-64bit.mem.total\_visible\(KB\) 8387596.00 1645372274

</td></tr><tr><td>

os.windows.check-process-status

</td><td>

Collects windows process status with CPU and memory data used by the process.

</td><td>

Usage:

 -   -n, process - Process name to collect status metric.
-   —scheme, scheme - Replaces output's hostname+process with the given value \(example: hostname.process\).

</td><td>

win2019-dc-64bit.Process.Status 67 1645372421

 win2019-dc-64bit.Process.CpuPercent 0 1645372421

 win2019-dc-64bit.Process.Memory\(KB\) 1226444 1645372421

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

