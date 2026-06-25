---
title: Manage task plan template access from the workspace
description: Remove access entries for a task plan template to control who can view or use it in the Task Plan Templates workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/manage-access-to-a-task-plan-template-from-the-workspace.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Sharing task plan templates, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Manage task plan template access from the workspace

Remove access entries for a task plan template to control who can view or use it in the Task Plan Templates workspace.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator

## About this task

The Manage access view displays all existing access entries for a template. Access entries are sorted by type in the following order: users, groups, business organizations, business organization criteria, and member type.

**Note:** The **Manage access** button appears in the share plan modal only after access has been granted to at least one entity other than the owner.

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **All Task Plan Templates**.

2.  Open a task plan template that has been shared with one or more entities.

3.  Select **Share**.

    The share plan modal opens on the Share plan view.

4.  Select **Manage access**.

    The manage access view opens and displays all current access entries.

5.  Select the check box next to one or more entries, then select **Remove access**.

    -   If you remove access for all entries, the modal returns to the share plan view automatically.
    -   If you remove access for a subset of entries, the list refreshes to show the remaining entries.
6.  Select **Back** to return to the share plan view without making changes.


**Related topics**  


[Share a task plan template with other users or groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/share-task-plan-template-with-user-groups-serviceorg.md)

[Notify users when a task plan template is shared](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/notify-users-when-taskplan-template-is-shared.md)

