---
title: Install the Task Mining agent
description: The Task Mining agent is a service installed on workstations that logs certain events from desktop applications.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Install the Task Mining agent

The Task Mining agent is a service installed on workstations that logs certain events from desktop applications.

Role required: Task Mining Agent Install

**Note:** You must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. If the group doesn't exist, create a group with that name and those roles manually. For more information, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

The process to install a Task Mining agent is as follows:

1.  A data request is submitted by a Task Mining analyst or power user.

    When a Task Mining adds a workstation user to a Task Mining project, a data request is sent to all managers of every workstation user. For more information, see [Add workstation users to a Task Mining project](../task/add-users-to-task-mining-project.md).

2.  The manager approves the request.

    When the manager approves the data log request, the Task Mining agent can be installed. For more information, see [Approve workspace user data collection](../task/approve-workspace-user-log-requests.md).

3.  Installation is performed by an IT or security user who is a part of the Task Mining Agent Install group with admin rights on the target workstation.

    For more information, see the article in the Now Support Knowledge Base for your operating system:

    -   [Install the Task Mining agent for macOS](../task/install-the-task-mining-agent-for-macos.md)
    -   [Install the Task Mining agent for Windows](../task/install-the-task-mining-agent-for-windows.md)
    -   [Install the Task Mining Portable Windows agent](../task/install-task-mining-portable-agent.md)
    **Note:** Use the standard Windows Agent unless instructed otherwise. The Portable Windows agent is only designed for users in a proof of concept state and shouldn’t be used in production.

4.  Workstation users are notified about workstation monitoring.

For more information about the data collected, see [Data collected by Task Mining](../reference/data-management.md).

