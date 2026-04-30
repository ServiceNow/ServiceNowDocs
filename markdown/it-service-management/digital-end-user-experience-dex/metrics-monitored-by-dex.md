---
title: Metrics monitored by DEX
description: Find out what endpoint performance and compliance metrics are monitored by DEX, as well as the frequency of data collection and the related check definitions and policies.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-09-09"
reading_time_minutes: 10
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Metrics monitored by DEX

Find out what endpoint performance and compliance metrics are monitored by DEX, as well as the frequency of data collection and the related check definitions and policies.

## macOS metrics

<table id="table_fpf_wg4_3hc"><thead><tr><th>

Metric Name

</th><th>

Key

</th><th>

Unit

</th><th>

Check Definition Name

</th><th>

Policy: Check Instance

</th><th>

Policy: Interval \(in min\)

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="7">

Application

</td></tr><tr><td>

Application version

</td><td>

appVersion

</td><td>

N/A

</td><td>

os.mac.check-app-version

</td><td>

 

</td><td>

 

</td><td>

Gets the version of the application.

</td></tr><tr><td>

CPU Usage

</td><td>

cpu\_usage

</td><td>

%

</td><td>

os.mac.check-app-cpu-usage

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the CPU usage of the application.

</td></tr><tr><td>

Crashes

</td><td>

crashes

</td><td>

count

</td><td>

os.mac.check-app-crashes

</td><td>

 

</td><td>

 

</td><td>

Fetches number of the application crashes and crash details.

</td></tr><tr><td>

Freezes

</td><td>

freezes

</td><td>

count

</td><td>

os.mac.check-app-freezes

</td><td>

 

</td><td>

 

</td><td>

Gets umber of the applications freezes.

</td></tr><tr><td>

IO Usage \(Read\)

</td><td>

io\_usage\_read

</td><td>

Bps

</td><td>

os.mac.check-app-io-usage-read

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the Read IO usage of the application.

</td></tr><tr><td>

IO Usage \(Write\)

</td><td>

io\_usage\_write

</td><td>

Bps

</td><td>

os.mac.check-app-io-usage-write

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the Write IO usage of the application.

</td></tr><tr><td>

Is Installed

</td><td>

is\_installed

</td><td>

N/A

</td><td>

os.mac.check-app-is-installed

</td><td>

 

</td><td>

 

</td><td>

Checks whether the application is installed.

</td></tr><tr><td>

Is Running

</td><td>

is\_running

</td><td>

Boolean

</td><td>

os.mac.check-app-is-running

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks whether the application is running.

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

msec

</td><td>

os.mac.check-app-last-access-time

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the last time that the application was running.**Note:** Data is available only for the past 7 days.

</td></tr><tr><td>

Last updated

</td><td>

last\_updated

</td><td>

N/A

</td><td>

os.mac.check-app-last-updated

</td><td>

 

</td><td>

 

</td><td>

Fetches the time that the last application update was installed.

</td></tr><tr><td>

Listening ports

</td><td>

listening\_ports

</td><td>

N/A

</td><td>

os.mac.check-app-listening-ports

</td><td>

 

</td><td>

 

</td><td>

Gets the port numbers that are open and listening for this app.

</td></tr><tr><td>

Zscaler service status

</td><td>

zscaler\_service\_status

</td><td>

Boolean

</td><td>

os.mac.check-app-zscaler-service-status

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Fetches the Zscaler service status information for ZPA, ZIA, and ZDX, with the type parameter set to latest. Additionally, returns whether the ZPA service status is connected for the type set to historical.

</td></tr><tr><td>

Network Latency

</td><td>

network\_latency

</td><td>

msec

</td><td>

os.mac.check-app-domain-network-latency

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the application domain network latency.

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

msec

</td><td>

os.mac.check-app-uptime

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the application uptime.

</td></tr><tr><td class="sub-head" colspan="7">

Device

</td></tr><tr><td>

Battery Charge Percentage

</td><td>

battery\_charge\_percentage

</td><td>

%

</td><td>

os.mac.check-system-battery-charge-percentage

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the device battery charge percentage.

</td></tr><tr><td>

Battery Details

</td><td>

battery\_details

</td><td>

N/A

</td><td>

os.mac.check-system-battery-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the device battery details.

</td></tr><tr><td>

Battery utilization

</td><td>

battery\_status

</td><td>

N/A

</td><td>

os.mac.check-system-battery-status

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Shows the percent of battery that is available on the device.

</td></tr><tr><td>

Clear cache

</td><td>

clear\_app\_cache

</td><td>

N/A

</td><td>

os.mac.action-clear-app-cache

</td><td>

 

</td><td>

 

</td><td>

Deletes the path passed as parameter for the check def.

</td></tr><tr><td>

CPU Details

</td><td>

cpu\_details

</td><td>

N/A

</td><td>

os.mac.check-system-cpu-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the device CPU model, processors, and architecture.

</td></tr><tr><td>

CPU Usage

</td><td>

cpu\_usage

</td><td>

%

</td><td>

os.mac.check-system-cpu-usage

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the CPU usage.

</td></tr><tr><td>

Device Crashes

</td><td>

crashes

</td><td>

count

</td><td>

os.mac.check-system-crashes

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the device crashes details.

</td></tr><tr><td>

Device Details

</td><td>

device\_details

</td><td>

N/A

</td><td>

os.mac.check-system-device-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the model, serial number, and a type of the device.

</td></tr><tr><td>

Device Events

</td><td>

device\_events

</td><td>

N/A

</td><td>

os.mac.check-system-device-events

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Fetches the details of events that occurred on the device during the specified time interval. \(last\_boot,logged\_in\_users,softwares\_installed,softwares\_updated,users\_added,passwords\_reset\)

</td></tr><tr><td>

Disk Details

</td><td>

disk\_details

</td><td>

N/A

</td><td>

os.mac.check-system-disk-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the details of the device disk.

</td></tr><tr><td>

Disk IO Usage \(Read\)

</td><td>

io\_usage\_read

</td><td>

Bps

</td><td>

os.mac.check-system-disk-io-usage-read

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Checks the disk bytes read per second.

</td></tr><tr><td>

Disk IO Usage \(Write\)

</td><td>

io\_usage\_write

</td><td>

Bps

</td><td>

os.mac.check-system-disk-io-usage-write

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Checks the disk bytes written per second.

</td></tr><tr><td>

Disk Usage

</td><td>

disk\_usage

</td><td>

%

</td><td>

os.mac.check-system-disk-usage

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the disk used space percentage.

</td></tr><tr><td>

Energy Consumption

</td><td>

energy\_consumption

</td><td>

mWh

</td><td>

os.mac.check-system-energy-consumption

</td><td>

 

</td><td>

 

</td><td>

Gets energy consumed by the device in the following 5 mins.

</td></tr><tr><td>

Execute Jamf policy

</td><td>

policy\_id

</td><td>

N/A

</td><td>

os.mac.action-execute-jamf-policy

</td><td>

 

</td><td>

 

</td><td>

Executes the Jamf policy on the end-user device.

</td></tr><tr><td>

Firewall enabled

</td><td>

firewall\_enabled

</td><td>

N/A

</td><td>

os.mac.check-system-firewall-enabled

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Indicates whether the OS firewall is enabled and active.

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_bytes

</td><td>

Bps

</td><td>

os.mac.check-system-net-bytes-incoming

</td><td>

 

</td><td>

 

</td><td>

Counts the network bytes incoming across all network devices.

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

msec

</td><td>

os.mac.check-system-last-access-time

</td><td>

 

</td><td>

 

</td><td>

Fetches the last time that the device was accessed.**Note:** Works with the display on or off.

</td></tr><tr><td>

Logged-in Users

</td><td>

logged\_in

</td><td>

N/A

</td><td>

os.mac.check-system-logged-in-users

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Fetches the details of the logged-in users.

</td></tr><tr><td>

Network Connectivity Details

</td><td>

network\_details

</td><td>

N/A

</td><td>

os.mac.check-system-network-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the system network details like Wi-Fi and Ethernet.

</td></tr><tr><td>

OS Details

</td><td>

os\_details

</td><td>

N/A

</td><td>

os.mac.check-system-os-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Shows the name, version, platform, architecture, and install date for the OS.

</td></tr><tr><td>

OS Setup Details

</td><td>

os\_setup\_details

</td><td>

N/A

</td><td>

os.mac.check-system-os-setup-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Shows the approximate OS age for the device.

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_bytes

</td><td>

Bps

</td><td>

os.mac.check-system-net-bytes-outgoing

</td><td>

 

</td><td>

 

</td><td>

Counts the network bytes outgoing from this device.

</td></tr><tr><td>

Pending System Updates

</td><td>

pending\_updates

</td><td>

N/A

</td><td>

os.mac.check-system-pending-updates

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Checks for available pending updates on the device.

</td></tr><tr><td>

Power Consumption

</td><td>

power\_consumption

</td><td>

mW

</td><td>

os.mac.check-system-power-consumption

</td><td>

 

</td><td>

 

</td><td>

Gets power consumption for the device.

</td></tr><tr><td>

RAM Usage

</td><td>

memory\_usage

</td><td>

%

</td><td>

os.mac.check-app-memory-usage

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks the RAM usage on the device.

</td></tr><tr><td>

RAM Usage

</td><td>

memory\_usage

</td><td>

%

</td><td>

os.mac.check-system-memory-usage

</td><td>

os.mac.check-app-historical

</td><td>

5

</td><td>

Checks system memory utilization.

</td></tr><tr><td>

Reboot Details

</td><td>

reboot\_details

</td><td>

N/A

</td><td>

os.mac.check-system-reboot-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the reboot details for your device.

</td></tr><tr><td>

Session Details

</td><td>

tes

</td><td>

min

</td><td>

os.mac.check-system-session-details

</td><td>

os.mac.check-system-metrics-latest

</td><td>

1,440

</td><td>

Shows the total session time of the logged-in users, in minutes.

</td></tr><tr><td>

System Compliance

</td><td>

system\_compliance\_details

</td><td>

%

</td><td>

os.mac.check-system-compliance-details

</td><td>

 

</td><td>

 

</td><td>

Retrieves the system compliance details.Also, provides the list of all configured apps and metric values that are non-compliant, and calculates a compliance rating based on these metrics.

</td></tr><tr><td>

System Time

</td><td>

time

</td><td>

sec

</td><td>

os.mac.check-system-time

</td><td>

 

</td><td>

 

</td><td>

Checks the current time of the system in UTC.

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

msec

</td><td>

os.mac.check-system-uptime

</td><td>

 

</td><td>

 

</td><td>

Checks the time passed since the last boot.

</td></tr><tr><td>

VPN Details

</td><td>

vpn\_details

</td><td>

Boolean

</td><td>

os.mac.check-system-vpn-details

</td><td>

 

</td><td>

 

</td><td>

Gets the VPN details for the device.

</td></tr><tr><td>

Wi-Fi RSSI

</td><td>

wifi\_rssi

</td><td>

mW

</td><td>

os.mac.check-system-wifi-rssi

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the Wi-Fi RSSI value for your device.Received Signal Strength \(RSSI\)

</td></tr><tr><td>

Wi-Fi transmit rate

</td><td>

wifi\_transmit\_rate

</td><td>

Mbps

</td><td>

os.mac.check-system-wifi-transmit-rate

</td><td>

os.mac.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the Wi-Fi transmit rate for the device.

</td></tr></tbody>
</table>## Windows metrics

<table id="table_ysw_cm4_3hc"><thead><tr><th>

Metric Name

</th><th>

Key

</th><th>

Unit

</th><th>

Check Definition Name

</th><th>

Policy: Check Instance

</th><th>

Policy: Interval \(in mins\)

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="7">

Application

</td></tr><tr><td>

Application version

</td><td>

version

</td><td>

N/A

</td><td>

os.win.check-app-version

</td><td>

 

</td><td>

 

</td><td>

Gets the application version.

</td></tr><tr><td>

CPU Usage

</td><td>

cpu\_usage

</td><td>

%

</td><td>

os.win.check-app-cpu-usage

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the application CPU usage.

</td></tr><tr><td>

Crashes

</td><td>

crashes

</td><td>

count

</td><td>

os.win.check-app-crashes

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Shows the number of times the app crashed.

</td></tr><tr><td>

Domain Network Details

</td><td>

domain\_network\_details

</td><td>

—

</td><td>

os.win.check-app-domain-network-details

</td><td>

os.win.check-web-app-dom-net-historical

</td><td>

10

</td><td>

Gets network latency, packet loss, and jitter for the installed app domain.

</td></tr><tr><td>

Domain Network Details

</td><td>

domain\_network\_details

</td><td>

msec

</td><td>

os.win.check-web-app-domain-network-details

</td><td>

 

</td><td>

 

</td><td>

Gets network latency, packet loss, and jitter for the web app domain.

</td></tr><tr><td>

Domain Network Route Details

</td><td>

source\_detailsdomain\_network\_route\_details

</td><td>

N/A

</td><td>

os.win.check-app-domain-network-route-details

</td><td>

os.win.check-app-dom-network-latest

</td><td>

30

</td><td>

Gets the complete network route details for the installed app domain.

</td></tr><tr><td>

Domain Network Route Details

</td><td>

source\_detailsdomain\_network\_route\_details

</td><td>

msec

</td><td>

os.win.check-web-app-domain-network-route-details

</td><td>

 

</td><td>

 

</td><td>

Gets the complete network route details for the web app domain.

</td></tr><tr><td>

Freezes

</td><td>

freezes

</td><td>

count

</td><td>

os.win.check-app-freezes

</td><td>

 

</td><td>

 

</td><td>

Shows the number of the application freezes.

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_network\_bytes

</td><td>

Bps

</td><td>

os.win.check-app-incoming-network-bytes

</td><td>

 

</td><td>

 

</td><td>

Gets incoming network bytes of the application for IPv4 and IPv6 networks.

</td></tr><tr><td>

IO Usage \(Read\)

</td><td>

io\_usage\_read

</td><td>

Bps

</td><td>

os.win.check-app-io-usage-read

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the application Read IO usage.

</td></tr><tr><td>

IO Usage \(Write\)

</td><td>

io\_usage\_write

</td><td>

Bps

</td><td>

os.win.check-app-io-usage-write

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the application Write IO usage.

</td></tr><tr><td>

Is Installed

</td><td>

is\_installed

</td><td>

Boolean

</td><td>

os.win.check-app-is-installed

</td><td>

 

</td><td>

 

</td><td>

Checks whether the application is installed.

</td></tr><tr><td>

Is Running

</td><td>

is\_running

</td><td>

Boolean

</td><td>

os.win.check-app-is-running

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks whether the application is running.

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

msec

</td><td>

os.win.check-app-last-access-time

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Gets the last time that the application was running.

</td></tr><tr><td>

Last updated

</td><td>

last\_updated

</td><td>

sec

</td><td>

os.win.check-app-last-updated

</td><td>

 

</td><td>

 

</td><td>

Shows the time the last application update was installed.

</td></tr><tr><td>

Listening ports

</td><td>

listening\_ports

</td><td>

N/A

</td><td>

os.win.check-app-listening-ports

</td><td>

 

</td><td>

 

</td><td>

Gets the port numbers that are open and listening for the application.

</td></tr><tr><td>

Network Latency

</td><td>

network\_latency

</td><td>

msec

</td><td>

os.win.check-app-domain-network-latency

</td><td>

 

</td><td>

 

</td><td>

Gets the network latency of application domain.

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_network\_bytes

</td><td>

Bps

</td><td>

os.win.check-app-outgoing-network-bytes

</td><td>

 

</td><td>

 

</td><td>

Gets outgoing network bytes of the application for IPv4 and IPv6 networks.

</td></tr><tr><td>

RAM Usage

</td><td>

memory\_usage

</td><td>

%

</td><td>

os.win.check-app-memory-usage

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the application RAM usage.

</td></tr><tr><td>

SCCM

</td><td>

sccm\_metrics

</td><td>

N/A

</td><td>

os.win.check-app-sccm

</td><td>

 

</td><td>

 

</td><td>

Fetches application-specific metrics for Microsoft Configuration Manager \(MCM\).

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

%

</td><td>

os.win.check-app-uptime

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the application uptime.

</td></tr><tr><td>

Zscaler service status

</td><td>

zscaler\_service\_status

</td><td>

Boolean

</td><td>

os.win.check-app-zscaler-service-status

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Fetches the Zscaler service status information for ZPA, ZIA, and ZDX, with the type parameter set to latest. Additionally, returns whether the ZPA service status is connected for the type set to historical.

</td></tr><tr><td class="sub-head" colspan="7">

Device

</td></tr><tr><td>

Admin Users

</td><td>

admin\_users

</td><td>

N/A

</td><td>

os.win.check-system-admin-users

</td><td>

 

</td><td>

 

</td><td>

Gets local user accounts with admin privileges.

</td></tr><tr><td>

Antimalware Details

</td><td>

antimalware\_details

</td><td>

N/A

</td><td>

os.win.check-system-antimalware-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the details of antimalware software on the computer.

</td></tr><tr><td>

Antivirus enabled

</td><td>

antivirus\_enabled

</td><td>

N/A

</td><td>

os.win.check-system-antivirus-enabled

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Indicates whether antivirus is enabled and active.

</td></tr><tr><td>

Battery Charge Percentage

</td><td>

battery\_charge\_percentage

</td><td>

%

</td><td>

os.win.check-system-battery-charge-percentage

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the battery charge percentage on the device.

</td></tr><tr><td>

Battery Details

</td><td>

battery\_details

</td><td>

N/A

</td><td>

os.win.check-system-battery-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

The percent of the battery that is available on the device.

</td></tr><tr><td>

Bios Details

</td><td>

bios\_details

</td><td>

N/A

</td><td>

os.win.check-system-bios-details

</td><td>

 

</td><td>

 

</td><td>

Shows the system bios details.

</td></tr><tr><td>

Bitlocker Details

</td><td>

bitlocker\_details

</td><td>

N/A

</td><td>

os.win.check-system-bitlocker-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets information about the volumes that BitLocker can protect.

</td></tr><tr><td>

BSOD \(Count\) &amp; Cause

</td><td>

bsod\_details

</td><td>

count

</td><td>

os.win.check-system-bsod

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Provides the count of the blue screens of death \(BSOD\) in the last 30 days, and the corresponding cause, id, level, and time created.

</td></tr><tr><td>

CPU Details

</td><td>

cpu\_details

</td><td>

N/A

</td><td>

os.win.check-system-cpu-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the CPU name, architecture, number of cores, number of logical processors, and device id.

</td></tr><tr><td>

CPU Performance Details

</td><td>

cpu\_performance\_details

</td><td>

%

</td><td>

os.win.check-system-cpu-performance-details

</td><td>

 

</td><td>

 

</td><td>

Gets the CPU performance details like user time.

</td></tr><tr><td>

CPU Usage

</td><td>

cpu\_usage

</td><td>

%

</td><td>

os.win.check-system-cpu-usage

</td><td>

 

</td><td>

 

</td><td>

Checks the CPU usage.

</td></tr><tr><td>

Device Crashes

</td><td>

device\_crashes

</td><td>

count

</td><td>

os.win.check-system-crashes

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the details of different crashes on the device.

</td></tr><tr><td>

Device Details

</td><td>

device\_details

</td><td>

N/A

</td><td>

os.win.check-system-device-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the device chassis type, description, model, and serial number.

</td></tr><tr><td>

Device Events

</td><td>

device\_events

</td><td>

N/A

</td><td>

os.win.check-system-device-events

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Fetches the details of events that occurred on the device during the specified time interval. \(last\_boot,logged\_in\_users\)

</td></tr><tr><td>

Disk Details

</td><td>

disk\_details

</td><td>

N/A

</td><td>

os.win.check-system-disk-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the total, free, and used space of all disks, in bytes.

</td></tr><tr><td>

Disk IO Usage \(Read\)

</td><td>

io\_usage\_read

</td><td>

Bps

</td><td>

os.win.check-system-disk-io-usage-read

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the disk IO read usage, in bytes per second.

</td></tr><tr><td>

Disk IO Usage \(Write\)

</td><td>

io\_usage\_write

</td><td>

Bps

</td><td>

os.win.check-system-disk-io-usage-write

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the disk IO write usage, in bytes per second.

</td></tr><tr><td>

Disk Usage

</td><td>

disk\_usage

</td><td>

%

</td><td>

os.win.check-system-disk-usage

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the disk used space percentage.

</td></tr><tr><td>

Energy Consumption

</td><td>

energy\_consumption

</td><td>

mWh

</td><td>

os.win.check-system-energy-consumption

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the energy consumption value of the device, in milliwatt per hour.

</td></tr><tr><td>

Firewall enabled

</td><td>

firewall\_enabled

</td><td>

N/A

</td><td>

os.win.check-system-firewall-enabled

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Indicates whether the OS firewall is enabled and active.

</td></tr><tr><td>

Get all services

</td><td>

services

</td><td>

N/A

</td><td>

os.win.check-services-data

</td><td>

 

</td><td>

 

</td><td>

Retrieves the services in the devices, included with the category of user and service.

</td></tr><tr><td>

Hard drive status

</td><td>

hard\_drive\_status

</td><td>

N/A

</td><td>

os.win.check-system-hard-drive-status

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the status of the hard drives on the device.

</td></tr><tr><td>

Incoming network bytes

</td><td>

incoming\_bytes

</td><td>

Bps

</td><td>

os.win.check-system-net-bytes-incoming

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Shows the count of network bytes incoming across all network devices.

</td></tr><tr><td>

Last access time

</td><td>

last\_access\_time

</td><td>

N/A

</td><td>

os.win.check-system-last-access-time

</td><td>

 

</td><td>

 

</td><td>

Shows the last time that the device was accessed.**Note:** Works whether the device is locked or unlocked.

Capturing of these events happens the first time that the check def is run. Initially there’s an error message because there’s no data.

</td></tr><tr><td>

List Executables

</td><td>

list\_executables

</td><td>

N/A

</td><td>

os.win.check-system-executables

</td><td>

 

</td><td>

 

</td><td>

Fetches all the executables \(\*.exe\) present on the device.

</td></tr><tr><td>

Logged-in users

</td><td>

logged\_in

</td><td>

N/A

</td><td>

os.win.check-system-logged-in-users

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the details of logged-in users.

</td></tr><tr><td>

Memory details

</td><td>

memory\_details

</td><td>

%

</td><td>

os.win.check-system-memory-details

</td><td>

 

</td><td>

 

</td><td>

Gets the system memory details like total, available, and used.

</td></tr><tr><td>

Memory modules

</td><td>

memory\_modules

</td><td>

N/A

</td><td>

os.win.check-system-memory-modules

</td><td>

 

</td><td>

 

</td><td>

Gets the memory modules details on the device.

</td></tr><tr><td>

Network Adapter Details

</td><td>

network\_adapter\_details

</td><td>

N/A

</td><td>

os.win.check-system-network-adapter-details

</td><td>

 

</td><td>

 

</td><td>

Gets the network adapter details for the device.

</td></tr><tr><td>

Network Connection Profiles

</td><td>

network\_connection\_profiles

</td><td>

Boolean

</td><td>

os.win.check-system-network-connection-profiles

</td><td>

os.win.check-system-metrics-historical

</td><td>

30

</td><td>

Gets the network connection profile details for the device.

</td></tr><tr><td>

Network Connectivity Details

</td><td>

network\_details

</td><td>

N/A

</td><td>

os.win.check-system-network-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the complete details for the system network details like Wi-Fi and Ethernet.

</td></tr><tr><td>

OS Details

</td><td>

os\_details

</td><td>

N/A

</td><td>

os.win.check-system-os-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets name, version, platform, architecture, and install date for the Windows OS.

</td></tr><tr><td>

OS Setup Details

</td><td>

os\_setup\_details

</td><td>

N/A

</td><td>

os.win.check-system-os-setup-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the approximate OS age for the device.

</td></tr><tr><td>

Outgoing network bytes

</td><td>

outgoing\_bytes

</td><td>

Bps

</td><td>

os.win.check-system-net-bytes-outgoing

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Shows the count of network bytes outgoing from this device.

</td></tr><tr><td>

Pending System Updates

</td><td>

pending\_updates

</td><td>

N/A

</td><td>

os.win.check-system-pending-updates

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Provides a list of pending updates on the device.

</td></tr><tr><td>

Peripheral device details

</td><td>

peripheral\_devices\_details

</td><td>

N/A

</td><td>

os.win.check-peripheral-devices-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the details of peripheral devices connected to the device.

</td></tr><tr><td>

Power Consumption

</td><td>

power\_consumption

</td><td>

mW

</td><td>

os.win.check-system-power-consumption

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the power consumption of the device, in milliwatts.

</td></tr><tr><td>

Reboot Details

</td><td>

reboot\_details

</td><td>

sec

</td><td>

os.win.check-system-reboot-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets the reboot duration and last reboot timestamp of the device.

</td></tr><tr><td>

System Compliance

</td><td>

system\_compliance\_details

</td><td>

%

</td><td>

os.win.check-system-compliance-details

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Retrieves the system compliance details. Provides a list of all configured apps and metric values that are non-compliant, and calculates compliance.

</td></tr><tr><td>

System Time

</td><td>

time

</td><td>

sec

</td><td>

os.win.check-system-time

</td><td>

 

</td><td>

 

</td><td>

Checks the current time of the system in UTC.

</td></tr><tr><td>

Uptime

</td><td>

uptime

</td><td>

msec

</td><td>

os.win.check-system-uptime

</td><td>

os.win.check-app-historical

</td><td>

5

</td><td>

Checks the time passed since the last boot.

</td></tr><tr><td>

User Profiles

</td><td>

user\_profiles

</td><td>

N/A

</td><td>

os.win.check-system-user-profiles

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Get the user profiles on the device.

</td></tr><tr><td>

Wi-Fi receive rate

</td><td>

wifi\_receive\_rate

</td><td>

Mbps

</td><td>

os.win.check-system-wifi-receive-rate

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the Wi-Fi receive rate for the device.

</td></tr><tr><td>

Wi-Fi signal strength

</td><td>

wifi\_signal\_strength

</td><td>

Mbps

</td><td>

os.win.check-system-wifi-signal-strength

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the Wi-Fi signal strength for the device.

</td></tr><tr><td>

Wi-Fi transmit rate

</td><td>

wifi\_transmit\_rate

</td><td>

Mbps

</td><td>

os.win.check-system-wifi-transmit-rate

</td><td>

os.win.check-system-metrics-historical

</td><td>

5

</td><td>

Gets the Wi-Fi transmit rate for the device.

</td></tr><tr><td>

Windows Power Plan

</td><td>

power\_plan

</td><td>

N/A

</td><td>

os.win.check-system-power-plan

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Gets power plan for the device.

</td></tr><tr><td>

Windows registry keys

</td><td>

windows\_registry

</td><td>

N/A

</td><td>

os.win.check-system-windows-registry

</td><td>

 

</td><td>

 

</td><td>

Gets Windows registry data.

</td></tr><tr><td>

Windows Stability Index

</td><td>

stability\_index

</td><td>

number

</td><td>

os.win.check-system-stability-index

</td><td>

os.win.check-system-metrics-latest

</td><td>

1,440

</td><td>

Provides a numerical rating that represents the overall stability of the system. \(Value: 1–10\).

</td></tr></tbody>
</table>**Parent Topic:**[DEX Application and Device Health reference](dex-console-reference.md)

