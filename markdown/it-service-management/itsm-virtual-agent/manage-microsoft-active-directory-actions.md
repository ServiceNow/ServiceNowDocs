---
title: Microsoft Active Directory pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage Microsoft Active Directory distribution lists using actions in conversation flows.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Active Directory pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage Microsoft Active Directory distribution lists using actions in conversation flows.

Natural Language Understanding \(NLU\) is used to identify and trigger the Microsoft Active Directory Group action that a user wants to perform.

Requirement: [Microsoft AD spoke](https://www.servicenow.com/docs/access?context=microsoft-ad-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for Integration Hub \(com.sn.ad.spoke\) plugin

**Note:** If the Microsoft Active Directory topics are duplicated in a different scope than ITSM Virtual Agent conversations, script logic can be affected and cause errors.

## Add User to AD Group

Group owners can add themselves or other users to a Microsoft Active Directory Group distribution list by providing the group name and the email address or username of one or more users to add.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Add User to AD Group topic.](../image/AddADUser2.png)

## Create AD Distribution Group

Users can create a Microsoft Active Directory distribution list by providing the following information:

-   Group name
-   Group description
-   Members \(optional\)

The current user is automatically added as the group owner. Distribution lists are always public.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Create AD Distribution Group topic.](../image/CreateADGroup2.png)

## Remove User from AD Group

Users can remove themselves from a Microsoft Active Directory Group distribution list. Group owners can remove other users from a group. Provide the group name and username or email addresses to remove.

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Remove User from AD Group topic.](../image/RemoveADUser2.png)

## Show My AD Group Membership

Group members can see a list of the Microsoft Active Directory distribution lists of which they are currently a member or manager.​

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Show my AD Group Membership topic.](../image/ShowADGroup2.png)

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

