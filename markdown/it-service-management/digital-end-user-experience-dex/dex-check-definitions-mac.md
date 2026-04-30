---
title: DEX check definitions for macOS
description: Check definitions for macOS are predetermined sets of rules and criteria that assess the performance, security, and conformance of macOS devices. These checks can cover various aspects such as CPU usage, memory usage, battery details, and firewall status.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX check definitions for macOS

Check definitions for macOS are predetermined sets of rules and criteria that assess the performance, security, and conformance of macOS devices. These checks can cover various aspects such as CPU usage, memory usage, battery details, and firewall status.

**Note:** You can configure the check definitions and associated retrievable data. Some of the listed check definitions might retrieve data that contains or is considered personal information.

## Check definitions — Application \(Metrics\)

DEX provides the following check definitions, available while the application is running, except these listed below, which remain accessible even when the application isn’t running:

-   os.mac.check-app-version
-   os.mac.check-app-is-installed
-   os.mac.check-app-last-access-time
-   os.mac.check-app-last-updated

In the check definition parameters:

-   appName = application name. For example, Webex.
-   appSysId = sys\_id of the application.
-   primaryProcess = list of primary processes for the application separated by a pipe symbol \( \| \). The first process that exists on the endpoint device is given priority. For example: Webex.app or Microsoft Teams.app \| Microsoft Teams Classic.app.

    **Note:** When determining priority based on process availability on an endpoint device, follow this logic: If the primary process for the Teams application is Microsoft Teams.app on one end-point device and it’s Microsoft Teams classic.app on another end-point device, then the process that is present on the endpoint device first is given precedence.

-   secondaryProcesses = list of secondary processes for the application separated by a pipe symbol \( \| \). For example: Cisco WebEx Start.app \| webexmtaV2.app.

<table id="table_yxf_q4d_hwb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.mac.check-app-cpu-usage

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the amount of CPU resources being used by the primary process and secondary process of the application.

.

</td></tr><tr><td>

os.mac.check-app-memory-usage

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the amount of memory resources being used by the primary process and secondary process of the application.

</td></tr><tr><td>

os.mac.check-app-listening-ports

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves the port numbers that are open and through which incoming network traffic can reach the application.

</td></tr><tr><td>

os.mac.check-app-last-updated

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the time and date of the latest application update installation.**Note:** This check definition doesn’t require the application to be in a running state.

</td></tr><tr><td>

os.mac.check-app-version

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves the version number of the application.**Note:**

-   This check definition doesn't require the application to be in a running state.
-   If an application doesn’t have a version, the check definition returns the string "unversioned" for that application.

</td></tr><tr><td>

os.mac.check-app-is-installed

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks if the application is installed or not on the device.**Note:** This check definition doesn’t require the application to be in a running state.

</td></tr><tr><td>

os.mac.check-app-is-running

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks whether the application is in a running state or not.

</td></tr><tr><td>

os.mac.check-app-uptime

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the uptime of the given application.

</td></tr><tr><td>

os.mac.check-app-last-access-time

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the most recent time when the application was executed or run.**Note:**

-   This check definition doesn’t require the application to be in a running state.
-   If the application hasn’t been run by the user within the last 7 days, the last access time is empty.

</td></tr><tr><td>

os.mac.check-app-io-usage-read

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the Read I/O \(Input/Output\) operations performed by the application's primary and secondary processes.

</td></tr><tr><td>

os.mac.check-app-io-usage-write

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the Write I/O \(Input/Output\) operations performed by the application's primary and secondary processes.

</td></tr><tr><td>

os.mac.check-app-domain-network-latency

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;
-   --domain=&lt;domain of the application&gt;

</td><td>

Fetches network latency of the application domain.

</td></tr><tr><td>

os.mac.check-app-crashes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Fetches number of crashes and crash details of the application.

</td></tr><tr><td>

os.mac.check-app-freezes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Fetches number of app freezes in the last 5 minutes and freeze details of the application.

</td></tr><tr><td>

os.mac.check-app-zscaler-service-status

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves the Zscaler service status information.

</td></tr></tbody>
</table>## Check definitions — Device \(Metrics\)

DEX provides the following types of check definitions for device.

<table id="table_wtg_ydq_rwb"><thead><tr><th>

Check definition name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.mac.check-system-cpu-usage

</td><td>

Checks the CPU utilization.

</td></tr><tr><td>

os.mac.check-system-cpu-details

</td><td>

Retrieves the CPU name, number of physical and logical cores, and architecture information.

</td></tr><tr><td>

os.mac.check-system-memory-usage

</td><td>

Checks system memory utilization.

</td></tr><tr><td>

os.mac.check-system-last-access-time

</td><td>

Checks the last time that the current device was accessed. **Note:** This check definition works on locked and unlocked devices.

</td></tr><tr><td>

os.mac.check-system-uptime

</td><td>

Checks the amount of time elapsed since the system was last booted.

</td></tr><tr><td>

os.mac.check-system-time

</td><td>

Checks the current time in Coordinated Universal Time \(UTC\) using UNIX timestamp.

</td></tr><tr><td>

os.mac.check-system-device-crashes

</td><td>

Retrieves details of different crashes on your device.**Note:** This check fetches Kernel Panics present in the device logs in the last five minutes.

</td></tr><tr><td>

os.mac.check-system-device-details

</td><td>

Retrieves the type, model, and serial number of the chassis.

</td></tr><tr><td>

os.mac.check-system-device-events

</td><td>

Retrieves the details of events that occurred on the device during the specified time interval. Events for macOS include: Last boot, logged-in users, installed software, updated software, added users, and reset passwords.

</td></tr><tr><td>

os.mac.check-system-disk-details

</td><td>

Retrieves disk details such as total space, used space, and free space in bytes.

</td></tr><tr><td>

os.mac.check-system-disk-io-usage-read

</td><td>

Retrieves disk bytes read per second.

</td></tr><tr><td>

os.mac.check-system-disk-io-usage-write

</td><td>

Retrieves disk bytes written per second.

</td></tr><tr><td>

os.mac.check-system-disk-usage

</td><td>

Retrieves the disk used space as a percentage of the total space.

</td></tr><tr><td>

os.mac.check-system-os-details

</td><td>

Retrieves the name, version, platform, architecture, and installation date of the operating system.

</td></tr><tr><td>

os.mac.check-system-net-bytes-incoming

</td><td>

Retrieves the incoming network bytes per second across all network devices.

</td></tr><tr><td>

os.mac.check-system-net-bytes-outgoing

</td><td>

Retrieves the outgoing network bytes per second across all network devices.

</td></tr><tr><td>

os.mac.check-system-logged-in-users

</td><td>

Retrieves the detail of users currently logged in to the device.

</td></tr><tr><td>

os.mac.check-system-session-details

</td><td>

Retrieves the session time of currently logged-in users in minutes.

</td></tr><tr><td>

os.mac.check-system-network-details

</td><td>

Retrieves the network details, including Ethernet, Wi-Fi, and other relevant information.

</td></tr><tr><td>

os.mac.check-system-battery-details

</td><td>

Retrieves battery-related data, including the remaining battery percentage, the designed voltage, the estimated run time, and the battery's maximum capacity.**Note:**

-   This check definition doesn't apply to virtual machines \(VMs\) or desktops because they don't have batteries.
-   If current capacity is greater than designed capacity, the battery is rounded off to 100%.

</td></tr><tr><td>

os.mac.check-system-battery-charge-percentage

</td><td>

Retrieves the charge percentage of batteries present on the device.**Note:**

-   This check definition doesn't apply to virtual machines \(VMs\) or desktops because they don't have batteries.
-   If current capacity is greater than designed capacity, the battery is rounded off to 100%.

</td></tr><tr><td>

os.mac.check-system-firewall-enabled

</td><td>

Checks if the operating system firewall is active and enabled.

</td></tr><tr><td>

os.mac.check-system-pending-updates

</td><td>

Checks the status of pending software updates.

</td></tr><tr><td>

os.mac.check-system-admin-users

</td><td>

Retrieves all user accounts with local administrative privileges.

</td></tr><tr><td>

os.mac.check-system-reboot-details

</td><td>

Retrieves the reboot details for the device.

</td></tr><tr><td>

os.mac.check-system-os-setup-details

</td><td>

Retrieves the approximate OS age for the device.

</td></tr><tr><td>

os.mac.check-system-compliance-details

</td><td>

Retrieves the system’s compliance details. This includes the list of all configured apps and metric values that are non-compliant, and calculates a compliance rating based on that.

 **Note:**

-   This check definition provides the following details:
    -   **Condition for app to be said as compliant**: Every process mentioned in primary process should be running.
    -   **Condition for metric value to be said as compliant**: Value should be matching with the configured expected value.
-   The score is then calculated using this formula: Score = \( Complaint Application + Compliant metric value\) / \(Total Applications and metric value - Failed Ones\) \*100

</td></tr><tr><td>

os.mac.check-system-vpn-details

</td><td>

Get the VPN details for your device.

</td></tr><tr><td>

os.mac.check-system-energy-consumption

</td><td>

Gets Energy consumed by Mac machine in coming 5 minutes.**Note:** It's important to consider the following:

-   /usr/bin/powermetrics must be added to sudo Permissions.
-   The check takes approximately five minutes to get completed as it’s calculating energy consumed in the coming five minutes
-   This check definition doesn't work if agent is installed with rosetta enabled on M1, M2, M3 machines.

</td></tr><tr><td>

os.mac.check-system-power-consumption

</td><td>

Gets Power consumption for mac device.

</td></tr><tr><td>

os.mac.check-system-custom-query-on-change

</td><td>

Executes the custom query provided in the parameters. Returns value only when changed.

</td></tr><tr><td>

os.all.check.internal.get-device-configuration-on-change

</td><td>

Gets the configurations of a device. For example: sudo configured, debug on, agent user, and so on. Runs only if value changes.

</td></tr></tbody>
</table>## Check definitions — Diagnostic Actions

DEX provides the following types of check definitions for Diagnostic actions.

<table id="table_tyx_nnj_swb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.mac.check-app-process-ids

</td><td>

--process\_name=&lt;process name&gt;

</td><td>

Retrieves the Process IDs \(PIDs\) of both the parent and all the child processes associated with the application.

</td></tr><tr><td>

os.mac.check-process-cpu

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their CPU usage percentage, CPU time, Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.mac.check-process-memory

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their memory usage in kilobytes \(KB\), Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.mac.check-process-data

</td><td>

None

</td><td>

Retrieves the CPU usage, memory usage, and disk usage of all currently running processes.

</td></tr><tr><td>

os.mac.check-process-disk

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their disk usage in Bytes, Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.mac.check-traceroute

</td><td>

--url=&lt;url&gt;--max\_hops = &lt;default value is 65&gt;

--timeout = &lt;default value is 5&gt;

</td><td>

Retrieves the IP address, domain name, and round-trip time \(RTT\) for each network hop.

</td></tr><tr><td>

os.mac.check-ping-test

</td><td>

--url=&lt;url&gt;

</td><td>

Sends a ping request to the provided URL and returns the connectivity status, indicating whether the URL is reachable or not.

</td></tr><tr><td>

os.mac.check-services-data

</td><td>

service\_type =&lt;Type of service\(one of user, system or all\)

</td><td>

Retrieves the list of all services with PID, Service Name, Status, Service Type.

</td></tr></tbody>
</table>## Check definitions — Remedial Actions

DEX provides the following types of check definitions for Remedial actions.

<table id="table_ink_wb3_bzb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.mac.action-kill-process

</td><td>

--pid=&lt;process id&gt;OR

--process\_name=&lt;executable file name&gt;

**Note:** The process ID takes priority over the application name.

</td><td>

Terminates a running process or multiple processes specified by their Process ID \(PID\) or executable \(.app\) file name.

</td></tr><tr><td>

os.mac.action-restart-service

</td><td>

--service\_name=&lt;service name&gt;

</td><td>

Restarts logged user services that take a service name as input to the system.

</td></tr><tr><td>

os.mac.action-execute-jamf-policy

</td><td>

--Policy ID - policy\_id

</td><td>

Execute the Jamf policy either with a policy ID or with a predefined action. Predefined actions are set by the DEX admins in dex\_jamf\_policy table. The service desk agents are able to select and run the predefined actions as they might not have access to Jamf policy IDs. Jamf policy has information about the application name, package version information, action to be performed \(for example, install or uninstall\), information on enabled on self service, defined in the Jamf server.**Note:** Jamf client must be installed on the device to execute the Jamf policy.

</td></tr><tr><td>

os.mac.action-clear-app-cache

</td><td>

auto\_close = &lt;True/False whether you want the process to be closed before clearing the cache&gt;process\_name = &lt;Process name&gt;

app\_name = &lt;Application name&gt;

cache\_path = &lt;Path to the cache folder&gt;

</td><td>

Clears the application cache.**Note:** Cache path is supported for Zoom, Microsoft Outlook, and Microsoft Teams. Enter cache path without the path to the user. For example, if the cache is at path C:\\User\\&lt;UserName&gt;\\AppData\\Roaming\\Zoom\\data enter AppData\\Roaming\\Zoom\\data.

</td></tr><tr><td>

os.mac.action-zscaler-zpa-reconnect

</td><td>

None

</td><td>

Resolves Zscaler connectivity issues.

</td></tr><tr><td>

os.mac.action-restart-one-drive

</td><td>

None

</td><td>

Restarts one drive on the end-user's machine.

</td></tr><tr><td>

os.mac.action-clear-google-chrome-browsing-data

</td><td>

remove\_web\_data = &lt;True/False whether you want to remove the web data&gt;

</td><td>

Removes all the browsing data on Google Chrome from all the Google Chrome profiles.

</td></tr><tr><td>

os.mac.action-purge-recycle-bin

</td><td>

None

</td><td>

Purging Recycle Bin will clear all the files in the recycle bin.

</td></tr><tr><td>

os.mac.action-reset-google-chrome-settings

</td><td>

None

</td><td>

This action clears the settings and removes all the installed Google Chrome extensions on all the Google Chrome profiles.

</td></tr><tr><td>

os.mac.action-toggle-power-mode

</td><td>

power\_mode - Automatic, High power, Low power.

</td><td>

This action toggles through different power modes in a user mac device.

</td></tr><tr><td>

os.mac.action-elevate-temporary-admin

</td><td>

duration

 user\_id = ID of the user

</td><td>

Elevates temporary admin access to users for a period of time to perform specific tasks without compromising on security.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

