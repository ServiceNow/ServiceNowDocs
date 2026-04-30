---
title: Legacy - Create branch
description: Application developers can create a branch to work on a new version of an existing application.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Create branch

Application developers can create a branch to work on a new version of an existing application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin or sn\_group\_creator.app\_creator
-   [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md)

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **Create Branch**.

    Studio opens the Create Branch window.

    ![Create Branch window](../image/CreateBranch.png)

2.  Enter the **Branch Name**.

3.  To create a branch from a tag, click the **Create from Tag**drop-down list and select an existing tag.

4.  Click **Create Branch**.

    Studio creates the branch.

    ![Create Branch window showing the success message.](../image/CreateBranchSuccess.png)

5.  Click **Close**.


## What to do next

Commit changes to the new branch.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

