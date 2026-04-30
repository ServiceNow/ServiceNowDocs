---
title: Case timeline
description: The timeline provides a visual display of case activities. The timeline appears at the top of the Case form when viewed by an agent or manager in the Customer Service Management application.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Case form, Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Case timeline

The timeline provides a visual display of case activities. The timeline appears at the top of the Case form when viewed by an agent or manager in the Customer Service Management application.

The timeline uses blue circles to represent case state changes and markers to represent case activities. The information included in the timeline is also shown on the Case form in the **Activity** history.

![Case timeline displaying different case states and case activities.](../image/CustomerServiceCaseTimeline.png "Customer Service Case Timeline")

## Header

The timeline header displays the time that the case began. It also displays the time that the case was either last updated or closed.

## State changes and case activities

Each state change for a case is represented by a blue circle on the timeline. Pointing to these circles provides more information about the state change in a tooltip. For example, pointing to the first blue circle that represents the **New** state displays the name of the user who created the case and the approximate time that the case was created.

Activity lines above and below the timeline represent other case activities, including comments, information requests, close notes, email, and phone calls. Activities performed by an agent are shown above the timeline and activities performed by a customer are shown below. Pointing to these activities on the timeline displays additional information.

Overlapping states and conversations are represented by thicker borders and thicker lines. Pointing to overlapped states and conversations results in grouped tooltips.

If a case is ongoing, the end of the timeline shows the last updated activity or state change. If a case is closed, the end of the timeline shows a blue circle that represents the **Closed** state.

## Time metric

The metric to the right of the timeline tracks the amount of time that a case is open. The date and time that the case was opened is used as the start of the time calculation. When a case is ongoing, the current time is used as the end time calculation. When a case is closed, the close time is used as the end time calculation.

The metric breaks down the time by the number of minutes and hours that a case is with the agent or with the customer. A case is considered to be with the agent when it is in the **New**, **Open**, or **Closed** state.

When a case is in the **Awaiting Info** or **Resolved** state, it is considered to be with the customer.

