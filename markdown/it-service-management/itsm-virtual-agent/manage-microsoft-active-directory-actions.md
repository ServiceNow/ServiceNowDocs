---
title: Microsoft Active Directory pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage Microsoft Active Directory distribution lists using actions in conversation flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-virtual-agent/manage-microsoft-active-directory-actions.html
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Active Directory pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage Microsoft Active Directory distribution lists using actions in conversation flows.

Natural Language Understanding \(NLU\) is used to identify and trigger the Microsoft Active Directory Group action that a user wants to perform.

Requirement: [Microsoft AD spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/microsoft-ad-spoke.md) for Integration Hub \(com.sn.ad.spoke\) plugin

**Note:** If the Microsoft Active Directory topics are duplicated in a different scope than ITSM Virtual Agent conversations, script logic can be affected and cause errors.

## Add User to AD Group

Group owners can add themselves or other users to a Microsoft Active Directory Group distribution list by providing the group name and the email address or username of one or more users to add.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "AddADUser2.png"\] Alt text: Add User to AD Group topic.

## Create AD Distribution Group

Users can create a Microsoft Active Directory distribution list by providing the following information:

-   Group name
-   Group description
-   Members \(optional\)

The current user is automatically added as the group owner. Distribution lists are always public.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "CreateADGroup2.png"\] Alt text: Create AD Distribution Group topic.

## Remove User from AD Group

Users can remove themselves from a Microsoft Active Directory Group distribution list. Group owners can remove other users from a group. Provide the group name and username or email addresses to remove.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "RemoveADUser2.png"\] Alt text: Remove User from AD Group topic.

## Show My AD Group Membership

Group members can see a list of the Microsoft Active Directory distribution lists of which they are currently a member or manager.​

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "ShowADGroup2.png"\] Alt text: Show my AD Group Membership topic.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/using-itsm-va.md)

