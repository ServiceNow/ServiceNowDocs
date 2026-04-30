---
title: Windows credentials
description: Windows credentials provide access to Windows computers. This credential type is available for Discovery and Orchestration.Configure the MID Server to use either the credentials of its own Windows service or credentials from the Credentials \[discovery\_credentials\] table.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2025-11-04"
reading_time_minutes: 5
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# Windows credentials

Windows credentials provide access to Windows computers. This credential type is available for Discovery and Orchestration.

## Credential requirements

Discovery and Orchestration have the following requirements for Windows credentials:

-   Install a MID Server on a Windows host as a service.
-   Add Windows credentials to one of these locations:
    -   An entry in the Credentials `[windows_credentials]`table
    -   A MID Server service account to run as a specific Windows user or domain account.

## Granting proper permissions

To provide sufficient permissions, Windows credentials must be one of the following:

-   A domain user with local administrator access on the target Windows hosts.

    **Important:** If User Account Control \(UAC\) is enabled on the Windows operating system where discovery runs, and the user account is part of the local Administrators group, administrator tasks may fail. To avoid interruptions, we recommend disabling UAC. For more information, see the [Why does the User Access Control \(UAC\) need to be disabled for Windows Discovery?](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638330) article in the Now Support Knowledge Base

-   A local account that has administrator privileges and UAC disabled on the same target host.
-   A user who meets the requirements of Windows [probes and permissions](https://www.servicenow.com/docs/access?context=r_DiscoWinProbesAndPermissions&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) \(Discovery only\).
-   A user who meets the requirements of the Orchestration activity to be run \(Orchestration only\).

**Note:** No logon privileges are needed. Account does NOT need to be interactive.

Security around granting privileged access can be enhanced by using JEA profiles to run Discovery. For more information, see [Microsoft Just Enough Administration \(JEA\) for Discovery](https://www.servicenow.com/docs/access?context=microsoft-jea-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Workgroup computers

To run Powershell commands to discover a Workgroup computer, configure the MID Server credentials for either of these users:

-   Built-in administrator account on the Workgroup computer.
-   Domain user on the Workgroup computer.

## Multi-domain configuration

To enable Windows credentials to function across multiple domains, make sure to sure to use the correct name formats and MID Server configuration.

Discovery and Orchestration support Windows domain credentials in both **User Principal Name** and **Down-Level Logon Name** user name formats. For example, **Domain\\UserName** or **UserName@example.domain.com**. You can provide Windows workgroup credentials in the following format: WORKGROUP\\UserName.

**Note:** You can also provide a local account by using the **. \\** user name.

These additional actions are required to enable credentials to function across multiple Windows domains.

|Condition|Additional actions required|
|---------|---------------------------|
|MID Server host on the same domain as the Windows target.|None|
|MID Server host on a different domain than the Windows target.|Ensure that PowerShell 3.0 \(or higher up to 5.1\) is installed on the MID Server host.|
|MID Server host on a different domain than the Microsoft SQL Server target.|See [MSSQL server discovery](https://www.servicenow.com/docs/access?context=mssql-data-collected-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) .|

## Windows credentials type

These fields are available in the Credentials form for Windows:

<table id="table_i3p_jjv_2y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter the user name to create in the Credentials table. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name. For CIM discovery, the user must have the admin role.

</td></tr><tr><td>

Password

</td><td>

Enter the password.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential system. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.To use the credential for discovering CIs not belonging to this CI type using Service Mapping and Discovery patterns, enter the table name for the CI type to which the CI belongs, for example cmdb\_ci\_apache\_web\_server.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. [External credential storage](../concept/c_ExternalCredentialStorage.md) is only available when the External Credential Storage plugin in activated. **Note:** Currently, the only supported external storage system is [CyberArk](../concept/c_CyberArkCredStorageIntegrate.md).

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.**Note:** Selecting Specific **Specific MID servers** doesn’t affect mid server selection. It’s used only to decide which mid servers should have visibility to the credential. **Specific MID servers** isn’t supported in Orchestration activities.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

Windows MID Server Service Account

</td><td>

When active, the defined credential represents the MID Server service account.

</td></tr></tbody>
</table>## Configure Windows credentials for the MID Server

Configure the MID Server to use either the credentials of its own Windows service or credentials from the Credentials \[discovery\_credentials\] table.

### Before you begin

Role required: admin

### Procedure

1.  Configure the MID Server to use credentials from the MID Server service account.

    1.  Set the [Configure Windows MID Server service credentials](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=zurich&pubname=zurich-servicenow-platform&section=t_ConfigMIDSvrSvcCredentials&ft:locale=en-US) to a user who meets the permission requirements.

    2.  Verify the user name meets the name format requirements.

    3.  Fill in the fields on the form, as appropriate.

    4.  Verify the credentials meet domain requirements.

2.  Configure the MID Server use credentials from the Credentials \[discovery\_credentials\] table.

    1.  Add individual Windows credentials to the Credentials `[windows_credentials]` table.

        -   Verify each credential meets the permission requirements.
        -   Verify each username meets the name format requirements.
        -   Verify each credential meets the Windows domain requirements.
    2.  Configure the MID Server to use Powershell by setting the `mid.use_powershell` parameter to **true**.

        See [Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    3.  Select the Windows MID Server Service Account check box to create a credential that represents the windows MID Server service account to run as a specific Windows user or domain account.


