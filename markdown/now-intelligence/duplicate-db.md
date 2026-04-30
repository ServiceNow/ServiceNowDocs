---
title: Duplicate a Platform Analytics dashboard
description: Duplicate a dashboard created in the inline editor so that you can share a modified version with different users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 1
keywords: [How to copy a dashboard, How to copy inline dashboards]
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Duplicate a Platform Analytics dashboard

Duplicate a dashboard created in the inline editor so that you can share a modified version with different users.

## Before you begin

Role required: At least one role, as well as access to the dashboard.

**Note:** This task only applies to dashboards created in the in-line editor. To work with dashboards created in UI Builder, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## About this task

When you duplicate a dashboard, you copy all settings and details of the original. Content that exists locally on the original dashboard is duplicated onto the new dashboard. If the original dashboard contains references to content in a library, such as a shared visualization, the references are duplicated. The role requirements for editing an element in a library apply to the latter.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select the **Dashboards** tab.

3.  Select the dashboard that you want to duplicate.

4.  If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    ![Application scope picker](../../par-for-workspace/image/app-scope-picker.png)

5.  Open the More actions menu \(![More actions menu icon](../../dashboards/image/icon-vert-3dot-p.png)\) and select **Duplicate**.

    ![Duplicate context action](../../par-for-workspace/image/db-duplicate.png)

6.  Give the duplicate a unique name and select **Duplicate**.


## Result

The dashboard is copied with the new name. The appearance of the dashboard is identical to the original.

**Important:** The new duplicate is automatically saved.

