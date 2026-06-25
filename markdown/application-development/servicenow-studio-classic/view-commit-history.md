---
title: Legacy - View commit history
description: Application developers can view the commit history of applications linked to a source control repository.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/servicenow-studio-classic/view-commit-history.html
release: xanadu
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - View commit history

Application developers can view the commit history of applications linked to a source control repository.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/servicenow-studio-landing.md).

-   Role required: admin
-   An existing link to a GIT repository

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **View History**.

    The system displays the History window.

    \[Omitted image "source-control-view-history.png"\] Alt text: History window displaying two commit changes: one from the user david.loo and one from the user admin.

2.  Select the commit sort order type.

<table id="choicetable_hz1_hmh_jx"><tbody><tr><td id="d199098e136">

**Date**

</td><td>

Sort by commit date.

</td></tr><tr><td id="d199098e145">

**Committer**

</td><td>

Sort by user name.

</td></tr></tbody>
</table>3.  Select the sort order direction.

<table id="choicetable_xvp_4mh_jx"><tbody><tr><td id="d199098e163">

**Descending**

</td><td>

Sort dates from the most recent to oldest date. Sort user names reverse-alphabetically from Z to A.

</td></tr><tr><td id="d199098e172">

**Ascending**

</td><td>

Sort dates from the oldest to most recent date. Sort user names alphabetically from A to Z.

</td></tr></tbody>
</table>    The system sorts commits by the selected sort order.

4.  Select a commit.

    The system displays the commit details for the selected commit.

5.  Review the commit details.

    |Field|Description|
    |-----|-----------|
    |Committer|The user who committed the change.|
    |Date|The date-time stamp of the commit.|
    |SHA-1|The secure hash value identifying this commit in the repository.|
    |Message|The commit message associated with this commit.|
    |Files|The list of application files changed in this commit.|

6.  Close the History window.


**Parent Topic:**[Legacy - Source Control integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/c_SourceControlIntegration.md)

