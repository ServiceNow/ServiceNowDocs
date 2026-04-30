---
title: Configure Microsoft Endpoint Configuration Manager and set up the spoke
description: Follow the Microsoft Endpoint Configuration Manager configuration procedures in the order shown.Ensure that the Microsoft Endpoint Configuration Manager administrative user has the correct permissions to deploy software and that PowerShell is properly configured.Ensure that the Microsoft Endpoint Configuration Manager Cmdlet Library is up-to-date.Integrate the ServiceNow instance and Microsoft Endpoint Configuration Manager account using the PowerShell and JDBC credentials to authenticate ServiceNow requests.Create a connection record for your Microsoft Endpoint Configuration Manager. The Microsoft Endpoint Configuration Manager connection and credential aliases use these connections to perform actions in Microsoft Endpoint Configuration Manager.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Microsoft Endpoint Configuration Manager Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure Microsoft Endpoint Configuration Manager and set up the spoke

Follow the Microsoft Endpoint Configuration Manager configuration procedures in the order shown.

**Note:** Ensure that user must be able to establish remote PowerShell sessions with the MECM server. The spoke scripts use **Microsoft.PowerShell32** configuration for creating sessions. For user permissions, see [User permissions](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_remote_requirements?view=powershell-7.4#user-permissions) in [Microsoft Learn](https://learn.microsoft.com/en-us/).

## Configure the Application Administrator role on the Microsoft Endpoint Configuration Manager server

Ensure that the Microsoft Endpoint Configuration Manager administrative user has the correct permissions to deploy software and that PowerShell is properly configured.

### Before you begin

Role required: Microsoft Endpoint Configuration Manager Application Administrator

### About this task

These instructions are for Microsoft Windows Server 2016 Standard.

### Procedure

1.  In the Microsoft Endpoint Configuration Manager console, navigate to **Administration** &gt; **Security** &gt; **Administrative Users**.

2.  Right-click the user to whom you want to grant the Application Administrator role.

3.  Select **Properties** from the drop-down menu.

4.  In the Properties dialog box, select the **Security Roles** tab.

5.  Ensure that the user has the Application Administrator role.

6.  If the user does not already have this role, click **Add**, select this role from the list, and click **OK**.

    ![Granting the deployment role on the Microsoft Endpoint Configuration Manager server.](../image/SCCMConsole.png "Granting the Application Administrator role on the Microsoft Endpoint Configuration Manager server")

7.  Log into Microsoft Endpoint Configuration Manager as the user with the Application Administrator role.

8.  Open the menu from the upper left corner of the console and select **Connect via Windows PowerShell**.

    ![Connect to PowerShell.](../image/ConnectSCCMviaPowerShell.png "Connect to PowerShell")

9.  Ensure that the user can access the CM console.

    This action establishes the environment path to PowerShell for the logged in Application Administrator user.


## Update the Microsoft Endpoint Configuration Manager cmdlet libraries

Ensure that the Microsoft Endpoint Configuration Manager Cmdlet Library is up-to-date.

### Before you begin

Role required: Either Microsoft Endpoint Configuration Manager current user or system administrator, depending on settings.

### About this task

The Microsoft Endpoint Configuration Manager Cmdlet Library installs and updates the Windows PowerShell module. Microsoft Endpoint Configuration Manager checks for library updates on a daily basis. Out-of-date libraries can cause Discovery of the Microsoft Endpoint Configuration Manager server to fail, because the system cannot parse the Microsoft Endpoint Configuration Manager activity output. This is an example warning message.

```
WARNING: An update to the 
            Microsoft Endpoint Configuration Manager Cmdlet
Library is available. Please go to
'http://go.microsoft.com/fwlink/?LinkId=528947' to download the latest version.
Running cmdlet version: 5.0.8231.1004 Latest cmdlet version: 5.0.8328.1155
```

Download the latest version of the cmdlet library from [http://go.microsoft.com/fwlink/?LinkId=528947](http://go.microsoft.com/fwlink/?LinkId=528947). For installation instructions, see [https://technet.microsoft.com/en-us/library/dn958404\(v=sc.20\).aspx](https://technet.microsoft.com/en-us/library/dn958404(v=sc.20).aspx).

If you elect to use an earlier version library, use this procedure to disable the CM update check, which allows Discovery to proceed without issues.

### Procedure

1.  Log in to the Microsoft Endpoint Configuration Manager console as an administrator.

2.  Open the menu from the upper left corner of the console.

3.  Select **Connect via Windows PowerShell**.

4.  Run one of these commands to disable the update check:

    -   **Per-user**: `Set-CMCmdletUpdateCheck -CurrentUser -IsUpdateCheckEnabled 0`
    -   **Per-system**: `Set-CMCmdletUpdateCheck -System -IsUpdateCheckEnabled 0`
    **Important:** The per-system cmdlet must run in an elevated Windows PowerShell session.

5.  Run the `Get-CMCmdletUpdateCheck` command to refresh the console and check the settings.

6.  Ensure that the value of the *IsEnabled* configuration variable has changed to **False**.

    This indicates that the warning for an out of date cmdlet library is disabled for the users specified.

7.  To re-enable the update check, run the `-IsUpdateCheckEnabled 1` command for either the current user or for the system.


## Set up the Microsoft Endpoint Configuration Manager spoke

Integrate the ServiceNow instance and Microsoft Endpoint Configuration Manager account using the PowerShell and JDBC credentials to authenticate ServiceNow requests.

### Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Endpoint Configuration Manager spoke.
-   Role required: admin.

### Procedure

1.  Configure the default connection and credential alias to authenticate requests.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the record **Microsoft Endpoint Configuration Spoke**.

    3.  Click the **Create New Connection &amp; Credential** related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Server Instance Name|Name of the Microsoft Endpoint Configuration Manager server.|
        |Host|Provider domain name.|
        |Credential Name|Name to identify the credential record.|
        |User Name|User name to log in to the Microsoft Endpoint Configuration Manager server.|
        |Password|Password to log in to the Microsoft Endpoint Configuration Manager server.|

    5.  Click **Create**.

2.  To use the two advanced actions, Look up Device Collections Stream \(Database\) and Look up User Collections Stream \(Database\), configure the JDBC credential.

    **Note:** If you are using the Microsoft Endpoint Configuration Manager spoke with [Client Software Distribution 2.0 application](csd-app-2.md), you must configure the JDBC credential.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Open the record **Microsoft Endpoint Configuration JDBC**.

    3.  Click the **Create New Connection &amp; Credential** related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to identify the JDBC connection record. For example, `JDBC Connection`.|
        |Host|Host name or IP address of the database server.|
        |Database name|Name of the database.|
        |Credential Name|Name to identify the connection record. For example, `JDBC Credentials`.|
        |User name|User name to log in to the JDBC database. Ensure that the user role is at least public with db\_datareader.|
        |Password|Password to log in to the JDBC database.|

    5.  Click **Create**.

        If the MecmConnector jar is not present on the MID Server, restart the MID server so that the jar file gets synchronised from the instance to the MID server.


### What to do next

To use the Microsoft Endpoint Configuration Manager spoke with [Client Software Distribution 2.0 application](csd-app-2.md), see [CSD 2.0 for Microsoft Endpoint Configuration Manager](csd2.md).

## Create a connection and credential record for the Microsoft Endpoint Configuration Manager spoke REST actions

Create a connection record for your Microsoft Endpoint Configuration Manager. The Microsoft Endpoint Configuration Manager connection and credential aliases use these connections to perform actions in Microsoft Endpoint Configuration Manager.

### Before you begin

-   To get the **Realm** value from the Microsoft Endpoint Configuration Manager server, do the following:
    1.  Open **Programs** &gt; **Administrative Tools** &gt; **Active Directory Management**.
    2.  Select **Active Directory Domains and Trusts**.

        The Active Directory domain names are listed. The Active Directory domain name is also the related Kerberos realm name and DNS domain name. Select the domain that you want to use for integration.

-   After getting Realm details, run the following command from the Command Line to get the Key Distribution Center value.

    `nslookup -type=srv _kerberos._tcp.<REALM_NAME_IN_UPPER_CASE>`

    Copy the `svr hostname` value from the list and use it as the **Key Distribution Center** value.

-   Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **Microsoft Endpoint Configuration REST**.

3.  From the **Related Links** tab, click **Create New Connection &amp; Credential**.

4.  On the form, fill these fields.

<table id="table_jrn_bmv_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection. For example, `MS Endpoint Configuration Manager REST Connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to **Microsoft Endpoint Configuration Manager**. Enter: `https://<computer_name>.com`

</td></tr><tr><td>

Credential Name

</td><td>

Credential record created for Microsoft Endpoint Configuration Manager. For example, `MS Endpoint Configuration Manager Cred`.

</td></tr><tr><td>

User Name

</td><td>

User name to connect to your Microsoft Endpoint Configuration Manager account.**Note:** You must provide the user name without prefixing with the domain name.

</td></tr><tr><td>

Password

</td><td>

Password to connect to your Microsoft Endpoint Configuration Manager account.

</td></tr><tr><td>

Key Distribution Center

</td><td>

Key distribution center of the Microsoft Endpoint Configuration Manager server.

</td></tr><tr><td>

Realm

</td><td>

Active Directory domain name in uppercase from the Microsoft Endpoint Configuration Manager server. For example, `OPS.LAB3.EXAMPLE.COM`

</td></tr></tbody>
</table>    **Note:** If either Key Distribution Center or Realm values is changed in the credential record, make sure to restart the MID server to sync the update. Because Key Distribution Center and Realm values are set as JRE properties on MID server.

5.  Click **Submit**.


### What to do next

Before using any REST based actions, make sure the MID JAR file, MecmConnector, is present at `<MID Folder>\agent\extlib` on MID server.

