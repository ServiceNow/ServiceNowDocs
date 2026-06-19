---
title: Pull changes from a repository
description: App developers using App Engine Studio \(AES\) can pull changes from a linked Git repository to apply remote changes to the local instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-studio/source-control-apply-changes.html
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Use AES with a Git source control repository, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Pull changes from a repository

App developers using App Engine Studio \(AES\) can pull changes from a linked Git repository to apply remote changes to the local instance.

## Before you begin

-   Role required: admin
-   [Link an application or application-customization to source control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/source-control-link-application.md)

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Pull from repository**.

4.  Review your uncommitted files, then select **Stash local changes** or **Discard local changes**.

    \[Omitted image "source-control-pull-repo-purple.png"\] Alt text: Pull changes from Git repository

5.  Select **Pull from repository**.

    The following operations occur:

    -   The system fetches the most recent changes from the remote repository.
    -   The system applies the remote changes to the instance.
    -   The system identifies any change conflicts requiring resolution.
    If there are conflicts, the system displays the **Resolve Conflicts** window.

    Delta loading is enabled by default in sys properties so your data isn't removed. You can disable this feature if you want data automatically deleted.


## What to do next

Resolve any change conflicts.

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/work-changes-in-git.md)

