---
title: Metrics monitored by DEX on macOS
description: Review the endpoint performance and compliance metrics that DEX collects from managed macOS devices, including collection intervals, and associated check definitions and policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/metrics-monitored-by-dex-macos.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 8
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Metrics monitored by DEX on macOS

Review the endpoint performance and compliance metrics that DEX collects from managed macOS devices, including collection intervals, and associated check definitions and policies.

## Application metrics

<table id="table_mac_metrics"><thead><tr><th>

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

Required Privileges

</th></tr></thead><tbody><tr><td>

Application version

</td><td>

appVersion

</td><td>

Version string of the installed Mac application. Snapshot metric retrieved via the osquery `apps` table.

</td><td>

Single metric — `appVersion` \(string\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-app-version

</td><td>

Sudo permissions

</td></tr><tr><td>

CPU usage

</td><td>

cpu\_usage

</td><td>

Percentage of CPU consumed by the target application's processes. Point-in-time gauge sampled every 5 minutes; rounded to 2 decimal places.

</td><td>

Single metric — `cpu_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-app-cpu-usage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Crashes

</td><td>

crashes

</td><td>

Count of application crashes and crash event details. Source: osquery `crash_log` table.

</td><td>

`crashes` \(count\); `crash_details` \(array\): timestamp, process\_name, responsible, exception\_type, signal

</td><td>

count

</td><td>

5

</td><td>

os.mac.check-app-crashes

</td><td>

Sudo permissions

</td></tr><tr><td>

Freezes

</td><td>

freezes

</td><td>

Count of application freeze or hang events on the device.

</td><td>

Single metric — `freezes` \(count\) per application.

</td><td>

count

</td><td>

5

</td><td>

os.mac.check-app-freezes

</td><td>

Sudo permissions

</td></tr><tr><td>

IO usage \(read\)

</td><td>

io\_usage\_read

</td><td>

Bytes read per second from disk by application processes.

</td><td>

Single metric — `io_usage_read` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.mac.check-app-io-usage-read

</td><td>

Sudo permissions

</td></tr><tr><td>

IO usage \(write\)

</td><td>

io\_usage\_write

</td><td>

Bytes written per second to disk by application processes.

</td><td>

Single metric — `io_usage_write` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.mac.check-app-io-usage-write

</td><td>

Sudo permissions

</td></tr><tr><td>

Is installed

</td><td>

is\_installed

</td><td>

Boolean indicating whether the target application is installed on the device. Prerequisite for all other application metrics.

</td><td>

Single metric — `is_installed` \(boolean\)

</td><td>

Boolean

</td><td>

N/A

</td><td>

os.mac.check-app-is-installed

</td><td>

Sudo permissions

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

os.mac.check-app-is-running

</td><td>

Sudo permissions

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

Unix timestamp \(milliseconds\) of the last time the application was observed running. Daily snapshot.Sudo permissions are required.

**Note:** Data is available only for the past 7 days due to macOS log retention limits.

</td><td>

Single metric — `last_access_time` \(milliseconds since epoch\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.mac.check-app-last-access-time

</td><td>

Sudo permissions

</td></tr><tr><td>

Last updated

</td><td>

last\_updated

</td><td>

Timestamp of the most recent application update installation. Derived from the `mdls` command which reads file system extended attributes of the `.app` bundle.Sudo permissions are required.

</td><td>

Single metric — `last_updated` \(Unix timestamp\)

</td><td>

seconds

</td><td>

N/A

</td><td>

os.mac.check-app-last-updated

</td><td>

Sudo permissions

</td></tr><tr><td>

Listening ports

</td><td>

listening\_ports

</td><td>

List of TCP and UDP port numbers on which the application is actively listening. Latest snapshot only; not stored historically.

</td><td>

Single metric — `listening_ports` \(array of integer port numbers\)

</td><td>

N/A

</td><td>

N/A

</td><td>

os.mac.check-app-listening-ports

</td><td>

Sudo permissions

</td></tr><tr><td>

RAM usage

</td><td>

memory\_usage

</td><td>

Percentage of physical RAM consumed by the target application's processes relative to total system RAM.

</td><td>

Single metric — `memory_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-app-memory-usage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

Continuous running time of each application process in milliseconds since its last start. Derived from the `ps` command elapsed time.

</td><td>

Single metric — `uptime` \(milliseconds, gauge\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.mac.check-app-uptime

</td><td>

No elevated privileges required

</td></tr></tbody>
</table>## Device metrics

<table id="table_uc4_2bj_sjc"><thead><tr><th>

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

List of local macOS user accounts with administrator \(admin group\) privileges. Snapshot only.

</td><td>

`admin_users` \(array\): `username` \(string\), `uid` \(integer\)

</td><td>

N/A

</td><td>

N/A

</td><td>

os.mac.check-system-admin-users

</td><td>

No elevated privileges required

</td></tr><tr><td>

Battery charge percentage

</td><td>

battery\_charge\_percentage

</td><td>

Current macOS battery charge percentage from osquery `battery` table. Integer value 0-100.

</td><td>

Single metric — `battery_charge_percentage` \(integer %, gauge\) with `battery_id` attribute

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-system-battery-charge-percentage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Battery details

</td><td>

battery\_details

</td><td>

Comprehensive macOS battery health snapshot from osquery `battery` table. Includes charge percentage, health, condition, cycle count, design and full-charge capacity \(converted from mAh to mWh using design voltage\), maximum capacity percentage, and installed battery count.

</td><td>

`charge_percentage` \(%\); `health` \(Good/Moderate/Poor\); `condition`; `cycle_count`; `designed_capacity` \(mWh\); `full_charge_capacity` \(mWh\); `maximum_capacity` \(%\); `design_voltage` \(volts\); `installed_batteries` \(count\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-battery-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

CPU details

</td><td>

cpu\_details

</td><td>

macOS CPU hardware details including model name, physical processor count, logical processor count, and architecture. Daily snapshot.

</td><td>

`model`; `number_of_cores`; `number_of_logical_processors`; `architecture` \(e.g., arm64 or x86\_64\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-cpu-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

CPU usage

</td><td>

cpu\_usage

</td><td>

Aggregate CPU utilization percentage across all CPU cores on macOS. Computed as 100 minus the average idle percentage across all cores, parsed from the `top` command output.

</td><td>

Single metric — `cpu_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-system-cpu-usage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Device crashes

</td><td>

crashes

</td><td>

Count of device-level crashes \(kernel panics, system crashes\) on macOS within the 5-minute collection window.

</td><td>

Single metric — `crashes` \(count per 5-min window, gauge\)

</td><td>

count

</td><td>

5

</td><td>

os.mac.check-system-crashes

</td><td>

No elevated privileges required

</td></tr><tr><td>

Device details

</td><td>

device\_details

</td><td>

macOS hardware identity snapshot: model name, serial number, and device type via `system_profiler SPHardwareDataType`.

</td><td>

`model` \(e.g., MacBook Pro 14-inch\); `serial_number`; `device_type`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-device-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Device events

</td><td>

device\_events

</td><td>

macOS device events during a specified time interval. Captures six event types: last\_boot, logged\_in\_users, softwares\_installed, softwares\_updated, users\_added, and passwords\_reset.Sudo permissions are required.

</td><td>

`last_boot` \(timestamp\); `logged_in_users` \(array\); `softwares_installed` \(array\); `softwares_updated` \(array\); `users_added` \(array\); `passwords_reset` \(array\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-device-events

</td><td>

Sudo permissions

</td></tr><tr><td>

Disk details

</td><td>

disk\_details

</td><td>

Per-disk snapshot of total space, free space, and used space in bytes for the primary macOS disk. Data from the osquery mounts table \(path = '/'\).

</td><td>

`total_space` \(bytes\); `free_space` \(bytes\); `used_space` \(bytes\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-disk-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Disk IO usage \(read\)

</td><td>

io\_usage\_read

</td><td>

Device-wide disk read throughput in bytes per second on macOS. Two-sample delta from osquery `processes` table `disk_bytes_read`.

</td><td>

Single metric — `io_usage_read` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.mac.check-system-disk-io-usage-read

</td><td>

Sudo permissions

</td></tr><tr><td>

Disk IO usage \(write\)

</td><td>

io\_usage\_write

</td><td>

Device-wide disk write throughput in bytes per second on macOS.

</td><td>

Single metric — `io_usage_write` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

5

</td><td>

os.mac.check-system-disk-io-usage-write

</td><td>

Sudo permissions

</td></tr><tr><td>

Disk usage\*

</td><td>

disk\_usage

</td><td>

Percentage of primary disk space used on macOS, computed as `(total - free) / total * 100`.

</td><td>

Single metric — `disk_usage` \(percentage, gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-system-disk-usage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Energy consumption

</td><td>

energy\_consumption

</td><td>

Energy consumed by the macOS device over the next 5-minute window in milliwatt-hours. Measured via the macOS `powermetrics` tool.

</td><td>

Single metric — `energy_consumption` \(milliwatt-hour, gauge\) with `battery_id` attribute

</td><td>

mWh

</td><td>

5

</td><td>

os.mac.check-system-energy-consumption

</td><td>

Sudo permissions

</td></tr><tr><td>

Firewall enabled

</td><td>

firewall\_enabled

</td><td>

Boolean status of the macOS application-layer firewall \(Application Firewall / `socketfilterfw`\).

</td><td>

Single metric — `firewall_enabled` \(boolean\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-firewall-enabled

</td><td>

No elevated privileges required

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_bytes

</td><td>

Total incoming network bytes per second aggregated across all network interfaces on macOS. Two-sample delta calculation from osquery `interface_details` table.

</td><td>

Single metric — `incoming_bytes` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

N/A

</td><td>

os.mac.check-system-net-bytes-incoming

</td><td>

No elevated privileges required

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

Unix timestamp \(milliseconds\) of the last time the macOS device was physically accessed by a user, based on display activity.**Note:** Works with the display on or off.

</td><td>

Single metric — `last_access_time` \(milliseconds since epoch\)

</td><td>

milliseconds

</td><td>

1,440

</td><td>

os.mac.check-system-last-access-time

</td><td>

No elevated privileges required

</td></tr><tr><td>

Logged-in users

</td><td>

logged\_in

</td><td>

List of users currently logged into the macOS including username and uid.

</td><td>

`logged_in` \(array\): `user` \(string\); `uid` \(integer\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-logged-in-users

</td><td>

No elevated privileges required

</td></tr><tr><td>

Network connectivity details

</td><td>

network\_details

</td><td>

Full network interface snapshot for both Wi-Fi and Ethernet on macOS.

</td><td>

Wi-Fi: `name`; `ssid`; `bssid`; `channel`; `rssi` \(dBm\); `transmit_rate` \(Mbps\); `mac_address`; `state`Ethernet: `name`; `mac_address`; `link_speed`; `media`; `status`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-network-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

OS details

</td><td>

os\_details

</td><td>

macOS inventory snapshot: OS name \(for example, macOS Ventura\), version, platform \(darwin\), architecture, and install date.

</td><td>

`name`; `version`; `platform`; `architecture`; `install_date` \(timestamp\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-os-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

OS setup details

</td><td>

os\_setup\_details

</td><td>

Approximate age of the macOS installation, indicating how long the current OS has been set up on the device.

</td><td>

`os_install_date` \(timestamp\); `os_age_days` \(integer\)

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-os-setup-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_bytes

</td><td>

Total outgoing network bytes per second across all macOS network interfaces. Two-sample delta from osquery `interface_details` `outbytes` column.

</td><td>

Single metric — `outgoing_bytes` \(bytes/second, gauge\)

</td><td>

Bps

</td><td>

N/A

</td><td>

os.mac.check-system-net-bytes-outgoing

</td><td>

No elevated privileges required

</td></tr><tr><td>

Pending system updates

</td><td>

pending\_updates

</td><td>

List of available pending software updates on macOS \(both system and app store updates\).

</td><td>

Per update: `update_name`; `version`; `description`; `restart_required`

</td><td>

N/A

</td><td>

1,440

</td><td>

os.mac.check-system-pending-updates

</td><td>

No elevated privileges required

</td></tr><tr><td>

Power consumption

</td><td>

power\_consumption

</td><td>

Instantaneous power consumption of the macOS device in milliwatts via `powermetrics`.

</td><td>

Single metric — `power_consumption` \(milliwatts, gauge\)

</td><td>

mW

</td><td>

5

</td><td>

os.mac.check-system-power-consumption

</td><td>

Sudo permissions

</td></tr><tr><td>

RAM usage

</td><td>

memory\_usage

</td><td>

System-wide physical memory utilization percentage on macOS. Calculated from `vm_stat` output.

</td><td>

`memory_total` \(bytes\); `memory_available` \(bytes\); `memory_usage` \(bytes\); `memory_usage_percentage` \(gauge\)

</td><td>

%

</td><td>

5

</td><td>

os.mac.check-system-memory-usage

</td><td>

No elevated privileges required

</td></tr><tr><td>

Reboot details

</td><td>

reboot\_details

</td><td>

Last reboot timestamp for the macOS device. Calculated from osquery `system_info` uptime.

</td><td>

`last_reboot_timestamp` \(Unix timestamp in seconds\)

</td><td>

seconds

</td><td>

1,440

</td><td>

os.mac.check-system-reboot-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Session details

</td><td>

session\_details

</td><td>

Session duration in minutes for each currently logged-in user on the macOS.

</td><td>

Array of session objects: `user` \(username\); `session_time` \(minutes since login\)

</td><td>

minutes

</td><td>

1,440

</td><td>

os.mac.check-system-session-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

System compliance

</td><td>

system\_compliance\_details

</td><td>

Compliance rating \(percentage\) for the macOS device based on configured compliance rules. Lists non-compliant metrics and apps.

</td><td>

`compliance_rating` \(percentage\); `non_compliant_apps` \(array\); `non_compliant_metrics` \(array\)

</td><td>

%

</td><td>

1,440

</td><td>

os.mac.check-system-compliance-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

System time

</td><td>

time

</td><td>

Current macOS system time as Unix epoch seconds \(UTC\). Used for time-drift detection and telemetry alignment.

</td><td>

Single metric — `time` \(Unix epoch seconds, gauge\)

</td><td>

seconds

</td><td>

N/A

</td><td>

os.mac.check-system-time

</td><td>

No elevated privileges required

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

Time in milliseconds since the last device boot on macOS. Derived from osquery `system_info`.

</td><td>

Single metric — `uptime` \(milliseconds, gauge\)

</td><td>

milliseconds

</td><td>

5

</td><td>

os.mac.check-system-uptime

</td><td>

No elevated privileges required

</td></tr><tr><td>

VPN details

</td><td>

vpn\_details

</td><td>

VPN connection status on macOS as a boolean. Detected by comparing DNS search domains in the resolver versus macOS network settings.

</td><td>

`vpn_status` \(boolean\); `vpn_domains` \(array of detected VPN search domains\)

</td><td>

Boolean

</td><td>

30

</td><td>

os.mac.check-system-vpn-details

</td><td>

No elevated privileges required

</td></tr><tr><td>

Wi-Fi RSSI

</td><td>

wifi\_rssi

</td><td>

Wi-Fi RSSI \(Received Signal Strength Indicator\) in dBm from osquery `wifi_status` table. Negative integer value \(for example, -65 dBm\).

</td><td>

Single metric — `wifi_rssi` \(dBm, negative integer, gauge\)

</td><td>

dBm

</td><td>

5

</td><td>

os.mac.check-system-wifi-rssi

</td><td>

Sudo permissions

</td></tr><tr><td>

Wi-Fi transmit rate

</td><td>

wifi\_transmit\_rate

</td><td>

Wi-Fi transmit rate in Mbps on macOS from osquery `wifi_status` table.

</td><td>

Single metric — `wifi_transmit_rate` \(Mbps, gauge\)

</td><td>

Mbps

</td><td>

5

</td><td>

os.mac.check-system-wifi-transmit-rate

</td><td>

Sudo permissions

</td></tr></tbody>
</table>**Note:** \* The Disk Usage metric reports storage consumption. For disk I/O throughput by process, see the Disk Usage action in [Digital End-User Experience remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-diff-ra.md).

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

