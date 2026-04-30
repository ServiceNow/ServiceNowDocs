---
title: Override a skill version for a bot process in RPA Hub
description: Override a skill package version in RPA Hub to use a specific version of a skill package for a bot process. When the bot process executes, it uses the selected version instead of the version that you defined in the automation.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [Associate skill version RPA Hub, Assign skill version RPA Hub]
breadcrumb: [Adding details for your bot process in RPA Hub, Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Override a skill version for a bot process in RPA Hub

Override a skill package version in RPA Hub to use a specific version of a skill package for a bot process. When the bot process executes, it uses the selected version instead of the version that you defined in the automation.

## Before you begin

Verify that the life-cycle stage status of the bot process isn't set to **Published**. For more information, see [Life-cycle stage statuses of a bot process in RPA Hub](../reference/lifecycle-stages-botprocess.md).

You can see the skill package versions in the **Skill Overrides** tab of the bot process when the attended or unattended packages have the skill package associated with them. For more information, see [Create a package to assign to a bot process](create-package.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

You can use different versions of the skill for different bot processes based on your specific requirements.

To use the latest version of a skill package, you can override the skill package version in RPA Hub without publishing the attended or unattended package again from RPA Desktop Design Studio.

If you're upgrading to Xanadu and can't view the existing skill package versions in the **Skill Overrides** tab, then publish the attended or unattended package again and associate the package with the bot process.

In the skill package version, you can select the bot processes that you want the skill package version to override. For more information, see [Override a skill package version for multiple bot processes in RPA Hub](override-skill-version-multi-bot-process.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process that you want to override a skill package version for.

5.  On the **Skill Overrides** tab, select the skill version that you want to override.

6.  In the **Overridden version** field, select the version to override.


