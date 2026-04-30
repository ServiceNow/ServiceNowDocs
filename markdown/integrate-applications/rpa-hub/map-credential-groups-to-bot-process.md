---
title: Associate a credential group to a bot process
description: Enable a robot to perform an automation in RPA Hub by mapping a credential group to an unattended bot process.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Associate a credential group to a bot process

Enable a robot to perform an automation in RPA Hub by mapping a credential group to an unattended bot process.

## Before you begin

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md), and [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Create a credential group. For more information, see [Create a credential group in RPA Hub](create-credential-group.md#).

You can associate the credential group to an unattended bot process that doesn’t have the life-cycle stage status set to **Retired** or **Published**. For more information, see [Life-cycle stage statuses of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

You can't edit the **Process Credential Mappings** record when the life-cycle stage status of the associated bot process is set to **Published**.

Only the RPA developers who have created the credential groups can associate credential groups to a bot process.

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A credential group includes application credentials and a robot credential.

**Note:** If you're upgrading to Xanadu and have customized the bot process related-list tabs, the **Process Credential Mappings** tab might not appear to you. However, you can add this tab in the bot process record by navigating to **Additional actions** &gt; **Configure** &gt; **Related Lists** in the classic environment.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Select the bot process that you want to map a credential group to.

5.  On the **Process Credential Mappings** tab, select **Add**.

6.  Select the required credential groups.

7.  Select **Add**.

8.  Provide access to authorized users.

    For more information, see [Provide users with access to a credential group](create-credential-group.md#).

9.  Select **Save**.


