---
title: Legacy - Create branch
description: Application developers can create a branch to work on a new version of an existing application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/servicenow-studio-classic/t\_CreateBranch.html
release: xanadu
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Create branch

Application developers can create a branch to work on a new version of an existing application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/servicenow-studio-landing.md).

-   Role required: admin or sn\_group\_creator.app\_creator
-   [Legacy - Link an application or application-customization to source control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/t_LinkAnApplicationToSourceControl.md)

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **Create Branch**.

    Studio opens the Create Branch window.

    \[Omitted image "CreateBranch.png"\] Alt text: Create Branch window

2.  Enter the **Branch Name**.

3.  To create a branch from a tag, click the **Create from Tag**drop-down list and select an existing tag.

4.  Click **Create Branch**.

    Studio creates the branch.

    \[Omitted image "CreateBranchSuccess.png"\] Alt text: Create Branch window showing the success message.

5.  Click **Close**.


## What to do next

Commit changes to the new branch.

**Parent Topic:**[Legacy - Source Control integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/c_SourceControlIntegration.md)

