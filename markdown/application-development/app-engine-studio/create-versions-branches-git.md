---
title: Create versions and branches in Git
description: App developers using App Engine Studio \(AES\) can create versions and branches in their Git repositories.Create a tag in the repository to link to a particular app version in App Engine Studio \(AES\).Application developers can switch to a different repository branch to work on another version of the application using App Engine Studio \(AES\).Application developers can create a branch to work on a new version of an existing app in App Engine Studio \(AES\).Set a default branch when you want to use a branch other than main for new changes or for your main App Engine Studio \(AES\) development repository.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use AES with a Git source control repository, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create versions and branches in Git

App developers using App Engine Studio \(AES\) can create versions and branches in their Git repositories.

**Parent Topic:**[Use AES with a Git source control repository](aes-source-control-use.md)

## Create a tag to link to a particular application version

Create a tag in the repository to link to a particular app version in App Engine Studio \(AES\).

### Before you begin

-   Role required: admin or sn\_group\_creator.app\_creator
-   [Link an application or application-customization to source control](../task/source-control-link-application.md)

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Create tag**.

    App Engine Studio opens the Create Branch window.![Create tag window](../image/source-control-create-tag-purple.png)

4.  Enter the **Tag Name**.

5.  Select **Create Tag**.

    App Engine Studio creates the tag.

6.  Select **Close**.


### What to do next

Commit changes to the new branch.

## Switch branches

Application developers can switch to a different repository branch to work on another version of the application using App Engine Studio \(AES\).

### Before you begin

-   Role required: admin
-   Git repository with one or more available branches.

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Switch branch**.

    ![Switch branch menu item](../image/source-control-switch-branch-purple.png)

    The system displays the Switch Branch window.

4.  If there any local changes on the instance, you can save or discard them.

    |Option|Description|
    |------|-----------|
    |**Save local changes**|Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.|
    |**Discard local changes**|Permanently deletes all local changes before switching to an alternate branch.|

    **Note:** Use caution when discarding local changes. Since all application developers share repository credentials, there is no way to discard just one set of user changes. Note you cannot later restore discarded changes.

5.  Select the branch you want to switch to.

6.  Select **Switch Branch**.

    App Engine Studio updates the local application to match the branch version from repository.


## Create a branch

Application developers can create a branch to work on a new version of an existing app in App Engine Studio \(AES\).

### Before you begin

-   Role required: admin or sn\_group\_creator.app\_creator
-   [Link an application or application-customization to source control](../task/source-control-link-application.md)

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Create branch**.

    App Engine Studio opens the Create Branch window.

    ![Create Branch window](../image/source-control-create-branch-name-purple.png)

4.  Enter the **Branch Name**.

5.  To create a branch from a tag, select the **Create from Tag** drop-down list and select an existing tag.

6.  Select **Create Branch**.

    App Engine Studio creates the branch.

    ![Create Branch window showing the success message.](../image/source-control-create-branch-done-purple.png)

7.  Select **Close**.


### What to do next

Commit changes to the new branch.

## Set the default branch

Set a default branch when you want to use a branch other than main for new changes or for your main App Engine Studio \(AES\) development repository.

### Before you begin

-   Role required: admin
-   [Link an application or application-customization to source control](../task/source-control-link-application.md)

### Procedure

1.  Follow the steps to [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  Add the **glide.source\_control.default\_branch\_name** property, and specify the default branch name of the Git source control repository to work from \(pull requests, code commits, etc.\).

    Application developers' work is managed from and saved into the default branch if not otherwise specified. If not changed, this value defaults to sn\_instances/&lt;instance\_name&gt;.


