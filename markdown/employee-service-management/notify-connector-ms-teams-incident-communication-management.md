---
title: Use Notify connector for Microsoft Teams with Incident Communication Management
description: Use Notify with an incident communication plan to start conference calls.Initiate a conference call in Microsoft Teams from an incident communication plan so you can discuss the resolution of an incident.Add a participant to a conference call on a task record from the incident communication plan.Mute a participant in a conference call to avoid unnecessary background disruption.As a host or a user with the incident communication manager role, you can end the conference call.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use Notify connector for Microsoft Teams, Use Microsoft Teams integration for Agent Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Use Notify connector for Microsoft Teams with Incident Communication Management

Use Notify with an incident communication plan to start conference calls.

The property **com.snc.iam.enable\_notify** must be enabled in Notify Properties to make calls from major incident record.

1.  Navigate to **Notify** &gt; **Administration** &gt; **Notify Properties**.
2.  Check the option **Enable Notify integration for Incident Communications Management. Entering phone number in 'com.snc.iam.notify\_number' property is equivalent to setting this to true** \(com.snc.iam.enable\_notify\).

    Right-click on the "Enable Notify integration for Incident Communications Management. Entering phone number in 'com.snc.iam.notify\_number' property is equivalent to setting this to true" text and click **Edit Property** to view the property details.

    ![Notify properties.](../image/notify-properties.png)

3.  Click **Save**.

**Parent Topic:**[Use Notify connector for Microsoft Teams](c-agent-ex-use-nc.md)

## Start a conference call from an incident communication plan

Initiate a conference call in Microsoft Teams from an incident communication plan so you can discuss the resolution of an incident.

### Before you begin

Role required: incident\_communication\_manager

### Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

2.  Open the relevant incident communication plan.

3.  Click the **Initiate Conference Call** related link.

4.  In the dialog box, select the participants for the conference.

5.  After you finalize the participant list, click **Start Call**.


### Result

A notification is sent to all the selected users in Microsoft Teams that a call is initiated. Each user can accept the call to join the conference call.

As the host, you can view the users who have answered the call.

## Add participants to a conference call from the incident communication plan

Add a participant to a conference call on a task record from the incident communication plan.

### Before you begin

Role required: ia\_admin, or admin

### Procedure

1.  Navigate to **Incident Communications Management** &gt; **All**.

2.  Open the relevant incident communication plan.

3.  Click the **Conference** tab.

4.  Click \(+\) Participants under **Active Participants**.

5.  In the dialog box, select the participants you want to add to the conference call.

6.  Click **Add Participants**.


### Result

A notification is sent to all the selected users in Microsoft Teams that a call is initiated. Each user can accept the call to join the conference call.

As the host, you can view the users who have answered the call.

## Mute a participant in a conference call

Mute a participant in a conference call to avoid unnecessary background disruption.

### Before you begin

This procedure assumes that there is an active conference call with one or more participants.

Role required: ia\_admin, or admin

### Procedure

1.  Navigate to **Incident Communications Management** &gt; **All**.

2.  Open the relevant incident communication plan.

3.  Click the **Conference** tab.

4.  Click **Mute** next to the participant name you want to mute.


## End a conference call made through an incident record

As a host or a user with the incident communication manager role, you can end the conference call.

### Before you begin

Role required: ia\_admin or admin

### Procedure

1.  Navigate to **Incident Communications Management** &gt; **All**.

2.  Open the relevant incident communication plan.

3.  Click the **Conference** tab.

4.  Click **End Conference Call**.


### Result

When you end a call, only the host \(bot\) exits the call. The other participants still stay in the call until they manually disconnect. After the host \(bot\) exits the call, call details are no longer logged.

