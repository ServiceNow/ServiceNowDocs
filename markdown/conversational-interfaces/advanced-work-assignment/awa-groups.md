---
title: Create or change groups for Advanced Work Assignment queues
description: Create or manage groups that have associated Advanced Work Assignment queues.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create or change groups for Advanced Work Assignment queues

Create or manage groups that have associated Advanced Work Assignment queues.

## Before you begin

Role required: awa\_manager or admin

## About this task

Groups are sets of users who share a common purpose. By creating these groups, information that is displayed in AWA is limited to only users that are in AWA groups. The assignment group can be configured so that work items are assigned using the group queue priority. Each round of assignment can include multiple passes through the work items, each with an increasingly inclusive set of groups. This process ensures that agents in each group are offered items according to their group's queue priority order.

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home** &gt; **Management** &gt; **Groups**

2.  Choose a situation:

    -   To create a group, select **New**
    -   To change a group, select the group you want to update.
3.  On the Group screen, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the group.|
    |Manager|Group manager or lead.|
    |Group email|Group email distribution list or the email address of the point of contact, such as the group manager.|
    |Parent|Other group of which this group is a member. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group aren’t members of the parent group. For example, if an incident is assigned to the parent group and you select the Assigned to look up icon, only the members in the parent group are available. The members of the child group aren’t available.|
    |Description|Helpful information about the group.|

4.  Select **Submit**.

5.  If you want to configure the queue priority order for the group, follow these steps:

    1.  Select the group name on the list.

    2.  Select the Queues related list at the bottom of the screen.

    3.  Double-click in the order number field that you want to change.

    4.  On the pop-up Order dialog, enter the new order number.

    5.  Select the green check mark to save the change.


**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

