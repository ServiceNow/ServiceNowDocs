---
title: Pull changes from a repository
description: App developers using ServiceNow Studio can pull changes from a linked Git repository to apply remote changes to the local instance.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Pull changes from a repository

App developers using ServiceNow Studio can pull changes from a linked Git repository to apply remote changes to the local instance.

## Before you begin

[Link an app to source control in ServiceNow Studio](link-app-to-source-control.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Pull from repository**.

5.  Choose whether you want to stash or discard local changes.

<table id="choicetable_evb_nr3_t5"><thead><tr><th align="left" id="d173681e150">

Option

</th><th align="left" id="d173681e153">

Description

</th></tr></thead><tbody><tr><td id="d173681e159">

**Stash local changes**

</td><td>

Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.

</td></tr><tr><td id="d173681e168">

**Discard local changes**

</td><td>

Permanently deletes all local changes before switching to an alternate branch. If you choose to discard, you will not be able to recover those files.**Note:** Use caution when discarding local changes. Since all application developers share repository credentials, there is no way to discard just one set of user changes.

</td></tr></tbody>
</table>    ![Before you pull from the repository, select whether you want to stash or discard local changes.](../image/sn-studio-pull-from-repo.png)

6.  Select **Pull from repository**.


## Result

The following operations occur:

-   The ServiceNow AI Platform fetches the most recent changes from the remote repository.
-   The ServiceNow AI Platform applies the remote changes to the instance.
-   The ServiceNow AI Platform identifies any change conflicts requiring resolution.

If there are conflicts, the system displays the **Resolve Conflicts** window.

Delta loading is enabled by default in sys\_properties so your data isn't removed. You can disable this feature if you want data automatically deleted.

**Parent Topic:**[Work with changes in Git](../concept/sns-sc-work-with-changes-in-git.md)

