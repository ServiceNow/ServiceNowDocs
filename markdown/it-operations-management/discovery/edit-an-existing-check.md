---
title: Edit an existing check
description: Edit a Tuning check definition to change its description or script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/edit-an-existing-check.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-11-10"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Edit an existing check

Edit a Tuning check definition to change its description or script.

## Before you begin

Role required: admin

## About this task

Active checks run automatically when their suite runs:

-   Discovery suite runs once a week on Sunday at 8 AM.
-   MID suite runs once a week on Sunday at 10 AM.
-   Self monitoring suite runs every 15 mins.

You can also deactivate a check. An inactive check doesn't run when its suite runs, and it isn't counted in the Tuning health score.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Tuning**.

2.  Select the check name.

3.  Select the **Check definition page** link.

4.  To edit the check, select **Switch scope**.

5.  Update the required details.

    To stop the check from running, clear the **Active** check box.

6.  Select **Save**.


