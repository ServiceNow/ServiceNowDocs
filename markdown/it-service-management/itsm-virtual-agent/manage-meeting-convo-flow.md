---
title: Microsoft Exchange Online meeting management pre-built topic for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO topic, you can schedule, reschedule, and cancel a meeting.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Exchange Online meeting management pre-built topic for ITSM Virtual Agent

ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO topic, you can schedule, reschedule, and cancel a meeting.

## Manage Meetings EXO v1.0

Natural Language Understanding \(NLU\) is used to identify and trigger the meeting action that a user wants to perform. Users can schedule, reschedule, or cancel a meeting.

Requirements:

-   [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) \(sn\_ex\_online\_spke\)
-   Email addresses for meeting attendees must be configured in the User \[sys\_user\] table to be added to meeting invites
-   Some actions can use the [Microsoft Teams Communication spoke](https://www.servicenow.com/docs/access?context=msteams-comm&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) \(sn\_msteams\_com\_spk\) to send meeting links to Microsoft Teams
-   Some actions can use the [Cisco Webex Teams spoke](https://www.servicenow.com/docs/access?context=cisco-teams-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) \(sn\_cisco\_teams\_spk\)
-   Some actions can use the [Zoom spoke](https://www.servicenow.com/docs/access?context=zoom-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)\(com.sn.zoom.spoke\) to add meeting links
-   This topic uses the [Employee Experience VA topic blocks](employee-experience-va-topicblocks.md)

**Note:** If this topic is duplicated in a different scope than ITSM Virtual Agent Conversations, script logic can be affected and cause errors. This topic must be duplicated in the ITSM Virtual Agent Conversations scope.

Basic flow for scheduling a meeting:

1.  User enters the email addresses for all attendees, the meeting time, and the meeting duration.
2.  Virtual Agent provides a list of available meeting times, based on the calendars of the invitees.
3.  User enters the meeting subject and description.
4.  User can choose the type of meeting: virtual/online, conference room, or hybrid.

    If the spokes are enabled on the instance, the user can add a meeting link for Microsoft Teams, Webex, or Zoom.

5.  Virtual Agent returns the meeting link \(if applicable\) and the meeting details.
6.  User confirms that Virtual Agent should schedule the meeting.
7.  Once the user confirms, Virtual Agent sends the email invitations and schedules the meeting.

**Note:** The user can also schedule a meeting through Virtual Agent using the Microsoft Teams service.

Basic flow for canceling a meeting:

1.  User enters the start and end date and time of the original meeting.
2.  Virtual Agent returns a list of potential meetings to cancel.
3.  User selects the desired meeting or can choose to cancel all meetings during the specified duration.
4.  Virtual Agent cancels all specified meetings and sends the user a confirmation email.

Basic flow for rescheduling a meeting:

1.  User enters the original meeting date.
2.  Virtual Agent returns a list of potential meetings to reschedule.
3.  User selects the desired meeting.
4.  User enters a new meeting time.
5.  Virtual Agent confirms that the meeting has been rescheduled.
6.  User can reschedule additional meetings, if desired.

## Manage Meetings EXO \(deprecated\)

This topic is deprecated. Use Manage Meetings EXO v1.0 instead.

Requirements:

-   [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   Email addresses for meeting attendees must be configured in the User \[sys\_user\] table to be added to meeting invites
-   Some actions can use the [Zoom spoke](https://www.servicenow.com/docs/access?context=zoom-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)\(com.sn.zoom.spoke\) to add meeting links
-   Some actions can use the [Microsoft Teams Communication spoke](https://www.servicenow.com/docs/access?context=msteams-comm&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) \(sn\_msteams\_com\_spk\) to send meeting links to Microsoft Teams

**Note:** If this topic is duplicated in a different scope than ITSM Virtual Agent Conversations, script logic can be affected and cause errors. This topic must be duplicated in the ITSM Virtual Agent Conversations scope.

Basic flow for scheduling a meeting:

1.  User enters the email addresses for all attendees, the meeting time, and the meeting duration.
2.  Virtual Agent provides a list of available meeting times, based on the calendars of the invitees.
3.  User enters the meeting subject and description.
4.  If the admin configured the script variable **default\_collaboration\_software** and the appropriate spoke is enabled on the instance, the user can add a Zoom link or a Microsoft Teams link.
5.  Virtual Agent returns the meeting link \(if applicable\) and the meeting details.
6.  User confirms that Virtual Agent should schedule the meeting.
7.  Once the user confirms, Virtual Agent sends the email invitations and schedules the meeting.

**Note:** The user can also schedule a meeting through Virtual Agent using the Microsoft Teams service.

Basic flow for canceling a meeting:

1.  User enters the start and end date and time of the original meeting.
2.  Virtual Agent returns a list of potential meetings to cancel.
3.  User selects the desired meeting or can choose to cancel all meetings during the specified duration.
4.  Virtual Agent cancels all specified meetings and sends the user a confirmation email.

Basic flow for rescheduling a meeting:

1.  User enters the original meeting date.
2.  Virtual Agent returns a list of potential meetings to reschedule.
3.  User selects the desired meeting.
4.  User enters a new meeting time.
5.  Virtual Agent confirms that the meeting has been rescheduled.
6.  User can reschedule additional meetings, if desired.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

