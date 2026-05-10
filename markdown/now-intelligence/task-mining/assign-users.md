---
title: Assign roles for Task Mining users
description: Assign roles to control access to features, capabilities, and data in the Task Mining application.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Assign roles for Task Mining users

Assign roles to control access to features, capabilities, and data in the Task Mining application.

## Before you begin

Set the application scope to Task Mining core using the application picker.

Role required: sn\_tm\_core.admin or admin

## About this task

For detailed information about roles that are installed with Task Mining, see [Components installed with Task Mining](../reference/installed-with-task-mining.md).

## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).
    -   [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

## What to do next

Users responsible for installing Task Mining agents must be a part of the Task Mining Agent Install group with roles itil, sn\_tm\_core.service\_user, and agent\_client\_collector\_admin to install the Task Mining agent. For more information, see [Install the Task Mining agent](../concept/install-agent.md).

