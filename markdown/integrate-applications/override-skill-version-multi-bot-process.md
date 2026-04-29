---
title: Override a skill package version for multiple bot processes in RPA Hub
description: Override a skill package version in RPA Hub for multiple bot processes that are associated with the same attended or unattended package. You can select the latest version of the skill package without publishing the attended or unattended package again from RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Package and package version, Use, RPA Hub, Workflow Data Fabric]
---

# Override a skill package version for multiple bot processes in RPA Hub

Override a skill package version in RPA Hub for multiple bot processes that are associated with the same attended or unattended package. You can select the latest version of the skill package without publishing the attended or unattended package again from RPA Desktop Design Studio.

## Before you begin

If you're upgrading to Xanadu, to view the associated bot processes in the **Bot Process** tab of the Skill Package Version form, publish the attended or unattended packages again and associate the packages to the bot processes.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

In the **Bot Process** tab of the Skill package version form, you can override a skill package version for multiple bot processes instead of overriding the version individually for each bot process.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Packages**.

4.  Select the skill package.

5.  On the **Package Versions** tab, select the version that you want to override.

6.  On the **Bot Process** tab, select **Edit**.

7.  Select the bot processes from the list that you want to override this skill version.

    The list shows the bot processes for the attended or unattended packages that are associated with the selected skill package.


**Parent Topic:**[Package and package version in RPA Hub](../concept/package-version-rpa-hub.md)

