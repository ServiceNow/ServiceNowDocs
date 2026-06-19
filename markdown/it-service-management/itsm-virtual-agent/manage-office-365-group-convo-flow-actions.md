---
title: Microsoft Office 365 Group pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage Microsoft Office 365 Groups using actions in conversation flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-virtual-agent/manage-office-365-group-convo-flow-actions.html
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Office 365 Group pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage Microsoft Office 365 Groups using actions in conversation flows.

Natural Language Understanding \(NLU\) is used to identify and trigger the Microsoft Office 365 Group action that a user wants to perform.

Requirement: Microsoft Azure AD spoke \(com.sn.azure\_ad.spoke\) plugin

**Note:** If the Microsoft Office 365 topics are duplicated in a different scope than ITSM VA Conversations, script logic can be affected and cause errors.

## Add Owner to Office 365 Group

Group Owners can add other users as Group Owners by providing the group name and the user email addresses to add.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "AddGroupOwner2.png"\] Alt text: Add group owner virtual agent chatbox dialog

## Add User to Office 365 Group

Group owners can add themselves or other users to a Microsoft Office 365 group by providing the group name and the email address of one or more users to add.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "AddGroupUser2.png"\] Alt text: Add User to Office 365 Group topic.

## Create Office 365 Group

Users can create a group in Microsoft Office 365 by providing the following information:

-   Group privacy
-   Group email alias
-   Outlook display name
-   Group description
-   Owners and members \(optional\)

The current user is automatically added as the Group Owner, along with any other specified users.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "CreateOfficeGroup1.png"\] Alt text: Create Office 365 Group topic.

## Get Office 365 Group Details

Group members can get group details by providing the name or email of the group.

\[Omitted image "GetGroupDetails2.png"\] Alt text: Get Office 365 Group Details topic.

## Remove Office 365 group Owner

Group Owners can remove themselves or other Group Owners by providing the group name and the user email addresses to remove.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "RemoveOwner2.png"\] Alt text: Remove Office 365 group Owner topic.

## Remove Office 365 group Users

Users can remove themselves from a Microsoft Entra ID group. Group owners can remove other users from a group. Provide the group name and user email addresses to remove.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

\[Omitted image "RemoveUser2.png"\] Alt text: Remove Office 365 group Users topic.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/using-itsm-va.md)

