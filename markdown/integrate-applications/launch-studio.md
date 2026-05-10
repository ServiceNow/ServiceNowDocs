---
title: Launch in Studio from RPA Hub
description: Review, edit, and debug automations by opening the associated package version of the bot process in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Monitor, RPA Hub, Workflow Data Fabric]
---

# Launch in Studio from RPA Hub

Review, edit, and debug automations by opening the associated package version of the bot process in the RPA Desktop Design Studio.

## Before you begin

Associate a package and a package version to the bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Role required: sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process.

5.  In the form header, select the down arrow in the **Start Process** button.

6.  Select **Launch In Studio**.

7.  Select one of the following options depending on whether you are on a remote or local machine.

<table id="choicetable_r3f_bsy_vqb"><thead><tr><th align="left" id="d221837e151">

Option

</th><th align="left" id="d221837e154">

Action and description

</th></tr></thead><tbody><tr><td id="d221837e160">

**Remote Machine**

</td><td>

**Note:**

Ensure to add the robot and connect to the Unattended Robot application.

 If robot pool option is enabled, select one robot from the associated robot pool and select **Launch**.

 Only robots that have mapped assigned process robot credential sets and are in the **Available** and **Busy** states are available.

 If robot pool option is not enabled, select one assigned robot and select **Launch**.

 Only robots that have an assigned credential group and are in the **Available** and **Busy** states are available.

 The associated package version opens in the selected robot machine.

</td></tr><tr><td id="d221837e210">

**Local Machine**

</td><td>

**Note:**

Ensure that the package and associated package version is available in bot process.

Select **Launch**.The associated package version opens in the Windows machine \(where your instance is rendering\), within the RPA Desktop Design Studio.

</td></tr></tbody>
</table>
**Parent Topic:**[Monitoring automations](../concept/monitoring-automations-rpa.md)

