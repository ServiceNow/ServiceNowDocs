---
title: Configure a robot credential in RPA Hub for smart card
description: Create a robot credential so that the unattended robot can log in to a Windows machine that uses smart card for login and perform the automation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Smart Card, Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# Configure a robot credential in RPA Hub for smart card

Create a robot credential so that the unattended robot can log in to a Windows machine that uses smart card for login and perform the automation.

## Before you begin

Ensure that the latest MSIs for Unattended Robot and Unattended Robot Login Agent \(version 10.1.0\) are installed.

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md), [Bot process configuration form in RPA Hub](create-botprocess-config.md#), and [Bot Process form in RPA Hub](select-botprocess.md#).

External credentials are not supported for smart cards.

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Robot Credentials**.

4.  Select **New**.

5.  Provide a unique name for the robot credential.

6.  From the **Authentication Type** field, select **Smart Card**.

7.  In the **Robot Username** field, enter the user principle name \(UPN\) to be used by the robot.

8.  In the **Robot Password** field, enter the smart card PIN to be used by the robot.

9.  Select **Save**.


