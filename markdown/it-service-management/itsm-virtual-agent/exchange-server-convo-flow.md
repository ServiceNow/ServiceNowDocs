---
title: Microsoft Exchange Server meeting management pre-built topics for ITSM Virtual Agent
description: ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Server. Using the Manage Meetings EXS topic, you can schedule, reschedule, and cancel a meeting.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Microsoft Exchange Server meeting management pre-built topics for ITSM Virtual Agent

ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Server. Using the Manage Meetings EXS topic, you can schedule, reschedule, and cancel a meeting.

## Manage Meetings EXS

Natural Language Understanding \(NLU\) is used to identify and trigger the meeting action that a user wants to perform. Users can schedule, reschedule, or cancel a meeting.

Requirements:

-   Microsoft Exchange Server spoke \(sn\_exchange\_spoke\)
-   Email addresses for meeting attendees must be configured in the User \[sys\_user\] table to be added to meeting invites
-   Some topics can use the Zoom spoke to add meeting links

**Note:** If these topics are duplicated in a different scope than ITSM Virtual Agent Conversations, script logic can be affected and cause errors. This topic must be duplicated in the ITSM Virtual Agent Conversations scope.

## Manage Meetings EXS: Cancel a meeting

Users can send a message to Virtual Agent requesting to cancel a meeting, or users can select the desired template and select **Cancel Meeting**.

Basic flow:

1.  User enters the start and end date and time of the original meeting.
2.  Virtual Agent returns a list of potential meetings to cancel.
3.  User selects the desired meeting or can choose to cancel all meetings during the specified duration.
4.  Virtual Agent cancels the meetings, sends an email to all attendees, and updates the calendar.

![Manage Meetings EXS topic - Canceling a meeting.](../image/CancelEXS2.png)

## Manage Meetings EXS: Reschedule a meeting

Users can send a message to Virtual Agent requesting to reschedule a meeting, or the user can select the desired template and select **Reschedule Meeting**.

Basic flow:

1.  User enters the original meeting date.
2.  Virtual Agent returns a list of potential meetings to reschedule.
3.  User selects the desired meeting.
4.  User enters a new meeting time.
5.  Virtual Agent reschedules the meeting, emails the attendees, and updates the calendar.

Virtual Agent reschedules the meeting, emails the attendees, and updates the calendar.

![Manage Meetings EXS topic - Rescheduling a meeting.](../image/RescheduleEXS2.png)

## Manage Meetings EXS: Schedule a meeting

Users can send a message to Virtual Agent requesting to schedule a meeting, or the user can select the desired template and select **Set up Meeting**.

Basic flow:

1.  User enters the email addresses for all attendees, the meeting time, and the meeting duration.
2.  Virtual Agent provides a list of available meeting times, based on the calendars of the invitees.
3.  User enters the meeting subject and description.
4.  Virtual Agent returns the meeting details.
5.  User confirms that Virtual Agent should schedule the meeting.
6.  Once the user confirms, Virtual Agent sends the email invitations and schedules the meeting.

![Manage Meetings EXS topic - Scheduling a meeting.](../image/scheduleEXS3.png)

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

