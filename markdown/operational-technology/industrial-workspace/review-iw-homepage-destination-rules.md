---
title: Review the homepage destination rules for the Industrial Workspace
description: Review the homepage destination rules for the Industrial Workspace.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Industrial Workspace, Operational Technology]
---

# Review the homepage destination rules for the Industrial Workspace

Review the homepage destination rules for the Industrial Workspace.

## Before you begin

Role required: admin

## About this task

The homepage destination rules redirect users to different pages in the Industrial Workspace based on user criteria. For more information about the homepage destination rules, see [Industrial Workspace homepage destination rules](../concept/industrial-workspace-homepage-destination-rules.md).

## Procedure

1.  Navigate to **All**.

2.  In the **Filter** field, add `sys_homepage_destination_rule.list`.

3.  Press the Enter key.

4.  Select one of the following Industrial Workspace homepage destination rules whose user criteria you want to edit:

    -   OT Progress Scorecard Page
    -   Industrial Workspace Home Page
    -   OT Dashboard Library Page

        **Note:** The OT Dashboard Library Page rule only displays if Operational Technology Manager is installed.

    -   ISA Equipment Model Page

        **Note:** The ISA Equipment Model Page rule only displays if Industrial Process Manager is installed.

    -   Industrial Workspace List Page
5.  In the **User Criteria** field, copy the user criteria.

6.  To apply the user criteria that redirects users to the page in the Industrial Workspace that you select, complete the following steps.

    1.  Navigate to **All** &gt; **User Criteria**.
    2.  In the list view's search bar, search the homepage destination rule's user criteria you copied in step 5.
    3.  Modify the User Criteria record so that the required users that you want redirected match the user criteria.
    4.  Select **Update**.

## Result

The users, groups, and roles defined in the user criteria record are now automatically redirected to the selected page in the Industrial Workspace.

**Parent Topic:**[Configuring the Industrial Workspace](../concept/configuring-industrial-workspace.md)

