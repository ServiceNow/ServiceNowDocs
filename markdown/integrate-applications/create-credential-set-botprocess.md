---
title: Create a robot credential in RPA Hub
description: Create a robot credential so that the unattended robot can log in to a Windows machine and perform the automation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [authenticate unattended robot rpa hub, authenticate bot rpa hub, unattended robot authentication rpa hub, bot authentication rpa hub]
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# Create a robot credential in RPA Hub

Create a robot credential so that the unattended robot can log in to a Windows machine and perform the automation.

## Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](create-botprocess-config.md#), and [Bot Process form in RPA Hub](select-botprocess.md#).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## About this task

You can't delete a robot credential if it’s associated with any credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

You can't edit the **Robot Username** field when the life-cycle stage status of the associated bot process is set to **Published**. You can edit the password irrespective of what the life-cycle stage is of the associated bot process. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

You can't edit the **External Credential** field when the life-cycle stage status of the associated bot process is set to **Published**.

If a robot credential uses an external credential vault, you must make sure that the associated external credential vault is active.

In RPA Hub, you can retrieve the robot credentials, application credentials, or a Time-based One-time Password \(TOTP\) seed in two ways:

-   From a ServiceNow credentials record \(application credential, robot credential, or TOTP authenticator\).
-   From an external credential vault. For more information, see [External credential vault in RPA Hub](../concept/external-credentials-rpa.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Robot Credentials**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the robot credential.

</td></tr><tr><td>

Authentication Type

</td><td>

The type of authentication for the robot login:-   **Windows Credentials** - Uses Windows username and password for robot authentication.
-   **Smart Card** - Uses user principle name \(UPN\) and smart card PIN for robot authentication.


</td></tr><tr><td>

Robot Username

</td><td>

For **Windows Credentials** - User name of the Windows machine to be used by the robot.Enter the user name in the `DOMAIN\Username` format.

For **Smart Card** - User principle name \(UPN\) to be used by the robot.

This field doesn’t appear if the **External Credential** option is selected.

</td></tr><tr><td>

Robot Password

</td><td>

For **Windows Credentials** - Password for the Windows machine to be used by the robot.For **Smart Card** - Smart card PIN to be used by the robot.

This field doesn’t appear if the **External Credential** option is selected.

</td></tr><tr><td>

External Credential

</td><td>

Option that you can select to fetch the credentials from the external credential vaults.External credential is not supported for Smart Card.

</td></tr><tr><td>

External Credential Vault

</td><td>

External credential vault record that is used for fetching the credentials from an external credential vault.Use the search icon to select an external credential vault record. For example, DemoCyberArk.

Only active external credential vault records are listed here.

This field appears only when the **External Credential** option is selected.

</td></tr><tr><td>

Subflow Input

</td><td>

JSON that acts as an input to the subflow mapped in the selected external credential record. This JSON is used by the Subflow REST Step and must contain the necessary information for retrieving the credentials from the external credential vault.

The value must be in a JSON format. You can't enter an empty JSON value.

For more information about the JSON, see [Steps to configure an external credential vault in RPA Hub](../reference/config-ext-cred-rpa.md).

This field appears only when the **External Credential** option is selected.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


