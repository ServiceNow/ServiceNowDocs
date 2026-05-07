---
title: Legacy - Apply remote changes
description: Application developers can pull changes from a linked GIT repository to apply remote changes to the local instance.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Apply remote changes

Application developers can pull changes from a linked GIT repository to apply remote changes to the local instance.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md)

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **Apply Remote Changes**.

    The following operations occur:

    -   The system fetches the most recent changes from the remote repository.
    -   The system applies the remote changes to the instance.
    -   The system identifies any change conflicts requiring resolution.
    If there are conflicts, the system displays the **Resolve Conflicts** window.

    Delta loading is enabled by default in sys properties so your data isn't removed. You can disable this feature if you want data automatically deleted.

    **Note:** After a Source Control **Apply Remote Changes** or other operation, you may encounter the error message: `Skipped loading file *.xml, cannot parse the xml document, found git merge conflicts tokens`. Make sure that the files in your application do not include values that the Git repository interprets as merge conflict tokens. While these aren’t actual conflicts, you should remove them anyway. Examples of these values are:

    `>>>>>>>`

    `=======`

    `<<<<<<<`


## What to do next

Resolve any change conflicts.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

