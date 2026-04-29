---
title: Installing Task Mining agent
description: The Task Mining agent is a service installed on workstations that logs certain events from desktop applications.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Task Mining, Platform Analytics]
---

# Installing Task Mining agent

The Task Mining agent is a service installed on workstations that logs certain events from desktop applications.

Role required: Task Mining Agent Install

**Note:** You must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. If the group doesn't exist, create a group with that name and those roles manually. For more information, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

The process to install a Task Mining agent is as follows:

1.  Data log request is submitted by a Task Mining analyst or power user.
2.  The manager approves the request.
3.  Installation is performed by an IT or security user who is a part of the Task Mining Agent Install group with admin rights on the target workstation.

    For more information, see the article in the Now Support Knowledge Base for your operating system:

    -   macOS - [Task Mining agent installation guide for MacOS \[KB2225974\]](https://support.servicenow.com/kb?sys_kb_id=eb4c97f747caea54c4e1a325126d436a&id=kb_article_view)
    -   Windows - [Task Mining agent installation guide for Windows \[KB2225869\]](https://support.servicenow.com/kb?sys_kb_id=e783177f4742e654c4e1a325126d432e&id=kb_article_view)
    **Note:** Use the standard Windows Agent unless instructed otherwise. The Windows Portable agent is only designed for users in a proof of concept state and shouldn’t be used in production.

4.  Workstation users are notified about workstation monitoring.

For more information about the data collected, see [Data collected by Task Mining](../reference/data-management.md).

