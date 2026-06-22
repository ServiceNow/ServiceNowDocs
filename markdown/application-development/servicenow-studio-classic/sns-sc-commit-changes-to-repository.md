---
title: Commit changes to a repository
description: Commit changes made in ServiceNow Studio to a linked Git repository by selecting individual file changes or committing all changes on the instance at once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-commit-changes-to-repository.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Commit changes to a repository

Commit changes made in ServiceNow Studio to a linked Git repository by selecting individual file changes or committing all changes on the instance at once.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Commit changes**.

    File changes from all update sets display. By default, changes from the current update set display first.

5.  Select the file changes to commit.

    \[Omitted image "sn-studio-commit-to-repo.png"\] Alt text: Select the changes you want to commit.

6.  To include untracked changes, select the **Include changes not tracked via the Customer Update \[sys\_update\_xml\] table** check box.

    -   The default for this check box is set via the **glide.sourcecontrol.default\_commit\_mode** property.
        -   The property can be set to **include\_untracked** or **exclude\_untracked**.
        -   The **include\_untracked** mode commits updates to the application that do not generate sys\_update\_xml records, as well as any user-selected updates.
        -   The **exclude\_untracked** mode commits only updates selected by the user in the **Select files to commit to source control** modal.
    -   The base system setting for the property is **exclude\_untracked**.
    -   To hide the check box and use the value of the **glide.sourcecontrol.default\_commit\_mode** property, create the **sn\_devstudio.vcs.allow\_commit\_mode\_selection** property and set it to false.
    -   Selecting this check box may incur a performance penalty.
    **Note:**

    Commits always occur in **include\_untracked** mode in the following cases:

    -   Linking to source control for the first time. For more information, see [Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md).
    -   Publishing an application linked to source control from ServiceNow Studio.
    -   Disabling selective commit mode.
7.  Select **Continue**.

8.  Enter a comment for the changes in the **Commit comment** field.

9.  Select **Commit Files**.


## Result

The following operations occur:

-   The ServiceNow AI Platform identifies all local changes.
-   The ServiceNow AI Platform commits all local changes to the remote repository.

**Note:** For list of known files that do not have customer update records and are untracked, see [Customer Updates table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/r_CustomerUpdatesTable.md).

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

