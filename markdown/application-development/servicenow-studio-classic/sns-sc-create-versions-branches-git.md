---
title: Create versions and branches in Git
description: Create tags and branches in a Git repository from ServiceNow Studio to version application releases and manage parallel development streams.Create a tag in the Git repository from ServiceNow Studio to mark a specific application version for future reference.Switch to a different repository branch in ServiceNow Studio to work on a separate version of the application.Create a branch in ServiceNow Studio to develop a new version of an existing app in isolation. The new branch is created in the remote repository and the application, including any uncommitted changes, switches to the new branch.Set a default branch in ServiceNow Studio to direct new changes to a branch other than main.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-create-versions-branches-git.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 3
breadcrumb: [Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create versions and branches in Git

Create tags and branches in a Git repository from ServiceNow Studio to version application releases and manage parallel development streams.

**Parent Topic:**[Source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-in-servicenow-studio.md)

## Create a tag to link to a particular application version

Create a tag in the Git repository from ServiceNow Studio to mark a specific application version for future reference.

### Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

Role required: admin or sn\_group\_creator.app\_creator

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Create tag**.

5.  Enter the **Tag name**.

6.  Select **Create tag**.

    The tag is created in the repository and linked to the current application version.

7.  Select **Close**.


### What to do next

Commit changes to the new branch.

## Switch repository branches

Switch to a different repository branch in ServiceNow Studio to work on a separate version of the application.

### Before you begin

A Git repository with one or more available branches must exist.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Switch branch**.

5.  Choose whether to stash or discard local changes before switching.

<table id="choicetable_evb_nr3_t5"><thead><tr><th align="left" id="d50915e393">

Option

</th><th align="left" id="d50915e396">

Description

</th></tr></thead><tbody><tr><td id="d50915e402">

**Stash local changes**

</td><td>

Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.

</td></tr><tr><td id="d50915e411">

**Discard local changes**

</td><td>

Permanently deletes all local changes before switching to an alternate branch. Discarded changes cannot be recovered.**Note:** Use caution when discarding local changes. Because all application developers share repository credentials, there is no way to discard only one set of user changes.

</td></tr></tbody>
</table>6.  Select the branch to switch to.

7.  Select **Switch Branch**.


### Result

ServiceNow Studio updates the local application to match the branch version from the repository.

## Create a repository branch

Create a branch in ServiceNow Studio to develop a new version of an existing app in isolation. The new branch is created in the remote repository and the application, including any uncommitted changes, switches to the new branch.

### Before you begin

Role required: admin or sn\_group\_creator.app\_creator

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Create branch**.

5.  Enter a **Branch name**.

6.  To base the branch on an existing tag, select the **Create from Tag** drop-down list and select a tag.

7.  Select **Create Branch**.

    The new branch is created in the remote repository and the application switches to the new branch.

8.  Select **Close**.


## Set a default branch

Set a default branch in ServiceNow Studio to direct new changes to a branch other than main.

### Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

Role required: admin

### Procedure

1.  Follow the steps in [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

2.  Add the **glide.source\_control.default\_branch\_name** property and specify the default branch name of the Git source control repository.

    All developer work is saved to the default branch unless a different branch is specified. If not set, the value defaults to `sn_instances/<instance_name>`.


### Result

The default branch is set. New changes in ServiceNow Studio are directed to the specified branch.

