---
title: Manage stashed changes
description: Apply or delete stashed changes in ServiceNow Studio to restore saved work or remove stashes that are no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-manage-stashed-changes.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Manage stashed changes

Apply or delete stashed changes in ServiceNow Studio to restore saved work or remove stashes that are no longer needed.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

At least one stashed change must exist.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Manage stashes**.

5.  Select the action next to the stash to manage.

    |Option|Description|
    |------|-----------|
    |**Apply**|Commits the stashed changes to the application and checks for conflicts.|
    |**Delete**|Permanently removes the stashed changes.|

6.  After applying stashed changes, continue normal pull and push operations to add the changes to the Git repository.

    For more information, see [Pull changes from a repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-pull-changes-from-repository.md).


## Result

The selected action is applied to the stash. If changes were applied, continue with pull and push operations to update the Git repository.

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

