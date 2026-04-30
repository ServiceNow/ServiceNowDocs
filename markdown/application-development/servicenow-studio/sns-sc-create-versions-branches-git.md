---
title: Create versions and branches in Git
description: App developers using ServiceNow Studio can create versions and branches in their Git repositories.Create a tag in the repository to link to a particular app version in ServiceNow Studio.Application developers can switch to a different repository branch to work on another version of the application using ServiceNow Studio.Application developers can create a branch to work on a new version of an existing app in ServiceNow Studio. Creating a branch will result in a new branch being created in the remote repository that is configured for this application. This application, including any uncommitted changes, will switch to the new branch.Set a default branch when you want to use a branch other than main for new changes or for your main ServiceNow Studio development repository.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create versions and branches in Git

App developers using ServiceNow Studio can create versions and branches in their Git repositories.

**Parent Topic:**[Source control in ServiceNow Studio](source-control-in-servicenow-studio.md)

## Create a tag to link to a particular application version

Create a tag in the repository to link to a particular app version in ServiceNow Studio.

### Before you begin

[Link an app to source control in ServiceNow Studio](../task/link-app-to-source-control.md)

Role required: admin or sn\_group\_creator.app\_creator

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Create tag**.

5.  Enter the **Tag name**.

6.  Select **Create tag**.

7.  Select **Close**.


### What to do next

Commit changes to the new branch.

## Switch repository branches

Application developers can switch to a different repository branch to work on another version of the application using ServiceNow Studio.

### Before you begin

You must have a Git repository with one or more available branches.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Switch branch**.

5.  Choose whether you want to stash or discard local changes.

<table id="choicetable_evb_nr3_t5"><thead><tr><th align="left" id="d195903e384">

Option

</th><th align="left" id="d195903e387">

Description

</th></tr></thead><tbody><tr><td id="d195903e393">

**Stash local changes**

</td><td>

Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.

</td></tr><tr><td id="d195903e402">

**Discard local changes**

</td><td>

Permanently deletes all local changes before switching to an alternate branch. If you choose to discard, you will not be able to recover those files.**Note:** Use caution when discarding local changes. Since all application developers share repository credentials, there is no way to discard just one set of user changes.

</td></tr></tbody>
</table>6.  Select the branch you want to switch to.

7.  Select **Switch Branch**.


### Result

ServiceNow Studio updates the local application to match the branch version from repository.

## Create a repository branch

Application developers can create a branch to work on a new version of an existing app in ServiceNow Studio. Creating a branch will result in a new branch being created in the remote repository that is configured for this application. This application, including any uncommitted changes, will switch to the new branch.

### Before you begin

Role required: admin or sn\_group\_creator.app\_creator

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Create branch**.

5.  Enter a **Branch name**.

6.  Create a branch from a tab by selecting the **Create from Tag** drop-down list and selecting an existing tag.

7.  Select **Create Branch**.

8.  Select **Close**.


## Set a default branch

Set a default branch when you want to use a branch other than main for new changes or for your main ServiceNow Studio development repository.

### Before you begin

[Link an app to source control in ServiceNow Studio](../task/link-app-to-source-control.md)

Role required: admin

### Procedure

1.  Follow the steps listed in [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  Add the **glide.source\_control.default\_branch\_name** property, and specify the default branch name of the Git source control repository to work from.

    For example, default branch names could include pull requests, code commits, and the like. Application developers' work is managed from and saved into the default branch if not otherwise specified. If not changed, this value defaults to sn\_instances/&lt;instance\_name&gt;.


