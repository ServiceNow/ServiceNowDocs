---
title: Create an application credential in RPA Hub
description: Create an application credential to add the application user name and password. An unattended robot can use this application credential to log in to an application when the automation is executed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# Create an application credential in RPA Hub

Create an application credential to add the application user name and password. An unattended robot can use this application credential to log in to an application when the automation is executed.

## Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](create-botprocess-config.md#), and [Bot Process form in RPA Hub](select-botprocess.md#).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_business\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

You can't delete an application credential when the life-cycle stage status of the associated bot process is set to **Published**. For more information, see [Life-cycle stage statuses \(LLCS\) of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

You can't edit the **Name** and **Application Name** fields when the life-cycle stage status of the associated bot process is set to **Published**. You can edit the application password irrespective of what the life-cycle stage is of the associated bot process.

You can't edit the **External Credential** field when the life-cycle stage status of the associated bot process is set to **Published**.

If an application credential uses an external credential vault, make sure that the associated external credential vault is active.

In RPA Hub, you can retrieve the robot credentials, application credentials, or a Time-based One-time Password \(TOTP\) seed in two ways:

-   From ServiceNow credentials record \(application credential, robot credential, or TOTP authenticator\).
-   From an external credential vault. For more information, see [External credential vault in RPA Hub](../concept/external-credentials-rpa.md).

If the **External Credential** check box is selected in an application credential record, then the **SetApplicationCredential** component in RPA Desktop Design Studio doesn’t set the credentials and an error is displayed. For more information about the component, see [Use the SetApplicationCredential component](../../rpa-studio/task/use-credentials-setappcredential.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Application Credentials**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_lgf_nm1_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this application credential.

</td></tr><tr><td>

Application Name

</td><td>

Name of the business application. Alternatively, you can use the search icon and select the available business application.

</td></tr><tr><td>

User name

</td><td>

User name for the application.This field doesn’t appear if the **External Credential** option is selected.

</td></tr><tr><td>

Password

</td><td>

Password for the application.This field doesn’t appear if the **External Credential** option is selected.

</td></tr><tr><td>

External Credential

</td><td>

Option that you can select to fetch the credentials from the external credential vaults.This field doesn't appear to an RPA business user.

</td></tr><tr><td>

External Credential Vault

</td><td>

Option that you can for an external credential vault record that is used for fetching the credentials from an external credential vault.Use the search icon to select an external credential vault record. For example, DemoCyberArk.

Only the active external credential vault records are listed here.

This field appears only when the **External Credential** option is selected.

This field doesn't appear to an RPA business user.

</td></tr><tr><td>

Subflow Input

</td><td>

JSON that acts as an input to the subflow mapped in the selected external credential record. This JSON is used by the Subflow REST Step and must contain the necessary information for retrieving the credentials from the external credential vault.

The value must be in a JSON format. You can’t enter an empty JSON value.

For more information about the JSON, see [Steps to configure an external credential vault in RPA Hub](../reference/config-ext-cred-rpa.md).

This field appears only when the **External Credential** option is selected.

This field doesn't appear to an RPA business user.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Related topics**  


[View Audit History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HistorySets.md)

