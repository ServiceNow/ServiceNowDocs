---
title: Using Notify for making conference calls
description: Notify administrators, major incident managers, or communications managers can manage conference calls.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Notify for making conference calls

Notify administrators, major incident managers, or communications managers can manage conference calls.

Conference call records are stored on the Notify Conference Calls \[notify\_conference\_call\] table. Conference call participant records are stored on the Notify Conference Call Participants \[notify\_participant\] table.

Conference call and participant records are created automatically when starting and connecting to a conference call. Most fields, such as the **Duration** of a call, are set automatically using business rules.

**Note:** If a participant attempts to join a conference call using an invalid phone number, the caller is added to the participant list and the phone number is marked with a status of **Invalid**.

Notify administrators, major incident managers, or communications managers can manage conference call participants.

Several conference call workflows are available by default. These workflows can be used for incoming and outgoing calls and incoming SMS messages. Conference call workflows are:

-   Notify: \(Re\)join Conference Call
-   Notify: Join Conference Call Via SMS
-   Notify: \(Re\)join Conference Call with muting

    **Note:** Notify: \(Re\)join Conference Call with muting is available only with demo data.


The number groups Conference Call Group and Notify On Task Group use these conference call workflows by default.

-   **[Start a conference call](../task/start-a-conference-call.md)**  
Start a conference call from a task or an incident communication plan by inviting one or more users to join a call. The conference will not start until at least two participants join.
-   **[Add participants to a conference call](../task/t_AddParticipantToConferenceCall.md)**  
Add a participant to a conference call using Notify.
-   **[Mute or unmute all participants](../task/t_MuteOrUnmuteAll.md)**  
As a communications manager or a conference call host, mute/unmute all the conference participants from the workbench.
-   **[Mute or remove a conference call participant](../task/t_MuteOrKickAConfCallParty.md)**  
As a communications manager, you can mute or kick conference call participants.
-   **[Send a message to conference call participants](../task/send-sms-confcall-participants.md)**  
Send a brief message as a text or voice message to the participants of a conference call to set a context to the call.
-   **[Viewing conference call information](../reference/r_IAViewConferenceCallInformation.md)**  
Conference calls are listed as system activities in the **Activity** section of the Incident Communication Plan form and also are listed in the **Conference Calls** related list.
-   **[List of Notify calls](../reference/view-list-of-notify-calls.md)**  
If you are a Notify administrator, you can view a list of calls and the status of a call made to or from Notify. The call records help in reporting and analytics.

**Parent Topic:**[Using Notify](using-notify.md)

