---
title: View actions in the Digital End-User Experience Action Library
description: View and use various pre-installed services available for a device in the Digital End-User Experience Action Library.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Monitor, Digital End-User Experience, IT Service Management]
---

# View actions in the Digital End-User Experience Action Library

View and use various pre-installed services available for a device in the Digital End-User Experience Action Library.

## Before you begin

Role required:

-   sn\_dex.user
-   sn\_dex.admin
-   sn\_dex.service\_desk\_user and itil
-   sn\_dex.user
-   sn\_dex.engineer

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the **Devices** icon\(![Devices icon](../image/icon-devices.png)\) from the primary navigation pane.

2.  Select a device from the list.

3.  On the contextual side panel, select the Action Library icon \(![Action library icon](../image/icon-action-library.png)\) and view the following actions:

<table id="table_tfz_qq3_ggc"><thead><tr><th>

Action

</th><th>

Description

</th><th>

Local System account required

</th></tr></thead><tbody><tr><td>

Add a registry key

</td><td>

Adds a registry key to this device, which stores settings and configuration data for the device OS and apps.Windows only.

</td><td>

Yes

</td></tr><tr><td>

Clear application cache

</td><td>

Removes the stored application data, which forces the app to retrieve fresh files from the internet.The default applications that support clearing app cache are Microsoft Teams, Zoom, and Microsoft Outlook.

Use the dex\_action\_app\_config table to add more applications that support this action. Configure the corresponding cache URL to be cleared for each application in the same table. Separate cache URLs by a comma if entering multiple URLs for an app.

**Note:** Select the field auto-close, which closes the application before clearing the cache to confirm all the cache files are cleared.

</td><td>

Yes

</td></tr><tr><td>

Clear browser cache

</td><td>

Removes temporary data stored on your laptop, such as cookies and website files.

</td><td>

Yes

</td></tr><tr><td>

Clear DNS Cache

</td><td>

Clears the DNS cache.

</td><td>

 

</td></tr><tr><td>

Clear Google Chrome browsing data

</td><td>

Clears the browsing data, deleting all the saved addresses, payment methods, and auto-fill data.

</td><td>

 

</td></tr><tr><td>

Clear Recycle Bin

</td><td>

Clears contents of the recycle bin on the device.

</td><td>

Yes for Windows

</td></tr><tr><td>

Delete a file

</td><td>

Permanently deletes the specified file.Submit one file at a time for deletion.

</td><td>

 

</td></tr><tr><td>

Delete Network Drive

</td><td>

Removes a mapped network drive from your system and disconnects access to the shared location.

</td><td>

 

</td></tr><tr><td>

Elevate temporary admin access

</td><td>

Provides temporary administrative privileges to perform specific tasks.

</td><td>

Yes for Windows

</td></tr><tr><td>

End process

</td><td>

Forcefully stops a running process.

</td><td>

Yes

</td></tr><tr><td>

Map Network Drive

</td><td>

Connects a shared network location to a local drive letter for an easy access to the device files and folders.Windows only.

</td><td>

 

</td></tr><tr><td>

Modify a registry key value

</td><td>

Updates the value of the registry key monitored on the device.Windows only.

</td><td>

Yes

</td></tr><tr><td>

Modify Device Battery Power Plan

</td><td>

Adjusts device power plan settings using PowerShell scripts to optimize performance, energy efficiency, and battery life.Windows only.

</td><td>

 

</td></tr><tr><td>

Configure device power scheme

</td><td>

Configures the power scheme settings and optimizes the performance, energy efficiency, and battery life of the device.macOS only.

</td><td>

 

</td></tr><tr><td>

Modify USB storage access: Execute

</td><td>

Modifies the Execute permission, which enables programs or scripts to run directly from the USB storage device.

</td><td>

Yes

</td></tr><tr><td>

Modify USB storage access: Read

</td><td>

Modifies the Read permission enabling the device to read directly from the USB storage device.

</td><td>

Yes

</td></tr><tr><td>

Modify USB storage access: Write

</td><td>

Modifies the Write permission enabling the device to write directly to the USB storage device.

</td><td>

Yes

</td></tr><tr><td>

Perform disk cleanup

</td><td>

Deletes the temporary internet, memory, log, and cache files, similar to the following:-   `C:\Windows"="*.dmp`
-   `"C:\Windows\Downloaded Program Files"="*.*"`
-   `"$env:UserProfile\Appdata\Local\Microsoft\Windows\Temporary Internet Files"="*.*"`
-   `"C:\Windows\Temp"="*.*"`
-   `"C:\Windows\System32\LogFiles"="*.*"`
-   `"C:\ProgramData\Microsoft\Windows\WER\ReportQueue"= "*.*"`
Windows only.

</td><td>

 

</td></tr><tr><td>

Remediate Zscaler connectivity

</td><td>

Fixes any connectivity issues with Zscaler Private Access.

</td><td>

Yes

</td></tr><tr><td>

Repair corrupt Outlook files

</td><td>

Detects and repairs OST and PST file types in Microsoft Classic Outlook to help enhance its performance and synchronization.

</td><td>

Yes

</td></tr><tr><td>

Reset Google Chrome browser settings

</td><td>

Resets Google Chrome browser settings.

</td><td>

 

</td></tr><tr><td>

Restart Audio Services

</td><td>

Restarts audio services to restore sound and microphone functionality, fixing common playback and recording issues on the device.

</td><td>

Yes

</td></tr><tr><td>

Restart Microsoft OneDrive

</td><td>

Restart Microsoft OneDrive to resolve any synchronization issues and update all recent changes.The device user must be signed in to Microsoft OneDrive for this action.

</td><td>

Yes for Windows

</td></tr><tr><td>

Restart Microsoft Outlook

</td><td>

Restarts Microsoft Outlook on the device.

</td><td>

Yes

</td></tr><tr><td>

Execute Jamf policy

</td><td>

Execute the Jamf policy either with a policy ID or with a predefined action. Predefined actions, configured by DEX admins in the `dex_jamf_policy_table`, can be selected and executed by service desk agents, who don’t have access to the policy IDs. The predefined actions must be set in the table `dex_jamf_policy` and update the fields Action name, Application, Policy ID, and Active. The detailed information on the fields is listed in the following table.macOS only.

</td><td>

 

</td></tr><tr><td>

Restart service

</td><td>

Restarts the service or application running on the device.

</td><td>

Yes

</td></tr><tr><td>

Uninstall an application

</td><td>

Uninstalls the chosen application from the action library.Only applications installed via .exe or .msi files can be uninstalled. Core OS and system applications don’t get uninstalled, even if the action is executed successfully.

</td><td>

Yes

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
</table>    The following are the Jamf limitations:

    -   As DEX Admin, you must know the Jamf pro features and have knowledge about the policies configured for applications at the customer Jamf server.
    -   Some policies when run, notify the user to update the application instead of automatically updating it. For example, Zoom doesn't automatically update. In cases like these, the policy is executed successfully only if the employee approves the update of the application. Otherwise, the remedial action execution fails.

