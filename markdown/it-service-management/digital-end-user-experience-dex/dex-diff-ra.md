---
title: Digital End-User Experience Remedial Actions
description: ServiceNow Digital End-User Experience \(DEX\) provides base system remedial actions to resolve issues on DEX-monitored devices.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Administration cards, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Digital End-User Experience Remedial Actions

ServiceNow® Digital End-User Experience \(DEX\) provides base system remedial actions to resolve issues on DEX-monitored devices.

<table id="table_opb_n5d_zfc"><thead><tr><th>

Remedial Action name

</th><th>

Supported OS

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Battery replacement catalog request

</td><td>

Windows/macOS

</td><td>

Catalog request for battery replacement to solve poor battery performance due to deteriorated battery. A catalog request would be raised for you based on your device and battery details.

</td></tr><tr><td>

Clear application cache

</td><td>

Windows/macOS

</td><td>

Performing this action removes the app cache for the selected application on this device. This helps the device run faster and frees up storage space. Supported applications include Microsoft Teams Classic \(macOS\), Google Chrome \(macOS\), Zoom \(macOS and Windows\), Slack \(macOS\), Outlook \(Windows\), and Teams \(Windows\).Use the dex\_action\_app\_config table to add more applications that support this action. Configure the corresponding cache URL to be cleared for each application in the same table. Separate cache URLs by a comma if entering multiple URLs for an app.

**Note:**

-   Select the field auto-close, which closes the application before clearing the cache to confirm all the cache files are cleared.
-   To clear application cache, you need to have the admin access to the device.

</td></tr><tr><td>

Clear browser cache

</td><td>

Windows/macOS

</td><td>

Clearing your browser cache removes temporary data stored on your laptop, such as cookies and website files.**Note:** To clear browser cache, you need to have the admin access to the device.

</td></tr><tr><td>

End process

</td><td>

Windows/macOS

</td><td>

Performing this action on an end user's device forcefully stops a running process.

</td></tr><tr><td>

Execute Jamf policy

</td><td>

macOS

</td><td>

Execute the Jamf policy either with a policy ID or with a predefined action. Predefined actions, configured by DEX admins in the `dex_jamf_policy_table`, can be selected and executed by service desk agents, who don’t have access to the policy IDs. The predefined actions must be set in the table `dex_jamf_policy` and update the fields Action name, Application, Policy ID, and Active. The detailed information on the fields is listed in the following table.The following are the Jamf limitations:

-   As DEX Admin, you must know the Jamf pro features and have knowledge about the policies configured for applications at the customer Jamf server.
-   Some policies when run, notify the user to update the application instead of automatically updating it. For example, Zoom doesn't automatically update. In cases like these, the policy is executed successfully only if the employee approves the update of the application. Otherwise, the remedial action execution fails.

</td></tr><tr><td>

Restart service

</td><td>

Windows/macOS

</td><td>

Performing this action on a end-user's laptop involves restarting the service or application running on their device.**Note:** To restart service, you need to have the admin access to the device.

</td></tr><tr><td>

Windows disk cleanup for low disk space

</td><td>

Windows

</td><td>

Performing Windows disk clean up to solve slow system performance due to insufficient disk space. Files such as temporary internet files, recycle bin, thumbnails, temporary files, etc would be deleted to free up your disk space.

</td></tr><tr><td>

Perform disk cleanup

</td><td>

Windows/macOS

</td><td>

Performing this action deletes temporary internet, memory, log, and cache files to free up the hard drive space and optimize the device performance similar to the following:-   `C:\Windows"="*.dmp`
-   `"C:\Windows\Downloaded Program Files"="*.*"`
-   `"$env:UserProfile\Appdata\Local\Microsoft\Windows\Temporary Internet Files"="*.*"`
-   `"C:\Windows\Temp"="*.*"`
-   `"C:\Windows\System32\LogFiles"="*.*"`
-   `"C:\ProgramData\Microsoft\Windows\WER\ReportQueue"= "*.*"`

</td></tr><tr><td>

Clear DNS cache

</td><td>

Windows/macOS

</td><td>

Performing this action on an end-user's device will clear the DNS cache.

</td></tr><tr><td>

Reset Google Chrome browser settings

</td><td>

Windows/macOS

</td><td>

Performing this action resets the Google Chrome browser settings to default on all devices.**Note:** This action would reset the configuration established by default by your organization's IT department. This is not the same as performing a factory reset.

-   Only the extensions that are synced with the user account are restored.
-   Preferences and Secure preferences files will be removed.

</td></tr><tr><td>

Clear Google Chrome browsing data

</td><td>

Windows/macOS

</td><td>

Deleting Google Chrome browsing data enhances its speed, resolves page loading issues, and safeguards the user's privacy.**Note:**

-   Clearing web data will sign you out of your Google account and remove all saved addresses, payment methods, and auto-fill data. To stay signed in and keep this data, do not clear your web data.
-   You need these minimum permissions on Windows to clear browsing data.
    -   List folder / read data
    -   Write attributes
    -   Delete sub-folders and files

</td></tr><tr><td>

Configure device power scheme

</td><td>

macOS

</td><td>

Performing this action on the end-user's device configures the power scheme settings and optimizes the performance, energy efficiency and battery life of the device.

</td></tr><tr><td>

Clear recycle bin

</td><td>

Windows/macOS

</td><td>

Performing this action on an end-user's device will clear the recycle bin on the device.**Note:**

-   To clear recycle bin, you need to have the admin access to the device.
-   For Windows devices, only C: drive recycle bin is targeted as part of the remedial action.

</td></tr><tr><td>

Elevate temporary admin access

</td><td>

Windows/macOS

</td><td>

Performing this action on the end-user's device provides temporary administrative privileges for a period of time to perform specific tasks without compromising on security.**Note:**

-   To elevate the temporary administrative privileges, you need to have the admin access to the device.
-   The task scheduler must be enabled to get the admin rights.

</td></tr><tr><td>

Remediate Zscaler connectivity

</td><td>

Windows/macOS

</td><td>

Performing this action on the end-user's device will fix any connectivity issues with Zscaler Private Access.**Note:**

-   Enable the Zscaler Command Line interface feature on the device.
-   It is applicable only if version 4.4 and later for Windows and Zscaler Client Connector version 4.3 and later for macOS is installed on the device.

</td></tr><tr><td>

Restart Microsoft OneDrive

</td><td>

Windows/macOS

</td><td>

Performing this action on the end-user's device will restart OneDrive to resolve any sync issues and update all recent changes as long as you are signed in to OneDrive.**Note:**

-   For macOS users, you need to stay logged in on OneDrive in order to restart OneDrive.
-   For Windows users, you need admin access to restart OneDrive if it is installed in the user's folder.

</td></tr><tr><td>

Repair corrupt Outlook files

</td><td>

Windows/macOS

</td><td>

Performing this action on an end-user's device detects and repairs both OST and PST file types in Microsoft Classic Outlook. This helps in enhancing Outlook performance and synchronization.**Note:** OST/PST files upto 2 GB size can be fixed using the `SCANPST.exe` and beyond 2 GB, the behaviour is as follows:

-   2-20 GB: The performance degrades, success depends on the corruption severity.
-   20-50 GB: Significantly reduced effectiveness, frequent failures are reported.
-   Over 50 GB: Very low success rate, tool struggles or fails completely.
-   In order to Fix outlook data file Remedial Action to work, you need permissions for the following folders where the OST/PST files reside.
    -   List folder / read data
    -   Write attributes
    -   modify or delete subfolders and files

</td></tr><tr><td>

Uninstall the application

</td><td>

Windows

</td><td>

-   Performing this action on an end-user's device uninstalls the selected application from the action library.
-   Only applications installed through .exe or .msi files will be uninstalled. Core OS and system applications do not get uninstalled, even if the action is executed successfully.

 **Note:** In order to uninstall an application, you need to have the admin access to the device.

</td></tr><tr><td>

Map Network Drive

</td><td>

Windows

</td><td>

Performing this action maps a network drive using a specified drive letter and network path. This action allows users to connect to shared resources on the network.**Note:**

-   The drive\_letter parameter specifies the drive letter to which the network location will be mapped, and the network\_path parameter specifies the path of the shared network location that is to be mapped.
-   The network\_path should not require authentication, or it should be pre-authenticated, for this check to run successfully.

</td></tr><tr><td>

Delete Network Drive

</td><td>

Windows

</td><td>

Performing this action removes a mapped network drive using the drive letter. This helps in cleaning up unused or outdated network connections.

</td></tr><tr><td>

Restart Audio Services

</td><td>

Windows

</td><td>

Performing this action restarts audio services **AudioEndpointBuilder** and **Audiosrv** to restore sound and microphone functionality. This fixes common playback and recording issues on your device.

</td></tr><tr><td>

Modify USB storage access: Execute

</td><td>

Windows

</td><td>

Performing this action adjusts the Execute permission, which controls whether programs or scripts can run directly from a removable USB storage device. Use this action to prevent unauthorized execution of files from USB devices.**Note:**

-   This action is effective only if removable USB storage access is not already controlled by other mechanisms, such as Group Policies, third-party endpoint protection tools, or device control software.
-   In order to perform this action, you need to have the admin access to the device.
-   After you perform this action, restart the device for the access changes to take effect.

</td></tr><tr><td>

Modify USB storage access: Read

</td><td>

Windows

</td><td>

Performing this action adjusts the Read permission, allowing or blocking the ability to read data from a Removable USB storage device. Use this action to restrict data exfiltration or unauthorized data access.**Note:**

-   This action is effective only if removable USB storage access is not already controlled by other mechanisms, such as Group Policies, third-party endpoint protection tools, or device control software.
-   In order to perform this action, you need to have the admin access to the device.
-   After you perform this action, restart the device for the access changes to take effect.

</td></tr><tr><td>

Modify USB storage access: Write

</td><td>

Windows

</td><td>

Performing this action adjusts the Write permission, allowing or blocking the ability to write data to a Removable USB storage device. Use this action to prevent data leakage or unauthorized file transfers to USB devices.**Note:**

-   This action is effective only if removable USB storage access is not already controlled by other mechanisms, such as Group Policies, third-party endpoint protection tools, or device control software.
-   In order to perform this action, you need to have the admin access to the device.
-   After you perform this action, restart the device for the access changes to take effect.

</td></tr><tr><td>

Restart Microsoft Outlook

</td><td>

Windows

</td><td>

Performing this action restarts Microsoft Outlook on the user's device.

</td></tr><tr><td>

Add a Registry Key

</td><td>

Windows

</td><td>

Performing this action adds a registry key to this device using a fully qualified path \(for example, `HKCU\Control Panel\TestColors\WindowText.`\), value \(for example,`2222`\), and type \(for example, String, DWord\). Windows registry key stores settings or configuration data for the device Operating system and Windows applications.

 **Note:**

-   The following types are supported:
    -   String – A null-terminated string. It can be Unicode or ANSI, depending on the function used.
    -   ExpandString – A null-terminated string with unexpanded environment variable references \(for example, %PATH%\).Use the ExpandEnvironmentStrings function to expand these references.
    -   DWord – A 32-bit number.
    -   QWord – A 64-bit number. Binary – Binary data in any form.
    -   Binary – Binary data in any form.
    -   MultiString – A sequence of null-terminated strings, terminated by an empty string \(\\0\). Example: String1\\0String2\\0String3\\0LastString\\0\\0. The final terminator must be included in the length.
-   To add a registry key value, you need to have the admin access to the device.

</td></tr><tr><td>

Modify a registry key value

</td><td>

Windows

</td><td>

Performing this action updates the registry key value using a fully qualified path \(for example, `HKCU\Control Panel\TestColors\WindowText.`\), value \(for example, `2222`\), and type \(for example, String, DWord\).

 **Note:**

-   The following types are supported:
    -   String – A null-terminated string. It can be Unicode or ANSI, depending on the function used.
    -   ExpandString – A null-terminated string with unexpanded environment variable references \(for example, %PATH%\).Use the ExpandEnvironmentStrings function to expand these references.
    -   DWord – A 32-bit number.
    -   QWord – A 64-bit number. Binary – Binary data in any form.
    -   Binary – Binary data in any form.
    -   MultiString – A sequence of null-terminated strings, terminated by an empty string \(\\0\). Example: String1\\0String2\\0String3\\0LastString\\0\\0. The final terminator must be included in the length.
-   To modify a registry key value, you need to have the admin access to the device.

</td></tr><tr><td>

Delete a file

</td><td>

Windows

</td><td>

Performing this action will permanently delete the entered file \(full file name or absolute file path\) from the user’s device. Proceed with caution when deleting critical system files.**Note:** Only one file can be entered at a time. The file name must include a valid extension \(for example, `.log`, `.txt`\).

</td></tr><tr><td>

Modify Device Battery Power Plan

</td><td>

Windows

</td><td>

Performing this action on the end-user’s device will adjust device power plan settings using PowerShell scripts to optimize performance, energy efficiency, and battery life.

</td></tr><tr><td>

Sync device to Intune

</td><td>

Windows

</td><td>

Performing this action on an end-user's device will sync the device on Intune.**Note:**

-   The minimum Microsoft Intune Spoke version required to run this action is 1.4.0.
-   For more information on sync device action, see [https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-syncdevice?view=graph-rest-1.0](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-syncdevice?view=graph-rest-1.0).


</td></tr></tbody>
</table><table id="table_f5n_gcl_cfc"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action name

</td><td>

Name of the action that is defined in the policy. Admins can predefine an action name so that SD agents don't need the policy ID to execute any action. The format is &lt;action&gt; &lt;application name&gt; &lt;version&gt;. For example, Reinstall Zoom 3.4.1 or Uninstall Firefox 134.2.

</td></tr><tr><td>

Active true/false

</td><td>

Enables the action to appear in action library.

</td></tr><tr><td>

Application

</td><td>

Identifies the application for which the policy is defined.

</td></tr><tr><td>

Policy ID

</td><td>

ID of the policy defined in Jamf server for the corresponding action.

</td></tr></tbody>
</table>**Parent Topic:**[Administration cards](administration-cards.md)

