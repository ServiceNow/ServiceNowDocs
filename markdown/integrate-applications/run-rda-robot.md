---
title: Run an automation using Attended Robot
description: Run an attended robot to execute the attended bot process \(attended automations\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Attended Robot, Workflow Data Fabric]
---

# Run an automation using Attended Robot

Run an attended robot to execute the attended bot process \(attended automations\).

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](../../rpa-hub/task/create-package.md#).

Ensure that the licenses are available. For more information, see [Robot license distribution in RPA Hub](../../rpa-hub/concept/license-rpa-hub.md).

If the auto assignment system property **sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment** is false, the attended robot record must be available for the assigned RPA Assisted User. If the auto assignment system property is true, attended robots license must be available to auto create attended robot record at the time of automation execution. For more information about this system property, see [Configure RPA Hub properties](../../rpa-hub/reference/rpahub-sys-properties.md).

Create a bot process. Select the **Process Type** field as **Attended** on the Bot process form, while you are creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../../rpa-hub/concept/create-botprocess.md) and [Bot Process form in RPA Hub](../../rpa-hub/task/select-botprocess.md#).

Ensure that the following conditions are met to execute a robot:

-   The life cycle stage status of the associated bot process must be **Published**.
-   The life cycle stage status of the executing robot must be **In-Use**.

Assign an attended user or a group to an attended bot process. For more information, see [Assign an attended user or group to an attended bot process](../../rpa-hub/task/assign-rda-users-botprocess.md).

Establish a connection between the Attended Robot and ServiceNow RPA Hub instance. For more information, see [Set up Attended Robot](set-up-rda-runtime.md).

Ensure that you meet the infrastructure requirements for running the Desktop In Desktop:

The minimum requirements are as follows:

-   Intel Processor \(1vCPU\)
-   8-GB RAM
-   Minimum 20-GB free disk space \(after installing OS, patches, and base software\).
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019
-   .NET Framework 4.7.1 or higher
-   DPI scaling setting must be deactivated.

The recommended requirements are as follows:

-   Intel Processor \(4vCPU\)
-   16-GB RAM
-   Minimum 50-GB free disk space \(after installing OS, patches, and base software\).
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019
-   .NET Framework 4.7.1 or higher
-   DPI scaling setting must be deactivated.

Role required: sn\_rpa\_fdn.rpa\_assisted\_user and snc\_internal

**Note:** If the Attended Robot tries to connect to an Federal Information Processing Standards \(FIPS\)-enabled instance, the robot user must have the `snc_internal` role.

## About this task

You can run an automation using an attended robot in two ways. Do these tasks after you establish a connection between the Attended Robot and ServiceNow RPA Hub instance. For more information, see [Set up Attended Robot](set-up-rda-runtime.md).

## Procedure

1.  In the Attended Robot dialog box, select the attended bot process that you want to run.

    Bot processes with Embedded Task Automation enabled are not displayed in this list. For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

2.  To run an attended robot, do any one of the following actions.

<table id="choicetable_ag1_lyx_jrb"><thead><tr><th align="left" id="d125196e320">

Option

</th><th align="left" id="d125196e323">

Action

</th></tr></thead><tbody><tr><td id="d125196e329">

**From the Run option**

</td><td>

Select the Run icon \(![Run icon.](../image/rda-runtime-icon-run.png)\).The Attended Robot runs the automation.

</td></tr><tr><td id="d125196e350">

**From the Desktop In Desktop option**

</td><td>

Select the Desktop In Desktop icon \(![Desktop In Desktop icon.](../image/rda-runtime-icon-run-desktop.png)\).The Attended Robot runs the automation in a desktop session.

 This option is useful when you want to work simultaneously while running an automation.

This option appears only when you select the **Enable Desktop In Desktop** check box on the Bot process form, while you are creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../../rpa-hub/concept/create-botprocess.md) and [Bot Process form in RPA Hub](../../rpa-hub/task/select-botprocess.md#).

**Important:** If an automation is executed in Desktop In Desktop, the Zscaler connection is lost in the main session and the connection is established in a bot session. This can lead to unresponsive state of the robot. For more information about the Zscaler limitation, see [https://help.zscaler.com/zpa/understanding-client-connector-support-multiple-tenants](https://help.zscaler.com/zpa/understanding-client-connector-support-multiple-tenants).

If the Desktop In Desktop feature prompts you to enter credentials unexpectedly on Windows 10 or Windows 11, it may be due to the system's security mechanisms such as Credential Guard. For more information on how to suppress the native credential prompt, see [KB2030392](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2030392).

**Tip:** If your computer uses the Windows 11 operating system, you might need to enter the login credentials because the Credential Guard is enabled in Windows 11 by default. To avoid entering login credentials every time, you can disable the Credential Guard. To learn the steps to disable, see the Disable Credential Guard section in [https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/configure?tabs=reg](https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/configure?tabs=reg).

</td></tr></tbody>
</table>3.  To stop an attended robot, do the following actions:

    1.  Select the stop icon \(![Stop attended robot icon.](../image/rda-runtime-icon-stop-robot.png)\).

    2.  In the Confirmation dialog box, select **Yes**.


**Parent Topic:**[Using Attended Robot](../concept/using-rda-runtime.md)

