---
title: Actionable notifications for Service Catalog requests in ITSM Virtual Agent
description: Notify employees of Service Catalog tasks and alerts with notifications from ITSM Virtual Agent.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITSM Virtual Agent pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Actionable notifications for Service Catalog requests in ITSM Virtual Agent

Notify employees of Service Catalog tasks and alerts with notifications from ITSM Virtual Agent.

You must activate these notifications in Workflow Studio. For details, see [Set up actionable notifications for ITSM Virtual Agent](../task/setup-actionable-notifications.md).

## Citrix provision notification

End users are notified whenever a change occurs to a Citrix session or application. For information about pre-built topics for Citrix, see [Citrix session pre-built topics for ITSM Virtual Agent](manage-citrix-convo-flow.md).

## Request approved or rejected

Virtual Agent sends a notification to the requester of a generic Service Catalog request. The requester can choose to view the details or skip the notification.

## Requested Item approval reminder

Virtual Agent sends a notification to the approver of a Service Catalog request. The approver can choose to view the request details or skip the notification.

Approvers can approve or reject the request directly in the chat. Approvers can also add comments to rejected requests directly in the chat.

![Requested item approval reminder.](../image/RITMapprover1.png)

## Requested item commented

Virtual Agent sends a notification to employees who have requested Service Catalog items when a new comment is added to the request. Requesters can choose to view the comment or skip the notification.

If the requester selects **View Comment**, Virtual Agent displays the three most recent comments and the requester can choose to add their own comment.

![Notification for Requested item commented.](../image/RITMcomment2.png)

The requester enters a comment and Virtual Agent adds the new comment directly from the chat.

## Requested item on behalf of requester

Virtual Agent sends a notification to an end user when a Service Catalog request is opened on the end user's behalf. The requester can choose to view request details, add comments directly in the chat, or skip the notification.

![Requested item on behalf of requester notification.](../image/RITMbehalf1.png)

## Requested Item Update

Virtual Agent sends a notification to the requester of a Service Catalog request any time the state changes. The requester can choose to view the details or skip the notification.

## Software Installation

End users \(requesters\) can submit a request for software from the Software Catalog by selecting the link displayed under **Use the link below to submit your request**.

![Submitting a software request.](../image/software_request1.png)

When the submitted request is approved, Virtual Agent sends an actionable notification to the end user letting them know that the software has been assigned and will be available soon.

**Note:** End users must be using [Client Software Distribution](https://www.servicenow.com/docs/access?context=c_ClientSoftwareDistribution&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

![Software assigned.](../image/software_request2.png)

The requester can do the following:

-   See details about the software request by selecting **Take me to the software center**.
-   See a list of relevant Knowledge Base \(KB\) articles, if any, by selecting **OK, I'm done**.

    By default, Virtual Agent displays the articles included in the sc\_2\_kb table. An admin can define which table is used by changing the value of the **sn\_itsm\_va.cat\_item\_related\_kb** system property.


**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](../concept/itsm-actionable-notifications.md)

