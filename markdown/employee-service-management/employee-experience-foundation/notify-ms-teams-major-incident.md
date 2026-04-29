---
title: Use Notify connector for Microsoft Teams with a major incident
description: Initiate a conference call from the major incident workbench by inviting one or more users to join a call. The conference doesn't start until at least two participants join.As a participant in a major incident ticket, you can create a conference call from the record.After a conference call is initiated, as a logged-in user with the major incident manager role, you can join the conference call.Add a participant to a conference call to participate in the discussion to resolve the major incident.Mute a participant from the conference call to avoid unnecessary background disruption.As a host or participant with the major incident manager role, you can end the conference call.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Notify connector for Microsoft Teams, Use Microsoft Teams integration for Agent Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Use Notify connector for Microsoft Teams with a major incident

Initiate a conference call from the major incident workbench by inviting one or more users to join a call. The conference doesn't start until at least two participants join.

Notify administrators, major incident managers, or communications managers can manage conference calls.

Conference call records are stored in the Notify Conference Calls \[notify\_conference\_call\] table. Conference call participant records are stored in the Notify Conference Call Participants \[notify\_participant\] table.

**Parent Topic:**[Use Notify connector for Microsoft Teams](c-agent-ex-use-nc.md)

## Initiate a conference call

As a participant in a major incident ticket, you can create a conference call from the record.

### Before you begin

Role required: notify\_admin, major\_incident\_manager, or communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click **View Workbench**.

4.  Click the **Collaborate** tab.

5.  Select the participants for the conference.

6.  After you finalize the participant list, click **Start Call**.


### Result

A notification is sent to all the users in Microsoft Teams that a call is initiated. Each user can accept the call to join the conference call.

As the host, you can view the users who have answered the call.

## Join a conference call

After a conference call is initiated, as a logged-in user with the major incident manager role, you can join the conference call.

### Before you begin

Role required: notify\_admin, major\_incident\_manager, or communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Do one of the following.

    -   Join via phone number: Dial in the conference bridge number along with the access code shown in the workbench from your mobile.
    -   Join Call: Click the **Join Call** to join the ongoing conference call.
    ![Join the conference call](../image/join-conf-call-2.png)


## Add participants to a conference call

Add a participant to a conference call to participate in the discussion to resolve the major incident.

### Before you begin

Role required: notify\_admin, major\_incident\_manager, or communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Click \(+\) Participants under **Active Participants**.

    ![Add a participant to a conference call.](../image/add-participant.png)

5.  In the dialog box that appears, select the participants for the conference.

6.  Click **Add Participants**.


### Result

A notification is sent to all the users in Microsoft Teams that a call is initiated. Each user can accept the call to join the conference call.

As the host, you can view the users who have answered the call.

## Mute participants from a major incident conference call

Mute a participant from the conference call to avoid unnecessary background disruption.

### Before you begin

Before starting this procedure, ensure that there is an active conference call with one or more participants.

Role required: notify\_admin, major\_incident\_manager, or communications\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Click **Mute** next to the participant name you want to mute.


## End a conference call from a major incident

As a host or participant with the major incident manager role, you can end the conference call.

### Before you begin

Role required: notify\_admin, major\_incident\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Click **End Call**.


### Result

When you end a call from ServiceNow, only the host \(bot\) exits the call. The other participants still stay in the call until they manually disconnect. The call details are no longer logged after the host \(bot\) exits the call.

