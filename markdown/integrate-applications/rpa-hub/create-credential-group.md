---
title: Create a credential group in RPA Hub
description: Create a credential group to include a robot credential and application credentials that you can reuse in multiple bot processes. Unattended robots leverage the credential group to perform an automation that you defined in the associated bot process.Associate one or more application credentials to the credential group in RPA Hub so that a robot can perform automation by logging in to the applications.Associate one or more unattended bot processes to a credential group in RPA Hub so that the associated robot can perform automation using the credential group.Provide access to either all users or specific users in the Managed by group of the associated bot processes in RPA Hub. This way, you can make sure that the correct users have access to the credentials.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Configuring credentials in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Create a credential group in RPA Hub

Create a credential group to include a robot credential and application credentials that you can reuse in multiple bot processes. Unattended robots leverage the credential group to perform an automation that you defined in the associated bot process.

## Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Create a robot credential. For more information, see [Create a robot credential in RPA Hub](create-credential-set-botprocess.md).

Create one or more application credentials. For more information, see [Create an application credential in RPA Hub](create-application-credential.md).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Credential Groups**.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the credential group.|
    |Robot Credential|Robot credential to be associated with this credential group. Robots use the robot credentials to authenticate on a system.|

6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Related topics**  


[Associate a credential group to a bot process](map-credential-groups-to-bot-process.md)

[Assign a process robot credential within a bot process](assign-process-robot-cred-botprocess.md)

## Associate an application credential to the credential group

Associate one or more application credentials to the credential group in RPA Hub so that a robot can perform automation by logging in to the applications.

### Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Create a credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

Create application credentials. For more information, see [Create an application credential in RPA Hub](create-application-credential.md).

Developers can only associate application credentials that are created by them to the credential group.

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

### Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Credential Groups**.

4.  In the Credential Groups list, select a credential group to associate an application credential to.

5.  On the **Application Credential** tab, select **Add**.

6.  Select one or more application credentials to associate with this credential group.

7.  Select **Add**.

8.  Select **Save**.


## Associate a bot process to a credential group

Associate one or more unattended bot processes to a credential group in RPA Hub so that the associated robot can perform automation using the credential group.

### Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Create a credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

Create a robot credential. For more information, see [Create a robot credential in RPA Hub](create-credential-set-botprocess.md).

Create an unattended bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

You can't edit the **Process Credential Mappings** record when the life-cycle stage status of the associated bot process is set to **Published**.

Only the developers who are part of the managed by group can associate the bot process to the credential group.

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

### Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Credential Groups**.

4.  In the Credential Groups list, select a credential group to create a process credential mapping for.

5.  On the **Process Credential Mappings** tab, select **Add**.

6.  Select one or more bot processes from the list to associate with this credential group.

    The list displays all the unattended bot processes that don’t have the life-cycle stage status set to **Published** or **Retired**.

    After selecting the bot processes and selecting **Add**, the process credential-mapping records for all corresponding bot processes are created.

7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.

9.  To remove a process credential mapping, select the process credential mapping, and select **Remove**.

    You can't remove process credential mappings that are associated with a published bot process.


### What to do next

For providing access to this credential group to all users in the Managed by group or to specific users, see [Provide users with access to a credential group](create-credential-group.md#).

## Provide users with access to a credential group

Provide access to either all users or specific users in the Managed by group of the associated bot processes in RPA Hub. This way, you can make sure that the correct users have access to the credentials.

### Before you begin

Familiarize yourself with the credential management concept. For more information, see [Credential Management in RPA Hub](../concept/credential-management-rpa-hub.md).

Create a credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

Add a bot process in the **Process Credential Mapping** tab of the credential group. For more information, see [Associate a bot process to a credential group](create-credential-group.md#).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

### About this task

Provide all users from the Managed by group of the associated bot process with access to a credential group by selecting the **Shared** option. Provide specific users from the Managed by group of the associated bot process with access to a credential group to by clearing the **Shared** option.

When the **Shared** option isn’t selected, the **Authorized Users** tab appears. You can add the users from the Managed by group of the associated bot process in the **Authorized Users** tab. These authorized users can create the process robot credentials in the associated bot process.

By selecting the **Shared** option, you grant access to all the users in the Managed by group. If **Shared** is selected on the Process Credential Mapping record, you can't add users in the **Authorized Users** tab.

If you remove an authorized user from the list, the Process Robot Credential record that was created by the user is deleted.

You can't edit the **Shared** option and add or remove the users in the **Authorized Users** tab when the life-cycle stage status of the associated bot process is set to **Published**.

**Important:** If you’re upgrading to Yokohama, the **Shared** option is pre-selected. When you clear the **Shared** option, the Process Robot Credential records that were created by an RPA release manager and an RPA administrator are retained. However, the Process Robot Credential records that were created by the developers from the Managed by group are deleted.

### Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Credential Groups**.

4.  In the Credential Groups list, select the credential group.

5.  On the **Process Credential Mappings** tab, select the record that you want to modify.

6.  Provide access to users.

<table id="choicetable_uvn_mw3_wbc"><thead><tr><th align="left" id="d604430e870">

Option

</th><th align="left" id="d604430e873">

Action

</th></tr></thead><tbody><tr><td id="d604430e879">

**Provide access to all users in the Managed by group**

</td><td>

Select the **Shared** option.

</td></tr><tr><td id="d604430e891">

**Provide access to the selected users in the Managed by group**

</td><td>

1.  If selected, clear the **Shared** option.

By default, this field is set to false.

**Note:** When you clear the **Shared** option, the Process Robot Credential records that were created by an RPA release manager and RPA administrator are retained. However, the Process Robot Credential records that were created by the developers from the Managed by group are deleted.

2.  Select the **Authorized Users** tab.
3.  Add the users that you want to provide access from the Managed by group of the associated bot process.


</td></tr></tbody>
</table>7.  Select **Save**.


