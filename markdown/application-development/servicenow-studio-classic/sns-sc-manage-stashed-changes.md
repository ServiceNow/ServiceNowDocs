---
title: Manage stashed changes
description: App developers can apply or delete stashed changes from ServiceNow Studio.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Manage stashed changes

App developers can apply or delete stashed changes from ServiceNow Studio.

## Before you begin

[Link an app to source control in ServiceNow Studio](link-app-to-source-control.md)

You must have one or more stashed changes.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Manage stashes**.

5.  Select the action next to the stash you want to manage.

    |Option|Description|
    |------|-----------|
    |**Apply**|Commits the stashed changes to the application and checks for conflicts.|
    |**Delete**|Removes the stashed changes.|

6.  If you apply the stashed changes to your application, continue normal pull/push operations to add your changes to the Git repository.

    For more information, see [Pull changes from a repository](sns-sc-pull-changes-from-repository.md).


**Parent Topic:**[Work with changes in Git](../concept/sns-sc-work-with-changes-in-git.md)

