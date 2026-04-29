---
title: Mapping application services containing Microsoft Exchange Server
description: Service Mapping can discover service instances containing a Microsoft Exchange Server and the Exchange Server components.Map an application service containing an Microsoft Exchange Server and verify that Service Mapping discovered all Microsoft Exchange Server components correctly.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Mapping application services containing Microsoft Exchange Server

Service Mapping can discover service instances containing a Microsoft Exchange Server and the Exchange Server components.

## Discovered components

If e-mail services in your organization deploy Microsoft Exchange Server, the discovered application service includes the following components:

<table id="SupportedApplications"><thead><tr><th>

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

Microsoft Active Directory Domain Services

</td><td>

Windows

</td><td>

13, 30, 31, 44, 47, 52, 56, 69

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Active Directory Service pattern

</td></tr><tr><td>

[Microsoft server \(as a Microsoft Exchange component\)](../../discovery/reference/r-ExchangeClientAccessServer.md)

</td><td>

Windows

</td><td>

2003, 2007, 2010, 2013, 2016

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

ExchangeFrontEndServer On Windows; PatternExchangeBackEndServer On Windows pattern

</td></tr><tr><td>

[HUB Transport Server \(as a Microsoft Exchange component\)](../../discovery/reference/r-ExchangeHub.md)

</td><td>

Windows

</td><td>

2003, 2007, 2010, 2013, 2016

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

Hub Transport Server On Windows pattern

</td></tr><tr><td>

Client Access Server \(CAS\) \(as a Microsoft Exchange component\)

</td><td>

Windows

</td><td>

2003, 2007, 2010, 2013, 2016

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

CAS On Windows pattern

</td></tr></tbody>
</table>Typically, you do not want to discover Outlook clients connected to the Exchange Server to avoid noise. If this is the case, disable the traffic-based discovery for this application service.

For information on the discovery flow, refer to pattern-based discovery in Service Mapping. Failure to provide users with required permissions may cause Service Mapping to perform [traffic-based discovery](traffic-based-discovery.md).

## Limitations

Discovery and Service Mapping cannot discover the Exchange Server if its configuration does not support public folders, edge transports, and public messaging. Create a pattern or customize the existing pattern to discover the Exchange Server with such configuration.

**Parent Topic:**[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

## Map application services containing Microsoft Exchange Servers

Map an application service containing an Microsoft Exchange Server and verify that Service Mapping discovered all Microsoft Exchange Server components correctly.

### Before you begin

-   On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). Use the Microsoft Exchange Server administrator's user name and password as Windows credentials. For example, user name: local\\administrator and password: Are1300.

    **Note:** If you configure Windows credentials for a user different from the Microsoft Exchange Server administrator, Service Mapping uses traffic-based discovery that results in mapping all Microsoft Exchange clients.

-   \(For Exchange CAS 2010 and 2013, 2016\) On the ServiceNow AI Platform, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US), setting the CI type to Exchange Mailbox.

    **Warning:** Do not confuse the Exchange Mailbox CI type with the Exchange Mailbox Server CI type.

    Service Mapping uses these applicative credentials to access the of/Servers/Servers.slab folder on the Key Exchange Admin Center \(EAC\). Service Mapping also uses the applicative credentials to run the following PowerShell commands against the MID Servers:

    -   Get-ExchangeServer
    -   Get-ExchangeServer
    -   Get-MailboxServer
    -   Get-ClusteredMailBoxServerStatus
    -   Get-ExchangeServer
    -   Get-StorageGroup
    -   Get-MailboxDatabase
-   \(For Microsoft Exchange CAS 2010 and 2016\) On the Windows Server hosting Microsoft Exchange CAS, install the Microsoft.Exchange.Management.PowerShell.E2010 module.
-   \(For Microsoft Exchange CAS 2007\) On the Windows Server hosting Microsoft Exchange CAS, install the Microsoft.Exchange.Management.PowerShell.Admin module.
-   \(For Microsoft Exchange CAS 2007, 2010\) On the ServiceNow AI Platform, upload the rctrlx tool for running PowerShell commands as described in [Upload the rctrlx.exe file to MID Servers](../task/upload-rctrlx-file.md).
-   \(For Microsoft Exchange CAS 2007 and 2010\) Provide an Exchange Mailbox OS user with the rights to run Exchange services on Windows and has permission to query Exchange repository:

    On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) setting the **Credential alias** attribute to \[cmdb\_ci\_exchange\_mailbox\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   Verify that you know the entry point necessary for discovering the Microsoft Exchange Server. Use the URL for the Outlook web access in the following format:

    `http(s)://<hostname>:<port>/owa`

    For example, `http(s)://myhost:<443>/owa`


Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Select **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this service instance:

    1.  Select the **Web Application** tile.

        The **Discoverable by Service Mapping** option is selected by default.

    2.  In the **URL** field, enter the URL of the Outlook web access.

        For example, http\(s\)://myhost:&lt;443&gt;/owa.

    3.  Click **Add**.

    4.  Click **Save**.

3.  Click **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Click **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Click **View Map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map and make sure that the service layout is as in the examples below.

        ![Check the result of mapping an application service containing the Microsoft Exchange Server.](../image/CheckResultExchangeServer.png)


If the mapping result is not as you expected, perform basic troubleshooting.

<table id="table_kjv_sdy_32b"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery failed. The discovery log displays the message that starts with the following text: You must have the Exchange Common Commands PowerShell Snapin installed to use this script.

</td><td>

The indication sections of the pattern fail, because the user does not have permissions for running PowerShell commands.

</td><td>

Make sure that you provided a user with permissions to run PowerShell commands on servers that host Microsoft Exchange Server components, for example, CAS.

</td></tr><tr><td>

Discovery failed. The discovery log displays the error message that starts with the following text:\[servername.destination.com\] Connecting to remote server failed with the following error message: The WinRM client can not process the request. The authentication mechanism requested by the client is not supported by the server or unencrypted traffic is disabled in the service configuration. Verify the unencrypted traffic setting in the service configuration or specify one of the authentication mechanisms supported by the server.

</td><td>

The indication sections of the pattern fail, because the MID Server is not configured as a trusted host on the component you are discovering.

</td><td>

Add the MID Server to the list of trusted hosts on all hosts that you want to discover.

</td></tr><tr><td>

The application service map is very large, because it includes connections to all Outlook clients.

</td><td>

\(In deployments using Microsoft Exchange Server 2007, 2010 or 2013\), Service Mapping created connections using traffic-based discovery, which traces all open connections, instead of using PowerShell commands.

</td><td>

Make sure that you provided a user with permissions to run PowerShell commands on servers that host Microsoft Exchange Server components, for example, CAS.

</td></tr></tbody>
</table>