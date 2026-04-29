---
title: PowerShell troubleshooting
description: Authentication and access denied errors can prevent PowerShell activities from running a command on a target host.This example uses the Create AD Object activity to illustrate troubleshooting authentication failure in PowerShell.This example uses the Create Mailbox activity to illustrate troubleshooting authentication failure in PowerShell.Typically, this error is logged when running a PowerShell script/command that uses WinRM or WMI.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [PowerShell protocols and troubleshooting, PowerShell activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# PowerShell troubleshooting

Authentication and access denied errors can prevent PowerShell activities from running a command on a target host.

Use these procedures for troubleshooting authentication failures with Orchestration PowerShell activities and when the Remote Procedure Call \(RPC\) server is unavailable or when access is denied. The authentication failure error displays when all credentials, including those of the local MID Server service account, do not have the correct permissions to run the Powershell script/command. The same error displays when the target host is unreachable.

![Authentication error message](../image/AuthenticationErrorMsg.png "Authentication error message")

**Parent Topic:**[PowerShell protocols and troubleshooting](../reference/powershell-protocols.md)

## Authentication failure in an Active Directory activity

This example uses the Create AD Object activity to illustrate troubleshooting authentication failure in PowerShell.

### Before you begin

Role required: Permissions to access and create accounts on Active Directory

### About this task

Validate that the account you are using has the proper permissions to run the activity.

### Procedure

1.  Log on to the target machine using the account under which you want to run the activity.

    Active Directory tools must be installed on this machine.

2.  Launch the Active Directory Users and Computers application.

3.  Navigate to the OU under which you want to create the Active Directory object.

4.  Attempt to create the object.

    If this procedure is successful under the specified user, the following might be the cause of the authentication failure:

    -   User name is invalid.
    -   Password entered incorrectly.
    -   Domain controller is unreachable.
    **Note:** The majority of the return codes listed in the MID Server log for this error are **1**s and **3**s. This is because the Active Directory activities use the ADSI provider and not WMI or WinRM. An error code of **1** means the account was able to connect with the test account, but running the script failed.

    ![Sample error code of 1](../image/ErrorCode1.png)

    An error code of **3** means that the MID Server attempted to run the PowerShell activity under the MID Server service account but failed.

    ![Sample error code of 3](../image/ErrorCode3.png)


## Authentication failure in an Exchange activity

This example uses the Create Mailbox activity to illustrate troubleshooting authentication failure in PowerShell.

### Before you begin

Role required: Permissions to access and create mailboxes on the Exchange server

### Procedure

1.  Validate that the account you are using has the proper permissions to run the PowerShell activity.

2.  Log on to a machine that has the Exchange Management Shell \(EMS\) installed.

3.  Create a user using the `New-mailbox` Exchange commandlet.

    ![Creating a new user in Exchange](../image/ExchangeCommandConsole.png "Creating a new user in Exchange")

    If this procedure is successful under the specified credential, the following is the likely cause of the failure:

    -   User name is invalid.
    -   Password entered incorrectly.
    -   Exchange server is unreachable.
4.  If the Exchange server is unreachable, examine the MID Server logs.

    Because the Exchange activities use WinRM to access the Exchange server, the logs can provide more troubleshooting information.

    **Note:** Ensure that the error is NOT **WinRM cannot process the request**.


## Remote Procedure Call \(RPC\) server unavailable or access denied

Typically, this error is logged when running a PowerShell script/command that uses WinRM or WMI.

### Possible causes of error

The target host might have one of these issues:

-   WinRM isn’t configured.
-   Firewall is blocking access to the host over TCP port 135 \(WMI\) or HTTP/HTTPs and TCP port 5985 \(WinRM\).
-   Kerberos issue, caused by hopping to multiple hosts using WMI.

### Example WinRM error

The Create Mailbox activity from the Exchange activity pack has generated an error in the ECC queue involving authentication using the MID Server service credential. This occurred because the MID Server credential is the last to be used if the targeted host is not the MID Server.

![Authentication failure error message](../image/AuthenticationErrorMsg.png "Authentication failure error message")

The MID Server log shows that the MID Server tried to run the activity under specific credentials, but wasn’t successful and received an exit code of 1.

![MID Server error code](../image/MIDServerErrorCode.png "MID Server error code")

