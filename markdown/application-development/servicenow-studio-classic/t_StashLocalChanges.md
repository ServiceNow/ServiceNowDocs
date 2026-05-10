---
title: Legacy - Stash local changes
description: Application developers can remove and save changes locally to apply them later.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Stash local changes

Application developers can remove and save changes locally to apply them later.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   Link an application to source control
-   Change one or more application files

## About this task

Stashing changes removes them from the current application and saves them for a developer to later apply or delete.

## Procedure

1.  From Studio, navigate to **Source Control** &gt; **Stash Local Changes**.

    The system displays a list of locally changed files.

2.  Enter your description.

3.  Click **Stash Local Changes**.

    The system saves the current changes and displays a success message.

    ![Stash change dialog](../image/stash-change-description.png)

    **Note:** In the San Diego release onward, user information is preserved with each update during stashing. When the stash is applied, each update is restored in the respective user's in-progress local update set.


## What to do next

-   Close dialog
-   [Legacy - Manage stashes](t_ManageStashes.md)

To learn more see [Getting started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md)

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

