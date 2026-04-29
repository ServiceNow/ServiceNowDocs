---
title: Use MID Server guided setup
description: MID Server guided setup provides a sequence of tasks that help you install a MID Server with the proper user account and validate the MID Server. If you are setting up a MID Server for the first time, this is a good way to get one up and running in your environment quickly.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Use MID Server guided setup

MID Server guided setup provides a sequence of tasks that help you install a MID Server with the proper user account and validate the MID Server. If you are setting up a MID Server for the first time, this is a good way to get one up and running in your environment quickly.

## Before you begin

Role required: admin

<table id="table_lkq_3s4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

You are guided through a series of configuration activities that create a fully qualified MID Server. A progress indicator on each screen allows you to monitor your progress on each task.

Each configuration activity provides the following resources to help you:

-   Contextual embedded help.
-   Links to comprehensive documentation on the ServiceNow product documentation site.

**Important:** You must complete MID Server configuration before you can launch any other IT Operations Management guided setup.

## Procedure

1.  Navigate to **All** &gt; **Guided Setup** &gt; **ITOM Guided Setup**.

    The IT Operations Management Guided Setup welcome screen appears.

2.  Take one of the following actions:

    -   If none of the MID Server installation and configuration tasks are complete, click **Get Started**.
    -   If you have completed any of the MID Server installation and configuration tasks, click **Continue** to return to the task list.
    -   Select the MID Server icon in the progress bar on the left side of the category screen to display the MID Server category pane at any time.

        ![MID Server installation progress indicator](../image/SelectMIDGuidedSetup.png "Continuing MID Server guided setup from the progress bar")

3.  Click **Continue**.

    The IT Operations Management Guided Setup category screen appears. The controls for starting the MID Server tasks are at the top of the list. These task must be completed before you can set up the other applications that rely on the MID Server.

    ![MID Server Guided Setup category](../image/MIDServerGuidedSetupCategory.png)

4.  In the MID Server pane, click **Get Started**.

    The MID Server task list appears with a description of each task.

    ![MID Server Guided Setup task list](../image/MIDServerGuidedSetupList.png)

5.  Click **Configure** to create the MID Server user and follow the instructions in the help pane that appears on the right side of the screen.

    **Important:** If you configured MID Servers manually prior to starting Guided Setup, select from that information to complete each specific task.

6.  When you have provided the requested information for the MID Server user, click **Submit**, and then click **Mark as Complete** at the bottom of the help pane.

    The view returns to the task list. Notice that the circular progress indicator for the category shows 33% of the MID Server configuration complete. The progress indicator on the left side of the screen shows the completion percentage for all the IT Operations Management tasks.

    ![MID Server Guided Setup completion percentage](../image/MIDServerGuidedInProgress.png)

7.  Click **Configure** for the next task, **Download &amp; Install MID**.

    Java 21.0.7 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 21.0.7 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 17.0.10, and recommended version 21.0.7. If you are using a lower version than 17.0.10, you may see encryption related issues.

8.  Validate your new MID Server.


## What to do next

If necessary, [deploy multiple MID Servers from a single host](t_InstallMultplMIDSvrOnASingleSys.md#) in your network. Otherwise, proceed to [configure your MID Server](../concept/c_MIDServerConfiguration.md).

