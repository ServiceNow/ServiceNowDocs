---
title: Legacy - Switch branch
description: Application developers can switch to a different repository branch to work on another version of the application.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Switch branch

Application developers can switch to a different repository branch to work on another version of the application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   GIT repository with one or more available branches.

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **Switch Branch**.

    The system displays the Switch Branch window.

2.  If there any local changes on the instance, you can save or discard them.

    |Option|Description|
    |------|-----------|
    |**Save local changes**|Saves local changes before switching to an alternate branch. You can later merge or discard the saved changes.|
    |**Discard local changes**|Permanently deletes all local changes before switching to an alternate branch.|

    **Note:** Use caution when discarding local changes. Since all application developers share repository credentials, there is no way to discard just one set of user changes. Note you cannot later restore discarded changes.

3.  Select the branch you want to switch to.

4.  Click **Switch Branch**.

    Studio updates the local application to match the branch version from repository.


**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

