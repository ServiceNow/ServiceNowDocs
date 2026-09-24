---
title: Assign or close a project task in the Retail Portal
description: Comment on a project task, assign it to someone in your store, or close it when the work is done.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-spm-act-on-tasks-portal.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [close project task, assign project task, OCRR]
breadcrumb: [Project tasks in Retail, Retail]
---

# Assign or close a project task in the Retail Portal

Comment on a project task, assign it to someone in your store, or close it when the work is done.

## Before you begin

Role required: a retail contributor or fulfiller responsibility, and either sn\_bus\_loc.location\_project\_stakeholder or sn\_bus\_loc.location\_manager\_project\_stakeholder for your store

Open the project task page as described in [Find a project task in the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-view-projects-portal.md).

## About this task

**Note:** The **Actions** button appears only while the task is open and at least one action is available to you.

## Procedure

1.  To add a comment or an attachment, use the **Activity** or **Attachments** tab.

2.  To assign or close the task, select **Actions**, and then select one of the available options.

    Which options are available depends on your permissions and on the task:

    -   **__Assign task__**

        Available when you can change the assignee and the assignment group of the task. Enter an assignment group, select an assignee, and then select **Save**. A task that is already assigned to someone can still be reassigned.

    -   **__Assign to me__**

        Available on the same condition, and only when the task isn't already assigned to you.

    -   **__Close task__**

        Available when the task is assigned to you. You can close only a task that has no open child tasks. Close the child tasks first.


## Result

Your update is saved to the project task. The project manager at headquarters sees the current state of the work without asking the store for a status update.

**Note:** Each action is checked again before the update is applied. If you don't have permission, the portal reports it instead of failing silently.

**Parent Topic:**[Project tasks in Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-overview.md)

