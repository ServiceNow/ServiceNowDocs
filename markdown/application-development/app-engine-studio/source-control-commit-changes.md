---
title: Commit changes to a repository
description: Commit changes made in your application in App Engine Studio \(AES\) to a linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work with changes in Git, Use AES with a Git source control repository, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Commit changes to a repository

Commit changes made in your application in App Engine Studio \(AES\) to a linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.

## Before you begin

-   Role required: admin
-   [Link an application or application-customization to source control](source-control-link-application.md)

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Commit changes**.

    The system displays the **Select files to commit to source control** window. The file changes from all the updates sets display. By default, the file changes from the current update set display.

    ![Select files to commit to source control](../image/source-control-select-commit-purple.png)

4.  Select the file changes you wish to commit.

5.  To include untracked changes, select the **Include changes not tracked via the Customer Update \[sys\_update\_xml\] table** check box.

    -   The default for this check box is set via the **glide.sourcecontrol.default\_commit\_mode** property.
        -   Property can be set to **include\_untracked** or **exclude\_untracked**.
        -   The **include\_untracked** mode commits the updates to the application that do not generate sys\_update\_xml records, as well as any user-selected updates.
        -   The **exclude\_untracked** mode commits only updates selected by the user in the **Select files to commit to source control** dialog.
    -   The base system setting for the property is **exclude\_untracked**.
    -   To hide the check box and use the value of the **glide.sourcecontrol.default\_commit\_mode** property, create the **sn\_devstudio.vcs.allow\_commit\_mode\_selection** property and set it to false.
    -   Checking this check box may incur a performance penalty.
    **Note:**

    Commits always occur in **include\_untracked** mode in the following cases:

    -   Linking to source control for the first time. \(To learn more, see [Link an application or application-customization to source control](source-control-link-application.md).\)
    -   Publishing an application that's linked to source control from App Engine Studio.
    -   Selective commit mode is disabled.
6.  Select **Continue**.

7.  In **Commit comment**, enter a comment for the changes.

8.  Select **Commit Files**.

    The following operations occur:

    -   The system identifies all local changes.
    -   The system commits all local changes to the remote repository.
    **Note:** For list of known files that don’t have customer update records and are untracked, see Customer Updates table.


**Parent Topic:**[Work with changes in Git](../concept/work-changes-in-git.md)

