---
title: Install the Task Mining Portable Windows agent
description: Run the Task Mining agent from a portable archive without installing it on the system. The portable agent does not modify the Windows registry or write files outside its extracted folder.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
breadcrumb: [Install the Task Mining agent, Configure, Task Mining, Platform Analytics]
---

# Install the Task Mining Portable Windows agent

Run the Task Mining agent from a portable archive without installing it on the system. The portable agent does not modify the Windows registry or write files outside its extracted folder.

## Before you begin

Role required: Task Mining Agent Install

**Note:** You must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. If the group doesn't exist, create a group with that name and those roles manually. For more information, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

## Procedure

1.  Extract the `ZIP` and copy the **Instance URL** and **Registration key**.

    1.  Navigate to **All** &gt; **Task Mining** &gt; **Agent Installation**.

    2.  Select an existing key or create one.

        ![Screenshot of registration key selection.](../image/tm-agent-3.png)

    3.  Select the Portable Windows agent tab.

    4.  Extract the `ZIP` archive to any folder, for example `C:\Tools\TM-Agent-Portable`.

    5.  Copy the **Instance URL** and **Registration key** on the Agent Installation page.

    ![Screenshot of portable windows agent download screen.](../image/tm-agent-5.png)

2.  Run `PortableLauncher.exe` from the extracted folder.

    `PortableLauncher.exe` starts the agent executable \(`tm-agent-winui.exe`\) from the `Bin` directory. If `tm-agent-winui.exe` exits unexpectedly or restarts itself, the launcher restarts automatically.

    On the first run, a registration dialog appears.

3.  Register the agent with your ServiceNow instance.

    1.  Enter the ServiceNow instance URL \(copied from the Agent Installation page\).

    2.  Enter the registration key \(copied from the Agent Installation page\).

    3.  Select **Register**.

    After successful registration, the agent starts normally. This can take up to 30 seconds. Once running, the agent icon appears in the Windows system tray \(notification area\).


## What to do next

If you encounter issues, check the logs in the `Bin\log` directory within the extracted folder.

