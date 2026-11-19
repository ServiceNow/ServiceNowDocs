---
title: Manage stashed changes
description: App developers can apply or delete stashed changes from ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-sc-manage-stashed-changes.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Manage stashed changes

App developers can apply or delete stashed changes from ServiceNow Studio.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/link-app-to-source-control.md)

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

    For more information, see [Pull changes from a repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-sc-pull-changes-from-repository.md).


**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

