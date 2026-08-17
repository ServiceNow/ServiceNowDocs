---
title: Digital End-User Experience remedial actions
description: ServiceNow Digital End-User Experience \(DEX\) provides base system remedial actions to resolve issues on DEX monitored devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/dex-diff-ra.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Digital End-User Experience remedial actions

ServiceNow® Digital End-User Experience \(DEX\) provides base system remedial actions to resolve issues on DEX monitored devices.

<table id="new_ra_table"><thead><tr><th>

Remedial action

</th><th>

Input parameters

</th><th>

Supported OS and required privileges

</th><th>

Description

</th><th>

Use cases

</th></tr></thead><tbody><tr><td>

Add a registry key

</td><td>

`registry_path`, `registry_data`, `registry_type`

</td><td>

Windows: Local System Account for registry modifications, especially HKLM keysAdmin access to the device is required.

</td><td>

Adds a registry key to the device using a fully qualified path, value, and type.The Windows registry key stores settings or configuration data for the device operating system and Windows applications.

</td><td>

Push specific configurations remotely without Group Policy updates or manual device access. Possible use cases may include the following:-   Configure Windows OS or app settings that require new registry entries. \(Path example: HKCU\\ControlPanel\\TestColors\\WindowText.\)
-   Apply security configurations or app behavior settings at the registry level.
-   Push targeted configuration changes without a Group Policy update.

</td></tr><tr><td>

Clear application cache

</td><td>

`app_name`, `auto_close` \(closes the application before clearing the cache to confirm all cache files are cleared\), `process_name` \(for example, zoom.exe\), `cache_path`

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

Admin access to the device is required.

</td><td>

Removes the app cache for the configured application on the device.

</td><td>

Apply a safe first-response fix for collaboration-app performance, sync, and crash issues caused by corrupted cache. Possible use cases may include the following:-   Resolve Teams or Outlook performance issues, missing content, or sync errors from corrupted cache.
-   Fix Zoom video or audio quality issues attributed to corrupted cache files.
-   Free up disk space consumed by excessive app cache.

</td></tr><tr><td>

Clear browser cache

</td><td>

`browsers`

</td><td>

Windows: Local System AccountAdmin access to the device is required.

</td><td>

Removes temporary data stored on the device, such as cookies and website files.

</td><td>

Remove temporary browser data stored in your laptop to address slow device performance issues. Possible use cases may include the following:-   Automatically clear browser cache when device performance degrades due to accumulated temporary files.
-   Fix display errors, stale content, and login issues in browser-based business apps.
-   Resolve website loading issues or authentication problems caused by stale cookies and cached data.

</td></tr><tr><td>

Clear DNS cache

</td><td>

None

</td><td>

Windows: No elevated privileges requiredmacOS: Sudo permissions

Admin access to the device is required.

</td><td>

Removes temporary data stored on your laptop, such as cookies and website files.

</td><td>

Resolve display errors and login issues caused by outdated browser cache instantly, without remote desktop or user involvement. Possible use cases may include the following:-   Resolve web application loading issues from outdated or corrupted browser cache.
-   Fix display errors, stale content, and login issues in browser-based business apps.
-   Clear cache across multiple browsers in a single action execution.

</td></tr><tr><td>

Clear Google Chrome browsing data

</td><td>

`Remove web data` \(true or false\)

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Deletes Google Chrome browsing data to enhance speed, resolve page loading issues, and safeguard user privacy.

</td><td>

Resolve authentication loops and display failures caused by corrupted cookies or stale cached data. Possible use cases may include the following:-   Resolve login or SSO authentication loops caused by corrupted Chrome cookies.
-   Fix Chrome-based web application display issues caused by outdated cached content.
-   Clear browsing data for privacy or compliance requirements.

</td></tr><tr><td>

Clear Recycle Bin

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: No elevated privileges required

Admin access to the device is required.

</td><td>

Clears the recycle bin on the device.

</td><td>

Reclaim disk space consumed by deleted files that continue to take up storage. Possible use cases may include the following:-   Recover disk space on devices where deleted files are accumulating in the Recycle Bin or Trash.
-   Address low-disk-space alerts where the Recycle Bin or Trash is a significant contributor.
-   Combine with Disk Cleanup for more comprehensive storage reclamation.

</td></tr><tr><td>

Configure device power scheme

</td><td>

`power_mode` \(Low Power, Automatic, or High Power\)

</td><td>

macOS: Sudo permissions

</td><td>

Configures the power scheme settings and optimizes the performance, energy efficiency and battery life of the device.

</td><td>

Adjust macOS power settings remotely to match the user's context without requiring user action. Possible use cases may include the following:-   Improve macOS performance by switching to High Power mode when a user reports sluggishness.
-   Extend battery life by switching to Low Power mode for remote or traveling employees.
-   Standardize power settings across macOS device fleets remotely.

</td></tr><tr><td>

Delete a file

</td><td>

`file_name_or_path` — full filename or absolute file path.

</td><td>

Windows: No elevated privileges required

</td><td>

Permanently deletes the entered file \(full file name or absolute file path\) from the device.

</td><td>

Remove specific files with IT-controlled precision when broader system changes aren't appropriate. Possible use cases may include the following:-   Delete corrupted or blocker files preventing software installations or updates.
-   Remove files left over from failed uninstalls or incomplete cleanup operations.
-   Delete specific files as part of security incident response.

</td></tr><tr><td>

Delete network drive

</td><td>

action \(MAP or DELETE\), drive\_letter, network\_path \(for example, `\\server\share`\)

</td><td>

Windows: Local System Account

</td><td>

Removes a mapped network drive from your system and disconnects access to the shared location.

</td><td>

Network drive access issues are a common helpdesk request — mapping or removing drives remotely eliminates the need for IT remote desktop sessions or on-site visits. Possible use cases may include the following:-   Re-map a disconnected network drive when a user loses access to a shared file location.
-   Provision new network drive access for new hires or team changes.
-   Remove outdated or incorrect drive mappings.

</td></tr><tr><td>

Disable startup program

</td><td>

`startup_programs` \(comma-separated list\)

</td><td>

Windows: Local System Account

</td><td>

Disables the specified startup programs on the device.

</td><td>

Disable startup programs categorized as non-essential with user approval to reduce boot time and improve device performance after login. Possible use cases may include the following:-   Speed up device startup when it takes more than 2 minutes after power-on for the device to be ready to use.
-   Improve device performance after login when too many programs launch at once.
-   Reduce recurring startup delays caused by non-essential programs that launch automatically at startup.

</td></tr><tr><td>

Disk cleanup for low disk space

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Performs disk cleanup to solve slow system performance due to insufficient disk space.\*

</td><td>

Reclaim disk space automatically without user involvement or IT site visits. Possible use cases may include the following:-   Recover disk space on devices with low storage before performance degrades.
-   Proactively address low-disk-space alerts as part of routine endpoint maintenance.
-   Reduce disk usage remotely without user involvement.

</td></tr><tr><td>

Elevate temporary admin access

</td><td>

`user_name` \(Windows\) or `user_id` as email \(macOS\)`duration` — dropdown: 1, 2, 4, or 8 hours

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

Admin access to the device is required.

</td><td>

Provides temporary administrative privileges on the device for a period of time to perform specific tasks without compromising security.

</td><td>

Grant just-in-time admin access that expires automatically, supporting zero-standing-privilege policies. Possible use cases may include the following:-   Enable just-in-time admin access for software installations without permanent elevation.
-   Support PAM workflows with automatic, time-bound privilege expiry.
-   Reduce the risk of standing admin accounts on managed devices.

</td></tr><tr><td>

End process

</td><td>

`process_name` or `pid`

</td><td>

Windows: No elevated privileges requiredmacOS: Sudo permissions

</td><td>

Forcefully stops a running process on the device.

</td><td>

Stop a running process on your device to resolve slow computer performance issues caused by unresponsive programs or applications. Possible use cases may include the following:-   Automatically end resource-intensive or background processes causing slow device performance.
-   Stop unresponsive or frozen applications.

</td></tr><tr><td>

Execute Jamf policy

</td><td>

`policy_id` — the ID of the Jamf policy to execute

</td><td>

macOS: Sudo permissions

</td><td>

Executes the Jamf policy either with a policy ID or with a predefined action.Predefined actions, configured by DEX admins in dex\_jamf\_policy\_table, can be selected and executed by service desk agents, who don't have access to the policy IDs.

</td><td>

Bring macOS MDM actions directly into DEX alert-driven automation without switching between platforms. Possible use cases may include the following:-   Deploy or remove applications on Jamf-managed macOS devices directly from ServiceNow workflows.
-   Trigger any Jamf-managed policy without requiring the user to open Jamf Self Service.
-   Enforce software configurations or security policies through existing Jamf policies.

</td></tr><tr><td>

Kill zombie/orphan processes

</td><td>

`app_name`

</td><td>

Windows: No elevated privileges requiredmacOS: Sudo permissions

Admin access to the device is required.

</td><td>

Resolves app hangs and frees the device resources.

</td><td>

Possible use cases may include the following:-   Resolve application unresponsive behavior caused by zombie \(macOS\) or orphan processes \(Windows\) consuming system resources.
-   Free up CPU and memory held by defunct or parentless processes identified via top processes diagnostics or DEX alerts.

</td></tr><tr><td>

Map network drive

</td><td>

`drive_letter` \(drive letter to which the network location is mapped\)`network_path` \(path of the shared network location to be mapped\)

</td><td>

Windows: No elevated privileges required

</td><td>

Maps or removes a network drive using a specified drive letter and network path. These actions enable you to connect to shared resources on the network or help in cleaning up unused or outdated network connections.

</td><td>

Connect to shared resources on the network or remove outdated mappings without IT remote desktop sessions or on-site visits. Possible use cases may include the following:-   Re-map a disconnected network drive when a user loses access to a shared file location.
-   Provision new network drive access for new hires or team changes.
-   Remove outdated or incorrect drive mappings.

</td></tr><tr><td>

Modify a registry key value

</td><td>

`registry_path`, `registry_data`, `registry_type`

</td><td>

Windows: Local System AccountAdmin access to the device is required.

</td><td>

Updates a registry key value using a fully qualified path, value \(for example, `2222`\), and type \(for example, String, DWord\).

</td><td>

Correct specific registry entries remotely without disruptive system-wide changes. Possible use cases may include the following:-   Correct misconfigured registry values causing application or OS behavior issues.
-   Apply registry-level changes as part of automated remediation for known configuration drift.
-   Update application behavior through existing registry settings without manual device access.

</td></tr><tr><td>

Modify device battery power plan

</td><td>

`power_mode`

</td><td>

Windows: Local System Account

</td><td>

Adjusts device power plan settings using PowerShell scripts to optimize performance, energy efficiency, and battery life.

</td><td>

Adjust device power plan settings to extend battery life and optimize energy efficiency and device performance. Possible use cases may include the following:-   Automatically switch to balanced or power-saving modes to improve battery life on low-battery devices.
-   Address poor battery performance by enabling appropriate power modes based on device usage patterns.
-   Improve overall device performance and battery longevity by managing power consumption remotely.

</td></tr><tr><td>

Modify USB storage access \(Execute, Write, Read\)

</td><td>

`access` \(Read, Write, or Execute\), `value` \(Allow or Deny\)

</td><td>

Windows: Local System Account

</td><td>

Adjusts the following permissions:-   Execute: controls whether programs or scripts can run directly from a removable USB storage device.
-   Read: allows or blocks the ability to read data from a removable USB storage device.
-   Write: allows or blocks the ability to write data to a removable USB storage device.

</td><td>

Lock down or restore USB access at the permission level instantly, without endpoint management console access. Possible use cases may include the following:-   Lock down USB write access to prevent data exfiltration during a security investigation.
-   Restore specific USB permissions for an authorized use case after a temporary restriction.
-   Enforce DLP policies by restricting USB Execute access to prevent running unauthorized code.
-   Prevent unauthorized execution of files from USB devices.
-   Prevent data leakage or unauthorized file transfers to USB devices.

</td></tr><tr><td>

Remediate Zscaler connectivity

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Fixes connectivity issues with Zscaler Private Access on the device.

</td><td>

Automate a fix for ZPA connection drops that leave remote employees cut off from internal applications. Possible use cases may include the following:-   Resolve ZPA connectivity issues remotely without IT remote desktop access.
-   Fix ZPA connections stuck in a disconnected or failed state.
-   Enable automated remediation when Zscaler monitoring detects a failure.

</td></tr><tr><td>

Repair corrupt Outlook files

</td><td>

None

</td><td>

Windows: Local System AccountYou require permissions for the folders where OST/PST files reside:

-   List folder/read data
-   Write attributes
-   Modify or delete subfolders and files

</td><td>

Detects and repairs both OST and PST file types in Microsoft Classic Outlook on end-user devices.

</td><td>

Enhance Microsoft Outlook performance and synchronization on end-user devices.The `SCANPST.exe` tool is used to fix files up to 2 GB in size. For larger files, the following behavior applies:

-   2-20 GB: Performance degrades, success depends on the corruption severity.
-   20-50 GB: Significantly reduced effectiveness, frequent failures are reported.
-   Over 50 GB: Very low success rate, tool struggles or fails completely.

</td></tr><tr><td>

Reset Google Chrome browser settings

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Resets the Google Chrome browser settings to default on all profiles of the current logged-in user.

</td><td>

Resolve corrupted Chrome settings and problematic extensions without reinstalling Chrome. Possible use cases may include the following:-   Resolve browser issues from misconfigured or corrupted Chrome settings.
-   Remove conflicting or malicious Chrome extensions affecting browser behavior or security.
-   Restore Chrome stability when it is crashing or behaving unexpectedly.

</td></tr><tr><td>

Reset network adapter

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Resets the WiFi network adapter by turning it off and back on.

</td><td>

Resolve connectivity issues where the device shows a strong WiFi signal but experiences poor network performance or application timeouts. Possible use cases may include the following:-   Speed up applications and web pages when network connectivity is degraded despite showing a strong WiFi signal.
-   Help identify if poor performance is caused by network issues rather than a slow device.
-   Restore WiFi connection with user approval when the adapter stops responding.

</td></tr><tr><td>

Restart Audio Services

</td><td>

`service_name`

</td><td>

Windows: Local System Account

</td><td>

Restarts audio services to restore sound and microphone functionality.

</td><td>

Restart audio services to restore sound and microphone functionality and resolve playback and recording issues on the device. Possible use cases may include the following:-   Automatically restart audio services when sound or microphone functionality fails or becomes unresponsive.
-   Resolve microphone issues affecting communication applications like Zoom by restarting audio services.

Use **AudioEndpointBuilder** and **Audiosrv** to restore sound and microphone functionality. This fixes common playback and recording issues on the device.

</td></tr><tr><td>

Restart Microsoft OneDrive

</td><td>

None

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

</td><td>

Restarts Microsoft OneDrive on the device to resolve sync issues and update all recent changes, as long as the user is signed in to Microsoft OneDrive.

</td><td>

Resolve Microsoft OneDrive sync failures that block access to cloud-stored files, without user involvement or a reboot. Possible use cases may include the following:-   Resolve Microsoft OneDrive sync failures or stuck uploads and downloads.
-   Fix Microsoft OneDrive showing as disconnected, paused, or stuck on "syncing".
-   Address OneDrive performance issues caused by a hung or unresponsive process.

</td></tr><tr><td>

Restart Microsoft Outlook

</td><td>

`process_name`, `app_name`

</td><td>

Windows: No elevated privileges required

</td><td>

Restarts Microsoft Outlook on the device.

</td><td>

Restart Microsoft Outlook on end-user devices to resolve application performance issues. Possible use cases may include the following:-   Automatically restart Microsoft Outlook to resolve email synchronization delays or connection issues.
-   Resolve frozen or unresponsive Outlook windows by forcefully restarting the application.
-   Restore Microsoft Outlook functionality and stability.

</td></tr><tr><td>

Restart service

</td><td>

`service_name` \(for example, Spooler or \)

</td><td>

Windows: Local System AccountmacOS: Sudo permissions

Admin access to the device is required.

</td><td>

Restarts the service or application running on the device.

</td><td>

Restore failed or hung services without rebooting the device, minimizing user disruption. Possible use cases may include the following:-   Restore a failed or hung service without rebooting the device.
-   Fix services that stopped after software updates \(print spooler, VPN client, security agents\).
-   Recover managed monitoring or security agents that have stopped responding.

</td></tr><tr><td>

Uninstall an application

</td><td>

`app_name` \(selected from a pre-configured dropdown in the UI\)

</td><td>

Windows: Local System AccountAdmin access to the device is required.

</td><td>

Uninstalls a selected application from the action library on the device.

</td><td>

Enforce software compliance remotely at scale by removing unauthorized or redundant applications. Possible use cases may include the following:-   Remove unauthorized or prohibited software from managed devices without user action.
-   Enforce software compliance policies during audits or security reviews.
-   Support license reclamation by removing software from specific devices.

</td></tr></tbody>
</table>**Note:** \* For the Disk cleanup for low disk space action, temporary files are deleted from the following device locations.

-   Windows:
    -   `C:\Windows"="*.dmp`
    -   `"C:\Windows\Downloaded Program Files"="*.*"`
    -   `"$env:UserProfile\Appdata\Local\Microsoft\Windows\Temporary Internet Files"="*.*"`
    -   `"C:\Windows\Temp"="*.*"`
    -   `"C:\Windows\System32\LogFiles"="*.*"`
    -   `"C:\ProgramData\Microsoft\Windows\WER\ReportQueue"= "*.*"`
-   macOS:
    -   $HOME/Library/Caches/\*/ = cache files older than 7 days \(excluding Homebrew\)
    -   $HOME/Library/Developer/Xcode/DerivedData/\*/ = Xcode build artifacts \(if Xcode is installed\)
    -   $HOME/Library/Caches/Homebrew/ = Homebrew package download cache \(if Homebrew is installed\)
    -   $HOME/Library/Caches/Homebrew/\*/ = Homebrew package download cache in subdirectories \(if Homebrew is installed\)
    -   /tmp/\*/ = temporary files older than 3 days

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

