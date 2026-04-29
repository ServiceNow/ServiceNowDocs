---
title: DEX check definitions for Windows
description: Check definitions for Windows are predetermined sets of rules and criteria that assess the performance, security, and conformance of Windows devices. These checks can cover various aspects such as CPU usage, memory usage, network tests, network bytes, and logged-in users.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX check definitions for Windows

Check definitions for Windows are predetermined sets of rules and criteria that assess the performance, security, and conformance of Windows devices. These checks can cover various aspects such as CPU usage, memory usage, network tests, network bytes, and logged-in users.

To fetch the complete playbook data for a Windows device, the Agent Client Collector \(ACC\) must run as a local system account. For more details on how to set up the ACC service as a local system account, see [Run ACC as a local system account user](../task/run-acc-local-sys-account.md).

**Note:** You can configure the check definitions and associated retrievable data. Some of the listed check definitions might retrieve data that contains or is considered personal information.

## Check definitions — Application \(Metrics\)

DEX offers the following check definitions that are accessible solely when the application is running, except for the os.win.check-app-crash-rate and os.win.check-app-last-access-time check definitions, which are accessible even when the application isn't running. In the check definition parameters:

-   appName = application name. Example, Zoom.
-   appSysId= sys\_id of the application.
-   primaryProcess = list of primary processes for the application separated by a pipe symbol \(\|\). The first process that exists on the endpoint device is given priority. Example 1: chrome.exe. Example 2: teams.exe\|msteams.exe.

    **Note:** If the primary process for the Microsoft Teams application in Windows 10 is teams.exe and in Windows 11 it's msteams.exe, then when determining priority based on process availability on the endpoint device, the process that is present on the endpoint device first is given precedence.

-   secondaryProcesses = list of secondary processes for the application separated by a pipe symbol \(\|\). Example, cpthost.exe\|cptservice.exe.

<table id="table_yxf_q4d_hwb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.win.check-app-cpu-usage

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the amount of CPU resources being used by the primary process and secondary process of the application.

</td></tr><tr><td>

os.win.check-app-memory-usage

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the amount of memory being used by the primary process and secondary process of the application.

</td></tr><tr><td>

os.win.check-app-last-access-time

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the most recent time when the application was executed or run.**Note:**

-   This check definition doesn't require the application to be in a running state.
-   If the application hasn't been run within the last 7 days, the last access time is empty.
-   If the application's process path changes within 7 days \(which can occur during app updates\), the last access time is empty until you run the app again.
-   To modify the 7-day retention policy, you can change the registry path in the following way:
    -   Registry Key: "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Session Manager\\BAM"
    -   Registry Name: "UserSettingsLifetimeMs"
    -   Registry Type: REG\_DWORD \(32-bit value\)
    -   Registry Value: Duration in milliseconds

</td></tr><tr><td>

os.win.check-app-last-updated

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the time and date of the latest application update installation.

</td></tr><tr><td>

os.win.check-app-crashes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves crash rate of the application.

 This check definition supports applications that emit a Window Error Reporting \(WER\) events \(event id = 1000\) on crashing.

**Note:** This check definition doesn't require the application to be running.

</td></tr><tr><td>

os.win.check.app.freezes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves freeze rate of the application in the last 5 minutes.

 This check definition supports applications that emit a Window Error Reporting \(WER\) events \(event id = 1001 or 1002\) on freezing.

**Note:** This check definition doesn't require the application to be running.

</td></tr><tr><td>

os.win.check-app-uptime

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Checks the uptime of the given application.

</td></tr><tr><td>

os.win.check-app-incoming-network-bytes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;
-   sleep\_time =&lt;Duration of time from now for which you must calculate the average incoming network byte/sec&gt;

</td><td>

Retrieves the incoming network bytes of an application for IPv4 and IPv6 networks.

</td></tr><tr><td>

os.win.check-app-outgoing-network-bytes

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;
-   sleep\_time =&lt;Duration of time from now for which you must calculate the average incoming network byte/sec&gt;

</td><td>

Retrieves the outgoing network bytes of an application for IPv4 and IPv6 networks.

</td></tr><tr><td>

os.win.check-app-domain-network-details

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;
-   domain=&lt;Domain of the application&gt;

</td><td>

Retrieves the network latency, packet loss, and jitter for installed application domain.**Note:** The system uses the Internet Control Message Protocol \(ICMP\) to collect network performance metrics, such as latency, jitter, and packet loss.

</td></tr><tr><td>

os.win.check-app-domain-network-route-details

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;
-   domain=&lt;Domain of the application&gt;

</td><td>

Retrieves the complete network route details for application domain.

</td></tr><tr><td>

os.win.check-app-sccm

</td><td>

None

</td><td>

Fetches application-specific metrics for the App - Microsoft System Center Configuration Manager.

</td></tr><tr><td>

os.win.check-app-zscaler-service-status

</td><td>

-   --appName=&lt;application name&gt;
-   --primaryProcess=&lt;primary process name&gt;
-   --secondaryProcesses=&lt;list of secondary processes separated by a pipe symbol&gt;
-   --appSysId=&lt;sys id of the application&gt;

</td><td>

Retrieves the Zscaler service status information.

</td></tr></tbody>
</table>## Check definitions — Device \(Metrics\)

DEX provides the following types of check definitions for the device.

<table id="table_wtg_ydq_rwb"><thead><tr><th>

Check definition name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.win.check-system-cpu-usage

</td><td>

Checks the current CPU utilization.

</td></tr><tr><td>

os.win.check-system-cpu-details

</td><td>

Retrieves the CPU ID, CPU name, number of physical and logical cores, and architecture information.

</td></tr><tr><td>

os.win.check-system-memory-usage

</td><td>

Checks the current system memory utilization.

</td></tr><tr><td>

os.win.check-system-last-access-time

</td><td>

Checks the last time the current device was accessed. **Note:** This check definition works on locked and unlocked devices. The first time this check definition runs, the events are captured and an error message appears as there is no prior data available.

</td></tr><tr><td>

os.win.check-system-uptime

</td><td>

Checks the time elapsed since the last boot of the system.

</td></tr><tr><td>

os.win.check-system-disk-io-usage-read

</td><td>

Retrieves disk bytes read per second.

</td></tr><tr><td>

os.win.check-system-disk-io-usage-write

</td><td>

Retrieves disk bytes written according to second.

</td></tr><tr><td>

os.win.check-system-energy-consumption

</td><td>

Retrieves the energy consumption values for CPU, SoC, display, disk, network, MBB, EMI, other, total, and loss of a Windows device in milliwatt-hours.**Note:** This check definition isn't compatible with virtual machines that don't have energy sensors.

Unlike other check definitions that retrieve latest data, this check definition retrieves the sum of last 5 minutes of data.

</td></tr><tr><td>

os.win.check-system-time

</td><td>

Checks the current time in Coordinated Universal Time \(UTC\) using UNIX timestamp.

</td></tr><tr><td>

os.win.check-system-power-plan

</td><td>

Retrieves the name of the active power plan.

</td></tr><tr><td>

os.win.check-system-os-details

</td><td>

Retrieves the name, version, platform, architecture, and installation date of the operating system.

</td></tr><tr><td>

os.win.check-system-device-crashes

</td><td>

Retrieves details of different crashes on your device.**Note:** This check definition supports BSOD that emits system events with event ids = 41,1001.

</td></tr><tr><td>

os.win.check-system-device-events

</td><td>

Retrieves the details of events that occurred on the device during the specified time interval. Events for Windows include: last boot and logged-in users.

</td></tr><tr><td>

os.win.check-system-disk-usage

</td><td>

Retrieves the disk used space as a percentage of the total space.

</td></tr><tr><td>

os.win.check-system-battery-details

</td><td>

Retrieves battery-related data, including the remaining battery percentage, the designed voltage, the estimated run time, and the battery's maximum capacity.**Note:**

-   This check definition doesn't apply to virtual machines \(VMs\) or desktops because they don't have batteries.
-   If current capacity is greater than designed capacity, the battery is rounded off to 100%.

</td></tr><tr><td>

os.win.check-system-network-details

</td><td>

Retrieves the network details, including Ethernet, Wi-Fi, and other relevant information.

</td></tr><tr><td>

os.win.check-system-logged-in-users

</td><td>

Checks the login user ID of the users who are currently logged in to the device.

</td></tr><tr><td>

os.win.check-system-power-consumption

</td><td>

Retrieves the power consumption of the device in milliwatt.**Note:** This check definition is exclusively compatible with physical machines and doesn't support virtual machines \(VMs\).

</td></tr><tr><td>

os.win.check-system-admin-users

</td><td>

Retrieves all user accounts with local administrative privileges.

</td></tr><tr><td>

os.win.check-system-bsod

</td><td>

Retrieves the count, message, ID, level, and time of Blue Screen of Death \(BSOD\) occurrences.**Note:** This check definition supports BSOD that emits system events with event ids = 1001.

</td></tr><tr><td>

os.win.check-system-firewall-enabled

</td><td>

Checks if the operating system firewall is active and enabled.

</td></tr><tr><td>

os.win.check-system-antimalware-details

</td><td>

Retrieves the details of the anti-malware software on the device.

</td></tr><tr><td>

os.win.check-system-reboot-details

</td><td>

Retrieves the reboot duration in seconds and the last reboot timestamp \(in UNIX epoch time\).**Note:** The displayed values might not accurately reflect cases where system reboots were interrupted, such as during system updates, power loss, or manual intervention.

</td></tr><tr><td>

os.win.check-system-os-setup-details

</td><td>

Retrieves the approximate OS age for the device.

</td></tr><tr><td>

os.win.check-system-network-adapter-details

</td><td>

Retrieves the network adapter details for the device.

</td></tr><tr><td>

os.win.check-system-network-connection-profiles

</td><td>

Retrieves the network connection profile details for the device.**Note:** This check definition retrieves the network type, which can be used to check the vpn status.

</td></tr><tr><td>

os.win.check-system-compliance-details

</td><td>

Retrieves the system’s compliance details. This includes the list of all configured apps and metric values that are non-compliant, and calculates a compliance rating based on that.**Note:**

-   This check definition provides the following details:
    -   **Condition for app to be said as compliant**: Every process mentioned in primary process should be running.
    -   **Condition for metric value to be said as compliant**: Value should be matching with the configured expected value.
-   The score is then calculated using this formula: Score = \( Complaint Application + Compliant metric value\) / \(Total Applications and metric value - Failed Ones\) \*100

</td></tr><tr><td>

os.win.check-system-battery-charge-percentage

</td><td>

Retrieves the battery charge percentage on Windows device.**Note:** If current capacity is greater than designed capacity, the battery is rounded off to 100%.

</td></tr><tr><td>

os.win.check-system-windows-registry

</td><td>

Retrieves the Windows registry data.

</td></tr><tr><td>

os.win.check-system-memory-details

</td><td>

Retrieves the system memory details like and virtual memory details.

</td></tr><tr><td>

os.win.check-system-bios-details

</td><td>

Retrieves the System Bios details.

</td></tr><tr><td>

os.win.check-system-executables

</td><td>

Fetches all the executables \(\*.exe\) present on Windows machine.

</td></tr><tr><td>

os.win.check-system-custom-query-on-change

</td><td>

Execute the custom query provided in the parameters. Runs only if value changes.

</td></tr><tr><td>

os.all.check.internal.get-device-configuration-on-change

</td><td>

Gets the configurations of a device. Example: sudo configured, debug on, agent user, and so on. Runs only if value changes.

</td></tr><tr><td>

os.win.check-system-boot-details

</td><td>

Gets latest boot details of a device from Windows event log.**Note:** Boot time is captured only during a full device boot. Windows generates Event ID 100 during a full boot to measure performance. Boot time is not recorded when the device is resumed, restored, or started through remote or virtual machine operations because Event ID 100 is not generated

</td></tr><tr><td>

os.win.check-system-gpu-usage-details

</td><td>

Monitor GPU \(Graphics Processing Unit\) and VRAM \(Video Random Access Memory\) usage on the **Device** page to assess graphics performance and identify bottlenecks.

</td></tr></tbody>
</table>## Check definitions — Diagnostic Actions

DEX provides the following types of check definitions for Diagnostic actions.

<table id="table_tyx_nnj_swb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Diagnostic action

</td></tr><tr><td>

os.win.check-app-process-ids

</td><td>

--process\_name=&lt;process name&gt;

</td><td>

Retrieves the Process IDs \(PIDs\) of both the parent and all the child processes associated with the application.

</td></tr><tr><td>

os.win.check-process-cpu

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their CPU usage percentage, CPU time, Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.win.check-process-memory

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their memory usage in kilobytes \(KB\), Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.win.check-process-disk

</td><td>

None

</td><td>

Retrieves a list of all running processes along with their disk usage in Bytes, Process ID \(PID\), Parent Process ID \(PPID\), and name.

</td></tr><tr><td>

os.win.check-rssi-value

</td><td>

None

</td><td>

Retrieves the Received Signal Strength Indicator \(RSSI\) value for the currently connected WiFi interface.RSSI indicates the signal strength between the wireless access point \(AP\) and the device, with higher RSSI values indicating stronger signal strength.

**Note:** This check definition can't be applied to a virtual machine.

</td></tr><tr><td>

os.win.check-services-data

</td><td>

service\_type =&lt;Type of service\(one of user, system or all\)

</td><td>

Retrieves the list of all services with PID, Service Name, Service Display Name, Status, Service Type.

</td></tr></tbody>
</table>## Check definitions — Remedial Actions

DEX provides the following types of check definitions for Remedial actions.

<table id="table_ozn_5c3_bzb"><thead><tr><th>

Check definition name

</th><th>

Check definition parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

os.win.action-kill-process

</td><td>

--pid=&lt;process id&gt;OR

--process\_name=&lt;list of comma separated executable file names&gt;

**Note:** The process ID takes priority over the application name.

</td><td>

Terminates a running process or multiple processes specified by their Process ID \(PID\) or a list of executable \(.exe\) file names.

</td></tr><tr><td>

os.win.action-restart-service

</td><td>

--service\_name=&lt;service name&gt;

</td><td>

Restarts logged user services that take a service name as input to the system.

</td></tr><tr><td>

os.win.action-flush-dns-cache

</td><td>

None

</td><td>

Flushes DNS cache on a Windows device.

</td></tr><tr><td>

os.win.action-clear-browser-cache

</td><td>

--auto\_close = &lt;true/false&gt;**Note:** When auto-close is enabled, while clearing the browser cache, the browser is closed and vice versa.

--browsers = &lt;List of comma separated browsers&gt;

</td><td>

Clears cache of the supported browsers such as Google Chrome,Mozilla Firefox, and Microsoft Edge.**Note:** Before executing this check definition, save your browser work.

</td></tr><tr><td>

os.win.action-clear-app-cache

</td><td>

auto\_close = &lt;True/False whether you want the process to be closed before clearing the cache&gt;process\_name = &lt;Process name&gt;

app\_name = &lt;Application name&gt;

cache\_path = &lt;Path to the cache folder&gt;

**Note:** The cache path is supported for Zoom, Microsoft Outlook, and Microsoft Teams. Cache path should be entered without the path to the user. For example, if the cache is at path C:\\User\\&lt;UserName&gt;\\AppData\\Roaming\\Zoom\\data enter AppData\\Roaming\\Zoom\\data.

</td><td>

Clears the application cache.

</td></tr><tr><td>

os.win.action-network-drive

</td><td>

action: &lt;MAP/DELETE&gt;drive\_letter

network\_path

</td><td>

Maps or deletes a network drive depending on the action input parameter, which supports the following values: -   MAP – to map a network drive
-   DELETE – to remove a mapped network drive

</td></tr><tr><td>

os.win.action-restart-application

</td><td>

process\_name = &lt;Process name&gt;

 app\_name = &lt;Application name&gt;

</td><td>

Restarts the application if it is running.

</td></tr><tr><td>

os.win.action-removable-usb-storage-access

</td><td>

access - &lt;deny\_read/deny\_write/deny\_execute&gt;value - &lt;true/false&gt;

</td><td>

Controls access to removable USB storage disks for read, write, and execute access.**Note:**

-   This action is effective only if removable USB storage access is not already controlled by other mechanisms, such as Group Policies, third-party endpoint protection tools, or device control software.
-   After you run the check, restart the device for the access changes to take effect.

</td></tr><tr><td>

os.win.action-uninstall-application

</td><td>

app\_name = &lt;application name&gt;

</td><td>

Uninstall an application.

</td></tr><tr><td>

os.win.action-zscaler-zpa-reconnect

</td><td>

None

</td><td>

Resolves Zscaler connectivity issues.

</td></tr><tr><td>

os.win.action-restart-one-drive

</td><td>

None

</td><td>

Restarts OneDrive on the end-user's machine.

</td></tr><tr><td>

os.win.action-disk-cleanup

</td><td>

None

</td><td>

Clears unwanted files or cache using Windows disk cleanup:-   Internet cache files
-   System error memory dump files
-   System error mini-dump files
-   Temporary files
-   Windows error reporting

</td></tr><tr><td>

os.win.action-windows-registry-action

</td><td>

registry\_path = &lt;Absolute Windows registry key path&gt; \(Complete path of the registry key to be added\)

 registry\_data = &lt;Data to be added or modified in a given registry key&gt;

 Registry\_type = &lt;Type of the registry key data&gt; \(One of the default provided options\)

</td><td>

Allows the user to create a new Windows registry key or modify an existing one. Users can add new keys, or update the data and value type of existing registry entries as needed.

</td></tr><tr><td>

os.win.action-delete-file

</td><td>

file\_name\_or\_path = &lt;File name or path&gt;

</td><td>

Permanently delete the entered file. Entered file should have a valid type extension.

</td></tr><tr><td>

os.win.action-clear-google-chrome-browsing-data

</td><td>

remove\_web\_data = &lt;True/False whether you want to remove the web data&gt;

</td><td>

Removes all the browsing data on Google chrome from all the Google chrome profiles.

</td></tr><tr><td>

os.win.action-purge-recycle-bin

</td><td>

None

</td><td>

Purging Recycle Bin will clear all the files in the recycle bin.

</td></tr><tr><td>

os.win.action-reset-google-chrome-settings

</td><td>

None

</td><td>

Clears the settings and removes all the installed Google chrome extensions on all the google chrome profiles.

</td></tr><tr><td>

os.win.action-toggle-power-plan

</td><td>

power\_mode - Balanced, High performance, Power saver

</td><td>

Toggle between different power plans.

</td></tr><tr><td>

os.win.action-elevate-temporary-admin

</td><td>

duration

 user\_id = ID of the user

</td><td>

Elevates temporary admin access to users for a period of time to perform specific tasks without compromising on security.

</td></tr><tr><td>

os.win.action-fix-classic-outlook-data-files

</td><td>

None

</td><td>

Fixes OST / PST data files using SCANPST.EXE in Classic outlook

</td></tr></tbody>
</table>**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

