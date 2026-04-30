---
title: Actionable notifications for incidents in ITSM Virtual Agent
description: Notify employees of pending tasks and incident alerts with notifications from ITSM Virtual Agent.
locale: en-US
release: yokohama
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ITSM Virtual Agent pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Actionable notifications for incidents in ITSM Virtual Agent

Notify employees of pending tasks and incident alerts with notifications from ITSM Virtual Agent.

You must activate notifications in Workflow Studio in order to use them. For details, see [Set up actionable notifications for ITSM Virtual Agent](../task/setup-actionable-notifications.md).

## Incident commented

End users are notified whenever someone adds a comment to their incident. The end user can choose to view comments, resolve the incident, or skip the notification.

If the end user selects **View Comments**, Virtual Agent displays the three most recent comments on the incident.

After viewing the most recent comments, the end user can choose to add their own comments and images.

![Actionable notification for Incident commented.](../image/NewComment2.png)

## Incident on behalf of caller

End users receive this notification whenever someone opens an incident on their behalf. The end user can choose to add a comment to the incident, resolve the incident, or skip the notification.

If the end user selects **Add Comment**, Virtual Agent provides a URL to the incident and the end user can enter comments directly into the chat.

If the end user selects **Resolve Incident**, Virtual Agent resolves the incident and provides the incident URL.

![Incident on behalf of caller actionable notification.](../image/IncidentOpen1.png)

## Incident resolved

End users receive this notification whenever someone other than the end user resolves one of their incidents. The end user can choose to close the incident, mark the incident unresolved, or skip the notification.

If the end user chooses to mark the incident unresolved, Virtual Agent offers to add comments from the end user directly through the chat and reopens the incident.

If the end user chooses to close the incident, Virtual Agent closes the incident and provides the incident URL.

![Actionable notification for incident resolved.](../image/ResolveIncident1.png)

## Incident Update

End users receive this notification whenever someone updates their incident. The end user can choose to add a comment to the incident, resolve the incident, or skip the notification.

## KB attached to incident \(deprecated\)

End users receive this notification from Virtual Agent when a Knowledge Base article is attached to their incident. The end user can choose to view the article, resolve the incident, or skip the notification.

If the end user chooses to view the article, Virtual Agent displays a snippet and a link to the complete article.

The end user can also give feedback and add comments to the incident​.

![Knowledge Base article attached to incident notification.](../image/KB3.png)

**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](../concept/itsm-actionable-notifications.md)

