---
title: Assign an attended user or group to an attended bot process
description: Assign an attended user or group to an attended bot process in RPA Hub, so that your user or group can access and execute this automation on Windows machines.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Assign an attended user or group to an attended bot process

Assign an attended user or group to an attended bot process in RPA Hub, so that your user or group can access and execute this automation on Windows machines.

## Before you begin

Do this task only when you select the **Process Type** field as **Attended** on the Bot process configuration form, while creating a bot process. You can't perform this task unless you select that field. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](../reference/bot-process-config-form.md), and [Bot Process form in RPA Hub](../reference/bot-process-form.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

Assign users or groups to an attended bot process. You must assign only those users who have the RPA assisted user role \(sn\_rpa\_fdn.rpa\_assisted\_user\).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to assign an attended user or a group to.

5.  On the **Attended Users/Groups** tab, select **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Process|Name of the associated bot process.|
    |Assigned User|Assigned user for the attended bot process.|
    |Assigned Group|Assigned group for the selected assigned user.|

7.  Select **Save**.


**Related topics**  


[RPA Hub actions and subflow](../reference/rpa-hub-actions.md)

