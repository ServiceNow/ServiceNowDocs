---
title: Configure email notifications in Unified Security Exposure Management
description: Set up email notifications to share useful information about important updates and activities such as approval and rejection of false-positive requests. Creating an email notification involves specifying when to send it, who receives it, and what it contains.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure email notifications in Unified Security Exposure Management

Set up email notifications to share useful information about important updates and activities such as approval and rejection of false-positive requests. Creating an email notification involves specifying when to send it, who receives it, and what it contains.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../concept/sem-acls-for-admin-rules.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Under **Others**, select **Review** on the **Notifications** tile.

4.  Select **New**.

    For detailed instructions on creating email notifications, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


## Result

When a recipient clicks the links in an email notification, the links open in the Security Exposure Management Workspace or IT Remediation Workspace based on their role.

-   Links open in the Security Exposure Management Workspace for the users with the roles, sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin.
-   Links open in the IT Remediation Workspace for the users with the role, sn\_vul.remediation\_owner.

If the recipient doesn’t have any of the preceding roles, the links in an email notification open in the classic UI.

