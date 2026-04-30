---
title: Initiate a Zoom or Microsoft Teams meeting from the Now Agent mobile application
description: Initiate a Zoom or Microsoft Teams meeting from the Now Agent mobile application to resolve customer issues by assisting them virtually while out of the office or away from your desktop computer.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Virtual Conferencing on Mobile Agent, Complete work orders on Mobile Agent, Using Field Service Management, Field Service Management]
---

# Initiate a Zoom or Microsoft Teams meeting from the Now Agent mobile application

Initiate a Zoom or Microsoft Teams meeting from the Now Agent mobile application to resolve customer issues by assisting them virtually while out of the office or away from your desktop computer.

## Before you begin

Role required: wm\_agent

## About this task

You can host a Zoom or Microsoft Teams meeting to do video conferencing and screen sharing with your customers from the Now Agent mobile application. You can invite multiple participants to the meeting when initiating a conference call or add a new participant after the call is initiated.

On initiating the meeting, participants receive an email and SMS notification that includes work order task number, a short description of the issue, and the meeting link.

**Note:** The conference call details of a Zoom or Microsoft Teams meeting are stored in the Notify Conference Calls \[notify\_conference\_call\] table.

## Procedure

1.  Navigate to the Field Service mobile application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Select and open the work order task.

5.  Initiate the meeting.

    1.  Tap the More actions \(![More actions icon](../image/OverflowIcon.png)\) icon and then select the call platform.

        -   For a Zoom call, select **Make a Zoom Call**.
        -   For a Microsoft Teams meeting, select **Make a MS Teams Call**.
    2.  Select required participants for the conference call.

<table id="table_hnh_m15_v4b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My Group Agents

</td><td>

Agents from the assignment group mentioned in the work order task.

</td></tr><tr><td>

Users

</td><td>

Specific users such as a manager, dispatcher, and so on.

</td></tr><tr><td>

Groups

</td><td>

Any groups in your instance.

</td></tr><tr><td>

Customer

</td><td>

For Zoom calls, you can add a customer mentioned in the work order task.You must install the Customer Service with Field Service Management plugin to see the customer name on work order tasks. For more information, see [Integration with Customer Service Management](../concept/customer-service-integration.md).

</td></tr></tbody>
</table>    3.  After the participants list is finalized, tap **Submit** to initiate the conference call.

    4.  Tap the conference call ID to enter into the active conference call, for example, CC000XXXX.

6.  Join the meeting by tapping **Join** from the Home screen.

7.  Invite more participants to an active call by tapping **Add Participants**.

    As a host of the meeting, you can admit participants by sharing the meeting URL with them. The number of participants you can admit depends on your Zoom or Microsoft Teams account settings.

    If SMS configuration is enabled, the customer receives an SMS with the link to join the conference call. Otherwise, the customer receives an email with the meeting link.

8.  Record the meeting.

    For more information, see the [Zoom Help Center](https://support.zoom.us/hc/en-us) for Zoom calls or [Record a meeting in Teams](https://support.microsoft.com/en-us/office/record-a-meeting-in-teams-34dfbe7f-b07d-4a27-b4c6-de62f1348c24) for Microsoft Teams calls.

    The recording of the meeting is added to the Conference form page in the Now Agent mobile application.


**Parent Topic:**[Virtual Conferencing on Mobile Agent](../concept/using-vci-fsm.md)

