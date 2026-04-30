---
title: View commit history
description: App developers can view the commit history of apps linked to a source control repository in App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use AES with a Git source control repository, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# View commit history

App developers can view the commit history of apps linked to a source control repository in App Engine Studio \(AES\).

## Before you begin

-   Role required: admin
-   An existing link to a Git repository

## Procedure

1.  Navigate to **All** &gt; **Source Control** &gt; **View History** .

    The system displays the History window.

2.  Select the commit sort order type.

<table id="choicetable_hz1_hmh_jx"><tbody><tr><td id="d219395e92">

**Date**

</td><td>

Sort by commit date.

</td></tr><tr><td id="d219395e101">

**Committer**

</td><td>

Sort by user name.

</td></tr></tbody>
</table>3.  Select the sort order direction.

<table id="choicetable_xvp_4mh_jx"><tbody><tr><td id="d219395e119">

**Descending**

</td><td>

Sort dates from the most recent to oldest date. Sort user names reverse-alphabetically from Z to A.

</td></tr><tr><td id="d219395e128">

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


**Parent Topic:**[Use AES with a Git source control repository](../concept/aes-source-control-use.md)

