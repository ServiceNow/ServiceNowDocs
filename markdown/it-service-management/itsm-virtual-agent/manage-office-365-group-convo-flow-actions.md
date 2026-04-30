---
title: Microsoft Office 365 Group pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage Microsoft Office 365 Groups using actions in conversation flows.
locale: en-US
release: xanadu
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Office 365 Group pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage Microsoft Office 365 Groups using actions in conversation flows.

Natural Language Understanding \(NLU\) is used to identify and trigger the Microsoft Office 365 Group action that a user wants to perform.

Requirement: [Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=set-up-azure&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) \(com.sn.azure\_ad.spoke\) plugin

**Note:** If the Microsoft Office 365 topics are duplicated in a different scope than ITSM VA Conversations, script logic can be affected and cause errors.

## Add Owner to Office 365 Group

Group Owners can add other users as Group Owners by providing the group name and the user email addresses to add.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Add group owner virtual agent chatbox dialog](../image/AddGroupOwner2.png)

## Add User to Office 365 Group

Group owners can add themselves or other users to a Microsoft Office 365 group by providing the group name and the email address of one or more users to add.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Add User to Office 365 Group topic.](../image/AddGroupUser2.png)

## Create Office 365 Group

Users can create a group in Microsoft Office 365 by providing the following information:

-   Group privacy
-   Group email alias
-   Outlook display name
-   Group description
-   Owners and members \(optional\)

The current user is automatically added as the Group Owner, along with any other specified users.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Create Office 365 Group topic.](../image/CreateOfficeGroup1.png)

## Get Office 365 Group Details

Group members can get group details by providing the name or email of the group.

![Get Office 365 Group Details topic.](../image/GetGroupDetails2.png)

## Remove Office 365 group Owner

Group Owners can remove themselves or other Group Owners by providing the group name and the user email addresses to remove.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Remove Office 365 group Owner topic.](../image/RemoveOwner2.png)

## Remove Office 365 group Users

Users can remove themselves from a Microsoft Azure AD group. Group owners can remove other users from a group. Provide the group name and user email addresses to remove.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Remove Office 365 group Users topic.](../image/RemoveUser2.png)

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

