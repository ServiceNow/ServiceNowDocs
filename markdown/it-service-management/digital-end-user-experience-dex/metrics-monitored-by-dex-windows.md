---
title: Metrics monitored by DEX on Windows
description: Review the endpoint performance and compliance metrics that DEX collects from managed Windows devices, including collection intervals, and associated check definitions and policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/metrics-monitored-by-dex-windows.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 14
keywords: [dex metrics, windows metrics, digital end-user experience, endpoint performance monitoring, check definition, collection interval, agent policy, application metrics, device metrics, cpu usage, memory usage, disk usage, network metrics, wi-fi signal strength, battery details, bitLocker, antivirus, antimalware, bsod, system compliance, windows registry, pending updates, managed devices]
audience: administrator
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Metrics monitored by DEX on Windows

Review the endpoint performance and compliance metrics that DEX collects from managed Windows devices, including collection intervals, and associated check definitions and policies.

## Application metrics

<table id="table_windows_metrics"><thead><tr><th>

Metric Name

</th><th>

Key

</th><th>

Description

</th><th>

Sub-metrics / Output fields

</th><th>

Unit

</th><th>

Policy: Interval \(min\)

</th><th>

Check Definition Name

</th><th>

Required privileges

</th></tr></thead><tbody><tr><td>

Application version

</td><td>

version

</td><td>

Version string of the installed application. Format is vendor-defined \(for example, `5.14.2.6`\).

</td><td>

Single metric — `version` \(string\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-app-version

</td><td>

No elevated privileges required

</td></tr><tr><td>

CPU usage

</td><td>

cpu\_usage

</td><td>

Percentage of CPU consumed by all processes belonging to the target application. Point-in-time gauge sampled every 5 minutes.

</td><td>

Single metric — `cpu_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-app-cpu-usage

</td><td>

Local System Account

</td></tr><tr><td>

Crashes

</td><td>

crashes

</td><td>

Count of application crashes detected in the last 5 minutes via the Windows Event Log.

</td><td>

Single metric — `crashes` \(count per 5-min window, gauge\)

</td><td>

count

</td><td>

5

</td><td>

os.win.check-app-crashes

</td><td>

No elevated privileges required

</td></tr><tr><td>

Domain network details \(installed apps\)

</td><td>

domain\_network\_details

</td><td>

Network quality metrics for the target application's domain or domains: round-trip latency, packet loss, and jitter.

</td><td>

`latency` \(ms\); `packet_loss` \(%\); `jitter` \(ms\)

</td><td>

N/A

</td><td>

10

</td><td>

os.win.check-app-domain-network-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Domain network details \(Web apps\)

</td><td>

domain\_network\_details

</td><td>

Network latency, packet loss, and jitter for a web application domain. Same measurement as the installed-app variant.

</td><td>

`latency` \(ms\); `packet_loss` \(%\); `jitter` \(ms\)

</td><td>

milliseconds

</td><td>

10

</td><td>

os.win.check-web-app-domain-network-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Domain network route details \(installed apps\)

</td><td>

source\_details, domain\_network\_route\_details

</td><td>

Complete hop-by-hop network route from the device to the application's domain\(s\), including per-hop latency, IP addresses, and packet loss.

</td><td>

`source_details` \(device source IP/network info\); `domain_network_route_details` \(array of hops\): `hop_number`, `ip_address`, `latency` \(ms\), `packet_loss` \(%\)

</td><td>

N/A

</td><td>

30

</td><td>

os.win.check-app-domain-network-route-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Domain network route details \(Web apps\)

</td><td>

source\_details, domain\_network\_route\_details

</td><td>

Complete hop-by-hop network route from Windows device to the web application domain.

</td><td>

`source_details`; `domain_network_route_details` array

</td><td>

milliseconds

</td><td>

30

</td><td>

os.win.check-web-app-domain-network-route-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Freezes

</td><td>

freezes

</td><td>

Count of application freeze \(hang\) events in the last 5 minutes per application process. Sources events from Windows Application Event Log: WER Event ID 1001 \(AppHangTransient\) and Application Hang Event ID 1002.**Note:** The metric collects data only from apps that report freeze events to the Windows Event Log. Apps that don't use Windows Error Reporting can't surface freeze data.

</td><td>

Single metric — `freezes` \(count per 5-min window\) per app+version

</td><td>

count

</td><td>

5

</td><td>

os.win.check-app-freezes

</td><td>

No elevated privileges required

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_network\_bytes

</td><td>

Incoming network bytes per second for a specific application, aggregated across IPv4 and IPv6 network connections.

</td><td>

Single metric — `incoming_network_bytes` \(bytes/second, gauge\) per application

</td><td>

Bps

</td><td>

N/A

</td><td>

os.win.check-app-incoming-network-bytes

</td><td>

Local System Account

</td></tr><tr><td>

Installed Apps Version

</td><td>

version

</td><td>

Fetches all the latest version of the applications.

</td><td>

Per installed application: application name and version; delivered as change sets \(`entries_to_add`, `entries_to_remove`\).

</td><td>

N/A

</td><td>

1,440

</td><td>

os.all.check-installed-apps-version

</td><td>

No elevated privileges required

</td></tr><tr><td>

IO usage \(read\)

</td><td>

io\_usage\_read

</td><td>

Bytes read per second from disk by all processes of the target application. Two-sample delta calculation.

</td><td>

Single metric — `io_usage_read` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.win.check-app-io-usage-read

</td><td>

Local System Account

</td></tr><tr><td>

IO usage \(write\)

</td><td>

io\_usage\_write

</td><td>

Bytes written per second to disk by all processes of the target application.

</td><td>

Single metric — `io_usage_write` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.win.check-app-io-usage-write

</td><td>

Local System Account

</td></tr><tr><td>

Is installed

</td><td>

is\_installed

</td><td>

Boolean indicating whether the target application is installed on the device.

</td><td>

Single metric — `is_installed` \(boolean, gauge\)

</td><td>

Boolean

</td><td>

N/A

</td><td>

os.win.check-app-is-installed

</td><td>

No elevated privileges required

</td></tr><tr><td>

Is running

</td><td>

is\_running

</td><td>

Boolean indicating whether at least one process of the target application is currently running.

</td><td>

Single metric — `is_running` \(boolean, gauge\)

</td><td>

Boolean

</td><td>

5

</td><td>

os.win.check-app-is-running

</td><td>

Local System Account

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

Unix timestamp \(milliseconds\) of the last time the application process was observed running.

</td><td>

Single metric — `last_access_time` \(milliseconds since epoch\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.win.check-app-last-access-time

</td><td>

Local System Account

</td></tr><tr><td>

Last updated

</td><td>

last\_updated

</td><td>

Unix timestamp \(seconds\) of the most recent application update installation.

</td><td>

Single metric — `last_updated` \(Unix timestamp in seconds\)

</td><td>

seconds

</td><td>

N/A

</td><td>

os.win.check-app-last-updated

</td><td>

No elevated privileges required

</td></tr><tr><td>

Listening ports

</td><td>

listening\_ports

</td><td>

List of TCP and UDP port numbers on which the application is actively listening.

</td><td>

Single metric — `listening_ports` \(array of integers\)

</td><td>

N/A

</td><td>

N/A

</td><td>

os.win.check-app-listening-ports

</td><td>

No elevated privileges required

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_network\_bytes

</td><td>

Outgoing network bytes per second for a specific application across IPv4 and IPv6 networks.

</td><td>

Single metric — `outgoing_network_bytes` \(bytes/second, gauge\) per application

</td><td>

Bps

</td><td>

N/A

</td><td>

os.win.check-app-outgoing-network-bytes

</td><td>

Local System Account

</td></tr><tr><td>

RAM usage

</td><td>

memory\_usage

</td><td>

Percentage of physical RAM consumed by all processes of the target application relative to total system RAM.

</td><td>

Single metric — `memory_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-app-memory-usage

</td><td>

Local System Account

</td></tr><tr><td>

SCCM

</td><td>

sccm\_metrics

</td><td>

Application-specific metrics for Microsoft Configuration Manager \(MCM\), including SCCM agent status, last policy refresh, deployment status, and other SCCM-specific data.

</td><td>

`agent_status`; `last_policy_request`; `last_scan_time`; `deployment_status`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-app-sccm

</td><td>

Local system account

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

Continuous running time of each application process in milliseconds since it was last started.

</td><td>

Single metric — `uptime` \(milliseconds, gauge\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.win.check-app-uptime

</td><td>

Local System Account

</td></tr><tr><td>

Zscaler service status

</td><td>

zscaler\_service\_status

</td><td>

Fetches the Zscaler service status information for the following services: ZPA, ZIA, and ZDX, with the type parameter set to "latest". Additionally, returns whether the ZPA service status is "connected" for the type set to "historical".

</td><td>

Per-service status for ZPA, ZIA, ZDX \(latest\); ZPA connected status \(historical\).

</td><td>

N/A

</td><td>

5

</td><td>

os.win.check-app-zscaler-service-status

</td><td>

No elevated privileges required

</td></tr></tbody>
</table>## Device metrics

<table id="table_pq1_3cj_sjc"><thead><tr><th>

Metric Name

</th><th>

Key

</th><th>

Description

</th><th>

Sub-metrics / Output fields

</th><th>

Unit

</th><th>

Policy: Interval \(min\)

</th><th>

Check Definition Name

</th><th>

Required privileges

</th></tr></thead><tbody><tr><td>

Admin users

</td><td>

admin\_users

</td><td>

List of local user accounts with administrator-level privileges on the device. Snapshot only.

</td><td>

`admin_users` \(array\): `username` \(string\), `uid` \(integer\)

</td><td>

N/A

</td><td>

N/A

</td><td>

os.win.check-system-admin-users

</td><td>

No elevated privileges required

</td></tr><tr><td>

Antimalware details

</td><td>

antimalware\_details

</td><td>

Antimalware software details including product name, version, enabled status, and definition update date.

</td><td>

`product_name`; `version`; `enabled`; `definition_date`; `am_running_mode`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-antimalware-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Antivirus enabled

</td><td>

antivirus\_enabled

</td><td>

Boolean status indicating whether an antivirus product is registered and active in Windows Security Center.

</td><td>

`name` \(AV product\); `enabled` \(boolean\); `up_to_date` \(boolean\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-antivirus-enabled

</td><td>

No elevated privileges required

</td></tr><tr><td>

Battery charge percentage

</td><td>

battery\_charge\_percentage

</td><td>

Current battery charge percentage on the Windows device as an integer.

</td><td>

Single metric — `battery_charge_percentage` \(integer %, gauge\) with `battery_id` attribute

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-battery-charge-percentage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Battery details

</td><td>

battery\_details

</td><td>

Comprehensive battery health snapshot including charge percentage, estimated runtime, battery status, health condition, chemistry, cycle count, design and full-charge capacity, serial number, design voltage, and installed batteries count.

</td><td>

`charge_percentage`; `estimated_runtime`; `battery_status`; `condition`; `health`; `design_voltage`; `chemistry`; `cycle_count`; `serial_number`; `designed_capacity` \(mWh\); `full_charge_capacity` \(mWh\); `maximum_capacity` \(%\); `installed_batteries` \(count\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-battery-details

</td><td>

Local System Account

</td></tr><tr><td>

BIOS details

</td><td>

bios\_details

</td><td>

BIOS firmware details for the Windows device including BIOS version, manufacturer, release date, and BIOS mode.

</td><td>

`bios_version`; `manufacturer`; `release_date`; `serial_number`; `bios_mode` \(UEFI/Legacy\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-bios-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Bitlocker details

</td><td>

bitlocker\_details

</td><td>

BitLocker encryption status per volume including protection status, encryption method, and key protector type.

</td><td>

Per volume: `volume_type`; `mount_point`; `encryption_percentage`; `protection_status`; `lock_status`; `encryption_method`; `key_protector`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-bitlocker-details

</td><td>

Local System Account

</td></tr><tr><td>

BSOD \(count\) &amp; cause

</td><td>

bsod\_details

</td><td>

Count of Windows BSOD \(Blue Screen of Death\) events in the last 30 days from the Windows Event Log, plus per-event details: cause/error code, event ID, severity level, and timestamp.

</td><td>

`bsod_count` \(count in last 30 days\); per event: `cause`, `event_id`, `level`, `time_created`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-bsod

</td><td>

No elevated privileges required

</td></tr><tr><td>

CPU details

</td><td>

cpu\_details

</td><td>

Static CPU hardware details: processor name/model, architecture, physical core count, logical processor count, device ID, and processor ID.

</td><td>

`name`; `architecture`; `number_of_cores`; `number_of_logical_processors`; `device_id`; `processor_id`; `manufacturer`; `current_clock_speed` \(MHz\); `max_clock_speed` \(MHz\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-cpu-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

CPU performance details

</td><td>

cpu\_performance\_details

</td><td>

CPU performance counter data including CPU user time percentage.

</td><td>

`cpu_user_time` \(% User Time, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-cpu-performance-details

</td><td>

Local System Account

</td></tr><tr><td>

CPU usage

</td><td>

cpu\_usage

</td><td>

Overall device CPU utilization percentage across all cores. Collected via `typeperf` performance counter.

</td><td>

Single metric — `cpu_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-cpu-usage

</td><td>

Local System Account

</td></tr><tr><td>

Device crashes

</td><td>

device\_crashes

</td><td>

Count of device-level crashes \(BSODs, kernel events\) on Windows within the 5-minute collection window.

</td><td>

Single metric — `device_crashes` \(count per 5-min window, gauge\)

</td><td>

count

</td><td>

5

</td><td>

os.win.check-system-crashes

</td><td>

No elevated privileges required

</td></tr><tr><td>

Device details

</td><td>

device\_details

</td><td>

Hardware device inventory snapshot: chassis type, description, model, serial number, and processor ID.

</td><td>

`chassis_type`; `description`; `model`; `serial_number`; `processor_id`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-device-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Device events

</td><td>

device\_events

</td><td>

Device-level events during a specified time interval on Windows. Captures `last_boot` \(Unix timestamp if reboot occurred in interval\) and `logged_in_users` \(list of user logins in interval\).

</td><td>

`last_boot` \(Unix timestamp or empty\); `logged_in_users` \(array of user login objects\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-device-events

</td><td>

Local System Account

</td></tr><tr><td>

Disk available

</td><td>

disk\_available

</td><td>

Gets the available disk space in GB.

</td><td>

Single metric — `disk_available` \(available disk space in GB, number\).

</td><td>

GB

</td><td>

5

</td><td>

os.win.check-system-disk-available

</td><td>

Local System Account

</td></tr><tr><td>

Disk details

</td><td>

disk\_details

</td><td>

Per-disk snapshot of total, free, and used space plus disk performance counters: `disk_reads_per_sec`, `disk_writes_per_sec`, and `avg_disk_queue_length`.

</td><td>

`total_space` \(bytes\); `free_space` \(bytes\); `used_space` \(bytes\); `disk_reads_per_sec`; `disk_writes_per_sec`; `avg_disk_queue_length`; `avg_disk_sec_per_read`; `avg_disk_sec_per_write`; `avg_disk_sec_per_transfer`

</td><td>

N/A

</td><td>

5

</td><td>

os.win.check-system-disk-details

</td><td>

Local System Account

</td></tr><tr><td>

Disk IO usage \(read\)

</td><td>

io\_usage\_read

</td><td>

Device-wide disk read throughput in bytes per second across all disks.

</td><td>

Single metric — `io_usage_read` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.win.check-system-disk-io-usage-read

</td><td>

Local System Account

</td></tr><tr><td>

Disk IO usage \(write\)

</td><td>

io\_usage\_write

</td><td>

Device-wide disk write throughput in bytes per second.

</td><td>

Single metric — `io_usage_write` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.win.check-system-disk-io-usage-write

</td><td>

Local System Account

</td></tr><tr><td>

Disk usage\*

</td><td>

disk\_usage

</td><td>

Percentage of primary disk space used.

</td><td>

Single metric — `disk_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-disk-usage

</td><td>

Local System Account

</td></tr><tr><td>

Energy consumption

</td><td>

energy\_consumption

</td><td>

Energy consumed by the device over a measurement period in milliwatt-hours. Cumulative energy metric.

</td><td>

Single metric — `energy_consumption` \(mWh, gauge\) with `battery_id` attribute

</td><td>

mWh

</td><td>

5

</td><td>

os.win.check-system-energy-consumption

</td><td>

Local system account

</td></tr><tr><td>

Firewall enabled

</td><td>

firewall\_enabled

</td><td>

Boolean status of the Windows OS firewall. Returns a single state value indicating whether the firewall is enabled.

</td><td>

`firewall_enabled` \(boolean\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-firewall-enabled

</td><td>

No elevated privileges required

</td></tr><tr><td>

GPU Usage Details

</td><td>

gpu\_usage,gpu\_vram\_usage

</td><td>

Checks GPU Usage percentage and GPU VRAM Usage in bytes.

</td><td>

`gpu_usage` \(3D engine utilization %, 0–100\); `gpu_vram_usage` \(local adapter memory usage, bytes\)

</td><td>

gpu\_usage: percentage; gpu\_vram\_usage: bytes

</td><td>

5

</td><td>

os.win.check-system-gpu-usage-details

</td><td>

Local System Account

</td></tr><tr><td>

Hard drive status

</td><td>

hard\_drive\_status

</td><td>

Physical disk drive inventory and health status including disk number, name, status, description, interface type, manufacturer, media loaded, media type, model, size, serial number, partition count, and partition details.

</td><td>

`drive_details` \(array\): `disk_number`; `name`; `status`; `description`; `interface_type`; `manufacturer`; `media_loaded`; `media_type`; `model`; `size`; `serial_number`; `partitions` `partition_details` \(array\): `name`; `partition_number`; `drive_letter`; `partition_size`; `partition_type`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-hard-drive-status

</td><td>

Local System Account

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_bytes

</td><td>

Total incoming network bytes per second aggregated across all active network interfaces on the device.

</td><td>

Single metric — `incoming_bytes` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

N/A

</td><td>

os.win.check-system-net-bytes-incoming

</td><td>

Local System Account

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

Timestamp of the last time the Windows device was accessed by a user, based on lock/unlock state.**Note:** The check enables event capturing on first run, so initial collection may return an error.

</td><td>

Single metric — `last_access_time` \(timestamp of last lock/unlock\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-last-access-time

</td><td>

Local System Account

</td></tr><tr><td>

List executables

</td><td>

list\_executables

</td><td>

Inventory of all `.exe` executable files present on the Windows device.

</td><td>

Per executable: `name`; `path`; `version`; `size`; `last_modified`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-executables

</td><td>

Local System Account

</td></tr><tr><td>

Logged-in users

</td><td>

logged\_in

</td><td>

List of users currently logged into the device including username and uid.

</td><td>

`logged_in` \(array\): `user`; `uid`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-logged-in-users

</td><td>

Local System Account

</td></tr><tr><td>

Memory details

</td><td>

memory\_details

</td><td>

Comprehensive memory snapshot including physical and virtual memory totals, available, and used \(bytes\); memory usage percentage; virtual memory usage percentage; page file size and usage percentage; and pages/sec performance counter.

</td><td>

`physical_memory_total`; `physical_memory_available`; `physical_memory_usage`; `memory_usage` \(%\); `virtual_memory_total`; `virtual_memory_available`; `virtual_memory_usage`; `memory_pages_per_sec`; `page_file_usage` \(%\); `total_page_file_size`

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-memory-details

</td><td>

Local System Account

</td></tr><tr><td>

Memory modules

</td><td>

memory\_modules

</td><td>

Physical RAM module details including capacity, speed, manufacturer, part number, and slot location.

</td><td>

Per module: `capacity`; `speed` \(MHz\); `manufacturer`; `part_number`; `slot`; `form_factor`

</td><td>

N/A

</td><td>

N/A

</td><td>

os.win.check-system-memory-modules

</td><td>

No elevated privileges required

</td></tr><tr><td>

Network adapter details

</td><td>

network\_adapter\_details

</td><td>

Details of all network adapters on the Windows device. On-demand collection only.

</td><td>

`name`; `interface_description`; `status`; `mac_address`; `link_speed`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-network-adapter-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Network connection profiles

</td><td>

network\_connection\_profiles

</td><td>

Network connection profile details for the Windows device, including network type \(public/private/domain\), which can be used to infer VPN status.

</td><td>

`network_type` \(Public/Private/Domain\); `interface_name`; `connected` \(boolean\)

</td><td>

Boolean

</td><td>

30

</td><td>

os.win.check-system-network-connection-profiles

</td><td>

No elevated privileges required

</td></tr><tr><td>

Network connectivity details

</td><td>

network\_details

</td><td>

Complete network adapter snapshot for both Wi-Fi and Ethernet interfaces.

</td><td>

Ethernet: `name`; `interface_description`; `driver_version`; `status`; `link_speed`; `mac_address`; `media_type`Wi-Fi: `ssid`; `bssid`; `radio_type`; `authentication`; `channel`; `receive_rate`; `transmit_rate`; `signal`; `profile`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-network-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

OS details

</td><td>

os\_details

</td><td>

Operating system inventory snapshot including name, version, platform, architecture, install date, locale, build number, build type, service pack versions, serial number, and system directory.

</td><td>

`name`; `version`; `platform`; `architecture`; `install_date`; `locale`; `status`; `build_number`; `build_type`; `service_pack_major_version`; `service_pack_minor_version`; `serial_number`; `system_directory`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-os-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

OS setup details

</td><td>

os\_setup\_details

</td><td>

Approximate age of the Windows OS installation. Derived from OS install date compared to the current date.

</td><td>

`os_install_date` \(timestamp\); `os_age_days` \(integer\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-os-setup-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_bytes

</td><td>

Total outgoing network bytes per second aggregated across all active network interfaces on the device.

</td><td>

Single metric — `outgoing_bytes` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

1,440

</td><td>

os.win.check-system-net-bytes-outgoing

</td><td>

Local System Account

</td></tr><tr><td>

Pending system updates

</td><td>

pending\_updates

</td><td>

List of pending Windows software updates not yet installed. Includes per-update details such as KB number, title, description, support URL, mandatory flag, uninstallable flag, download size, and reboot requirement.

</td><td>

Per update: `kb`; `title`; `description`; `support_url`; `is_mandatory`; `is_uninstallable`; `max_download_size`; `min_download_size`; `reboot_required`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-pending-updates

</td><td>

Local System Account

</td></tr><tr><td>

Peripheral device details

</td><td>

peripheral\_devices\_details

</td><td>

Inventory of connected peripheral devices \(USB, HID, etc.\) including device name, type, manufacturer, and connection status.

</td><td>

Per device: `name`; `device_id`; `type`; `status`; `manufacturer`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-peripheral-devices-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Power consumption

</td><td>

power\_consumption

</td><td>

Current device power consumption in milliwatts.**Note:** Not collected for VMs \(the check skips devices where no data is available\).

</td><td>

Single metric — `power_consumption` \(milliwatts, gauge\)

</td><td>

mW

</td><td>

5

</td><td>

os.win.check-system-power-consumption

</td><td>

Local System Account

</td></tr><tr><td>

Reboot details

</td><td>

reboot\_details

</td><td>

List of system startup \(Event ID 6005\) and shutdown \(Event ID 6006\) events with Unix timestamps from the Windows System Event Log.

</td><td>

Array of events: `id` \(6005=startup or 6006=shutdown\); `time_created` \(Unix timestamp\). `last_reboot_timestamp` is calculated from this data.

</td><td>

seconds

</td><td>

1,440

</td><td>

os.win.check-system-reboot-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

System compliance

</td><td>

system\_compliance\_details

</td><td>

Compliance rating \(percentage\) for the device based on configured compliance rules across apps and device metrics. Lists non-compliant metrics and apps.

</td><td>

`compliance_rating`; `non_compliant_apps` \(array\); `non_compliant_metrics` \(array\)

</td><td>

%

</td><td>

1,440

</td><td>

os.win.check-system-compliance-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

System time

</td><td>

time

</td><td>

Current system time as a Unix epoch timestamp in seconds \(UTC\). Used for time-drift detection and telemetry alignment.

</td><td>

Single metric — `time` \(Unix epoch seconds, gauge\)

</td><td>

seconds

</td><td>

N/A

</td><td>

os.win.check-system-time

</td><td>

No elevated privileges required

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

Continuous time in milliseconds since the last device boot.

</td><td>

Single metric — `uptime` \(milliseconds, gauge\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.win.check-system-uptime

</td><td>

No elevated privileges required

</td></tr><tr><td>

User profiles

</td><td>

user\_profiles

</td><td>

List of Windows user profiles present on the device including profile path, SID, and profile type.

</td><td>

Per profile: `sid`; `localpath`; `lastusetime`; `loaded` \(boolean\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-user-profiles

</td><td>

No elevated privileges required

</td></tr><tr><td>

Wi-Fi receive rate

</td><td>

wifi\_receive\_rate

</td><td>

Wi-Fi receive rate \(downlink speed\) in Mbps on Windows. Sourced from `netsh wlan show interfaces`.

</td><td>

Single metric — `wifi_receive_rate` \(Mbps, gauge\)

</td><td>

Mbps

</td><td>

5

</td><td>

os.win.check-system-wifi-receive-rate

</td><td>

No elevated privileges required

</td></tr><tr><td>

Wi-Fi signal strength

</td><td>

wifi\_signal\_strength

</td><td>

Wi-Fi signal strength as a percentage \(0-100%\) on Windows. Parsed from `netsh wlan show interfaces` Signal field.

</td><td>

Single metric — `wifi_signal_strength` \(percentage 0-100, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.win.check-system-wifi-signal-strength

</td><td>

No elevated privileges required

</td></tr><tr><td>

Wi-Fi transmit rate

</td><td>

wifi\_transmit\_rate

</td><td>

Wi-Fi transmit rate \(uplink speed\) in Mbps from the Windows device.

</td><td>

Single metric — `wifi_transmit_rate` \(Mbps, gauge\)

</td><td>

Mbps

</td><td>

5

</td><td>

os.win.check-system-wifi-transmit-rate

</td><td>

No elevated privileges required

</td></tr><tr><td>

Windows power plan

</td><td>

power\_plan

</td><td>

Active Windows power plan \(for example, Balanced, High Performance, Power Saver\) and its GUID.

</td><td>

`power_plan_name`; `power_plan_guid`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-power-plan

</td><td>

No elevated privileges required

</td></tr><tr><td>

Windows registry keys

</td><td>

windows\_registry

</td><td>

Windows registry key values for specified paths. Registry keys are parameterized — the specific keys queried depend on the check definition configuration.

</td><td>

Configurable per key: `key`; `name`; `data`; `type` \(REG\_SZ, REG\_DWORD, etc.\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.win.check-system-windows-registry

</td><td>

No elevated privileges required

</td></tr><tr><td>

Windows stability index

</td><td>

stability\_index

</td><td>

Windows Reliability Index score \(1-10 scale\) representing overall system stability. Higher is more stable.

</td><td>

Single metric —`stability_index` \(number 1–10, gauge, asDouble\)

</td><td>

index \(0-10\)

</td><td>

1,440

</td><td>

os.win.check-system-compliance-details

</td><td>

No elevated privileges required

</td></tr></tbody>
</table>**Note:** \* The Disk Usage metric reports storage consumption. For disk I/O throughput by process, see the Disk Usage action in [Digital End-User Experience remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-diff-ra.md).

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

