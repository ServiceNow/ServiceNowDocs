---
title: On-Call Scheduling workflows
description: Workflows perform On-Call Scheduling operations.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference for on-call scheduling, On-Call Scheduling, IT Service Management]
---

# On-Call Scheduling workflows

Workflows perform On-Call Scheduling operations.

## Workflows installed with On-Call Scheduling

-   **On-Call: Assign by Acknowledgement**

    The workflow uses data from escalation settings, including overlapping shifts and custom escalation settings for shifts and rosters. Depending on the settings, the workflow moves through the escalation path and sends notifications by SMS, voice, or email that ask users to accept a task.

    To send notifications, a trigger rule is required. Trigger rules supersede some On-Call business rules in earlier releases. To define a trigger rule, you must deactivate business rules that you customized in earlier releases.

    The workflow respects time off as specified in rosters. Roster members with time off are not included in the escalation path and no notifications are sent to them.

    If **Force communication channel** is specified in the **Escalation settings** for rosters, the [Subscription-based notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_SubscriptionBasedNotifications.md) is used: SMS, email, voice, Microsoft Teams, or mobile push. If the preferred method is SMS and the on-call member does not have an SMS device defined, the user is not contacted even if the user has an email address. When forcing a communication channel on an escalation level does not succeed, no further communication attempts are made. The failed contact attempt is logged. The setting **Force communication channel** is available only if Notify is installed.

    -   Until acknowledged, sends on-call notifications to escalatees based on the escalation policy and configured contact preference.
    -   Logs escalation details for each communication.
    -   Resumes the workflow immediately after rejection.
    -   Catch-all users are treated like all other escalation users: A response is expected and the incident might be assigned to them based on their response.
    **Note:** This workflow internally launches the On-Call: Assign by Acknowledgement per Rota workflow.

-   **On-Call: Escalations by Email**
    -   Until acknowledged, sends on-call email notifications to escalatees based on the escalation policy and configured email contact preferences.
    -   Logs escalation details for each communication.
    -   Catch-all users are treated like all other escalation users: A response is expected and the incident might be assigned to them based on their response.
-   **On-Call: Assign**

    Assigns the task to the current primary roster member.

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

-   **[Workflow Activities for On-Call Scheduling](workflow-activities-oncall.md)**  
Workflow activities in On-Call Scheduling workflows.

**Parent Topic:**[Reference for on-call scheduling](../../user-administration/concept/reference-for-on-call-scheduling.md)

