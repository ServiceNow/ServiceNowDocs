---
title: Use Notify connector for Microsoft Teams with a major incident
description: Start a conference call from the major incident workbench by inviting users to join. The conference doesn't start until at least two participants join.Start a conference call from a major incident record and notify the participants you select.Join an ongoing major incident conference call by dialing in with the bridge number and access code or by selecting Join Call.Add participants to a conference call so they can join the discussion to resolve a major incident.Mute a participant from the conference call to avoid unnecessary background disruption.End a conference call from a major incident record. Only the host bot exits the call; other participants stay until they disconnect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/employee-experience-foundation/notify-ms-teams-major-incident.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Notify connector for Microsoft Teams, Use Microsoft Teams integration for Agent Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Employee Center \(Pro\), Employee Service Management]
---

# Use Notify connector for Microsoft Teams with a major incident

Start a conference call from the major incident workbench by inviting users to join. The conference doesn't start until at least two participants join.

Notify administrators, major incident managers, or communications managers can manage conference calls.

Conference call records are stored in the Notify Conference Calls \[notify\_conference\_call\] table. Conference call participant records are stored in the Notify Conference Call Participants \[notify\_participant\] table.

**Parent Topic:**[Use Notify connector for Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/employee-experience-foundation/c-agent-ex-use-nc.md)

## Initiate a conference call

Start a conference call from a major incident record and notify the participants you select.

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

Join an ongoing major incident conference call by dialing in with the bridge number and access code or by selecting Join Call.

### Before you begin

Role required: notify\_admin, major\_incident\_manager, or communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Do one of the following.

    -   Join via phone number: Dial in the conference bridge number along with the access code shown in the workbench from your mobile.
    -   Join Call: Click the **Join Call** to join the ongoing conference call.
    \[Omitted image "join-conf-call-2.png"\] Alt text: Join the conference call


## Add participants to a conference call

Add participants to a conference call so they can join the discussion to resolve a major incident.

### Before you begin

Role required: notify\_admin, major\_incident\_manager, or communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Click \(+\) Participants under **Active Participants**.

    \[Omitted image "add-participant.png"\] Alt text: Add a participant to a conference call.

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

End a conference call from a major incident record. Only the host bot exits the call; other participants stay until they disconnect.

### Before you begin

Role required: notify\_admin, major\_incident\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click the **Collaborate** tab.

4.  Click **End Call**.


### Result

When you end a call from ServiceNow, only the host \(bot\) exits the call. The other participants still stay in the call until they manually disconnect. The call details are no longer logged after the host \(bot\) exits the call.

