---
title: Add a quick link to the Home view of CMDB Workspace
description: For an immediate access to tools or data that you need, add your own quick link to the Home view of CMDB Workspace.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Add a quick link to the Home view of CMDB Workspace

For an immediate access to tools or data that you need, add your own quick link to the Home view of CMDB Workspace.

## Before you begin

Role required: sn\_cmdb\_admin, sn\_cmdb\_editor, or sn\_cmdb\_user

## About this task

Quick links are stored in the Quick Links \[sn\_cmdb\_ws\_quick\_links\] table including those that are included in the base system. Only the user that added a quick link has access to that link, and can subsequently edit or delete that added link.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the Quick links section, click the '+' icon.

3.  Enter the **URL** and **Display text** for the link and then click **Add**.

    A valid URL must start with "http:" or "https:". To link to a tool in the instance such as the CI Class Manager, enter the full URL to the tool's landing page.

4.  Click **Done**.


## Result

The new link is available only for the user that created the link, in the Quick links section in the landing page of the CMDB Workspace.

## What to do next

Click on the Edit quick links icon to edit, delete, or reposition an added link. Then use the up and down arrows to move a link within the list, and click the Edit icon next to a link that you want to modify or delete from the list.

**Parent Topic:**[Configuring CMDB Workspace](../concept/configuring-cmdb-workspace.md)

