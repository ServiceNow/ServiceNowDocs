---
title: Subflows installed with On-Call Scheduling
description: Subflows are installed with On-Call Scheduling to support building on-call escalation notification configurable flows.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [On-Call Scheduling subflows, Reference for on-call scheduling, On-Call Scheduling, IT Service Management]
---

# Subflows installed with On-Call Scheduling

Subflows are installed with On-Call Scheduling to support building on-call escalation notification configurable flows.

Starting from the Zurich release, the following subflows are available instead of the workflows as the workflows are deprecated:

-   **On-Call: Assign by Acknowledgement**

    The subflow sends notifications to the members on the escalation path via channels configured in the user or shift preferences. Assignment occurs after the On-Call member acknowledges the notification.The subflow uses data from escalation settings, including overlapping shifts and custom escalation settings for shifts and rosters. Depending on the settings, the subflow moves through the escalation path and sends notifications by SMS, voice, or email that ask users to accept a task.

    On-call notifications are sent to multiple channels such as SMS or email simultaneously instead of sending it sequentially.

    The subflow respects time off as specified in rosters. Roster members with time off are not included in the escalation path and no notifications are sent to them.

    If **Force communication channel** is specified in the **Escalation settings** for rosters, the [Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_SubscriptionBasedNotifications.md) is used: SMS, email, voice, Microsoft Teams, or mobile push. If the preferred method is SMS and the on-call member does not have an SMS device defined, the user is not contacted even if the user has an email address. When forcing a communication channel on an escalation level does not succeed, no further communication attempts are made. The failed contact attempt is logged. The **Force communication channel** setting is available only if Notify is installed.

    -   Until acknowledged, sends on-call notifications to escalatees based on the escalation policy and configured contact preference.
    -   Logs escalation details for each communication.
    -   Resumes the subflow immediately after rejection.
    -   Catch-all users are treated like all other escalation users: A response is expected, and the incident might be assigned to them based on their response.
    **Note:** This subflow internally launches the On-Call: Assign by Acknowledgement per Rota subflow for each shift if multiple shifts are available at a time for a group.

-   **On-Call: Escalations by Email**

    -   Until acknowledged, sends on-call escalation notifications via email to on-call members based on the escalation policy and configured email contact preferences.
    -   Logs escalation details for each communication.
    -   Catch-all users are treated like all other escalation users: A response is expected and the incident might be assigned to them based on their response.
    **Note:** This subflow internally launches the On-Call: Escalation By Email per Rota subflow for each shift if multiple shifts are available at a time for a group.

-   **On-Call: Assign**

    Assigns the task directly to the current primary roster member. You can also enable the **Notify to assignee** check box to notify the member about the assignment. By default, the **Notify to assignee** check box is cleared for On-Call: Assign subflow.

-   **On-Call: Assign and Notify**

    Assigns the task directly to the current primary roster member and notifies the member about the assignment. If no member is available at the current time, the subflow ends. By default, the **Notify to assignee** check box is selected for On-Call: Assign and Notify subflow.

-   **On-Call: Check Assignment Response**
    -   Triggered when an inbound SMS message is received.
    -   Based on the response in the message, assigns the task to the roster member.
    -   Updates the response in the corresponding notification record.
-   **On-Call: Assign by Acknowledgement Voice**
    -   Triggered when an outbound call is made from the on-call number to any user or device.
    -   Based on the response to the voice call, assigns the task to the roster member.
    -   Updates the response in the corresponding notification record.
-   **On-Call: Time-off approval**
    -   Triggered when vacation time off \(PTO\) is requested by a user.
    -   Sends approval requests to appropriate managers.
-   **On-Call: Conference Call Escalation**
    -   Triggered when a conference call is initiated and a group is added to the call.
    -   Makes a voice call to the first group member in the escalation policy.
    -   If the member does not join the conference call, then escalates to next group member in the policy

**Note:** All the flows and channel information related to notifications channels including the primary, secondary channel, user preferences are placed inside the On-call Send Notifications subflow. This subflow is invoked to send notifications to the on-call members or user groups.

**Parent Topic:**[On-Call Scheduling subflows](on-call-scheduling-subflows-overview.md)

