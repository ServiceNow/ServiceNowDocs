---
title: Mapping application services containing Citrix XenApp and Presentation Server
description: Service Mapping can discover application services containing Citrix XenApp, Presentation Server, and Citrix Usage Collector.Map an application service containing Citrix XenApps, Presentation Servers, and Citrix Usage Collectors and verify that Service Mapping discovered all Citrix components correctly.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Mapping application services containing Citrix XenApp and Presentation Server

Service Mapping can discover application services containing Citrix XenApp, Presentation Server, and Citrix Usage Collector.

## Discovered components

<table id="table_vnn_x21_4fb"><thead><tr><th>

Name

</th><th>

Platform

</th><th>

Version

</th><th>

Protocol

</th><th>

Discovery type

</th><th>

Pattern \(or probe if indicated\)

</th></tr></thead><tbody><tr><td>

Citrix XenApp Server

</td><td>

Windows

</td><td>

6.x&gt;6.5, 7.x&lt;7.6

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

Citrix XenApp or Presentation Server

</td></tr><tr><td>

Citrix Presentation Server

</td><td>

Windows

</td><td>

4.x, 5.x, 6.x&lt;6.5

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

Citrix XenApp or Presentation Server

</td></tr><tr><td>

Citrix Usage Collector

</td><td>

Windows

</td><td>

7.x&gt;7.5, 8.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Citrix Collector

</td></tr><tr><td>

Generic application based on the Icon Path

</td><td>

Windows

</td><td>

-

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Citrix Application Icon Path

</td></tr></tbody>
</table>**Parent Topic:**[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

## Map application services containing Citrix XenApp and Presentation Server

Map an application service containing Citrix XenApps, Presentation Servers, and Citrix Usage Collectors and verify that Service Mapping discovered all Citrix components correctly.

### Before you begin

-   Provide a user with permissions to read and query the Citrix repository:
    -   For versions 4.5 and later, a PowerShell script from the XenApp server.
    -   For versions earlier than 4.5, a Microsoft Visual Basic Script \(VBScript\) from the Citrix Presentation Server
-   On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    **Note:** To use this credential later for XenAPP, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_xenapp. To use this credential later for Citrix, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_collector.

-   \(Optional\) To discover using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   Configure a user with permissions to run PowerShell commands on the Citrix server.
-   \(For discovery of Citrix Presentation Server only\) Find out the icon path for the entry point:
    1.  In the Citrix Access Management Console, navigate to **Presentation Server** &gt; **Applications**.
    2.  Locate the Icon Path folder in the navigation tree.
    3.  Right-click the Icon Path folder and click **Copy path**.
-   \(For discovery of Citrix XenApp Server only\) Find out the icon path for the entry point by checking the Distinguish Name attribute for the Icon Path.

Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Click **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this service instance:

    1.  Select the **Citrix XenApp** tile.

    2.  Define entry point attributes.

        |Attribute|Description|
        |---------|-----------|
        |Host|The URL of the Citrix XenApp or Presentation Server. The URL must contain a VIP IP or a physical host.|
        |Port|The port that the Citrix XenApp or Presentation Server uses on the host.|
        |Icon Path|The path to the logical application location as it appears in the Citrix Access Management Console. The path must start with the Applications folder. For example, /Application/Jane/Windows Media Player.|
        |URL|The URL must contain a VIP IP or a physical host. For example, http://&lt;host&gt;/Citrix/StoreWeb.|

    3.  Click **Add**.

    4.  Click **Save**.

3.  Click **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Click **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Click **View map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map and make sure that it resembles in the following example.

        ![Check the result of mapping an application service containing the XenApp Servers and other environment components.](../image/Citrix-XenApp-top-down-map.png)


If the mapping result is not as you expected, perform basic troubleshooting.

<table id="table_kjv_sdkwo0_3556"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery failed. The discovery log displays the message that starts with the following text: You do not have sufficient permissions.

</td><td>

The indication sections of the pattern fail, because the user does not have permissions for running PowerShell commands.

</td><td>

Make sure that you provided a user with permissions to run PowerShell commands on servers that host Citrix XenApp, Presentation Server, or Citrix Usage Collector.

</td></tr><tr><td>

Discovery failed. The discovery log displays the error message that includes the following text:CategoryInfo : NotSpecified: \(:\) \[\], PSSecurityException+ FullyQualifiedErrorId : RuntimeException

</td><td>

The MID Server cannot run PowerShell commands remotely, because the execution policy is set to RemoteSigned on the target servers.

</td><td>

Use the `set-executionpolicy remotesigned` command on the target servers to enable the MID Server to successfully run PowerShell commands.

</td></tr><tr><td>

Discovery failed. The discovery log displays the error message that includes the following text:Import-XAFarm : The Citrix Common Commands PowerShell Snapin is not installed

</td><td>

The target host does not have this PowerShell library: Citrix Common Commands PowerShell Snapin.

</td><td>

Download and install PowerShell SDK for Citrix XenApp on all servers hosting Citrix XenApp, Presentation Server, or Citrix Usage Collector.

</td></tr><tr><td>

The application service map shows the Citrix Delivery Controller, but does not include the Citrix XenApp, Citrix Presentation Server or Citrix Usage Collector.

</td><td>

The icon path you defined is incorrect.

</td><td>

Verify the icon path and reenter it in the entry point attributes for the application service.

</td></tr></tbody>
</table>