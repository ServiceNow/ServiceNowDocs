---
title: Pull changes from a repository
description: Pull changes from a linked Git repository in ServiceNow Studio to apply remote updates to the local instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-pull-changes-from-repository.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Pull changes from a repository

Pull changes from a linked Git repository in ServiceNow Studio to apply remote updates to the local instance.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Pull from repository**.

5.  Choose whether to stash or discard local changes before pulling.

<table id="choicetable_evb_nr3_t5"><thead><tr><th align="left" id="d50873e152">

Option

</th><th align="left" id="d50873e155">

Description

</th></tr></thead><tbody><tr><td id="d50873e161">

**Stash local changes**

</td><td>

Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.

</td></tr><tr><td id="d50873e170">

**Discard local changes**

</td><td>

Permanently deletes all local changes before switching to an alternate branch. Discarded changes cannot be recovered.**Note:** Use caution when discarding local changes. Because all application developers share repository credentials, there is no way to discard only one set of user changes.

</td></tr></tbody>
</table>    \[Omitted image "sn-studio-pull-from-repo.png"\] Alt text: Before you pull from the repository, select whether you want to stash or discard local changes.

6.  Select **Pull from repository**.


## Result

The following operations occur:

-   The ServiceNow AI Platform fetches the most recent changes from the remote repository.
-   The ServiceNow AI Platform applies the remote changes to the instance.
-   The ServiceNow AI Platform identifies any change conflicts requiring resolution.

If there are conflicts, the system displays the **Resolve Conflicts** window.

Delta loading is enabled by default in sys\_properties so your data is not removed. Disable this feature if you want data automatically deleted.

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

