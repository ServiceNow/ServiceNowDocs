---
title: Create an external credential vault record in RPA Hub
description: Create an external credential vault record in RPA Hub to register your external credential vault for further usage by the robot.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring credentials, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create an external credential vault record in RPA Hub

Create an external credential vault record in RPA Hub to register your external credential vault for further usage by the robot.

## Before you begin

Familiarize yourself with the external credentials concepts. For more information, see [External credential vault in RPA Hub](../concept/external-credentials-rpa.md).

Verify that you’ve completed the tasks that are related to configuring the external credentials in RPA Hub. For more information, see [Steps to configure an external credential vault in RPA Hub](../reference/config-ext-cred-rpa.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

An external credential vault is a secure storage system often used to store and manage sensitive information. For example, user names, passwords, and other access credentials for various applications, services, or systems.

To edit an existing external credential vault record, clear the **Active** check box.

You can’t deactivate an external credential vault record, if it’s associated with a published bot process.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **External Credential Vaults**.

4.  Select **New**.

5.  On the External Credential Vault form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the external credential vault.For example, Demo CyberArk.

</td></tr><tr><td>

Subflow

</td><td>

Associated subflow that fetches the credentials from the external credential vault.Only published and active subflows are listed here, that aren't associated with any existing External Credential Vault record.

Subflow and External Credential Vault names have a one-on-one mapping.

</td></tr><tr><td>

Active

</td><td>

Option to activate the external credential vault.Clear the **Active** check box to edit an existing external credential vault record.

</td></tr><tr><td>

Description

</td><td>

Brief description of the external credential vault.

</td></tr></tbody>
</table>6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


