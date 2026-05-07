---
title: Start a conference call
description: Start a conference call from a task or an incident communication plan by inviting one or more users to join a call. The conference will not start until at least two participants join.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Notify for making conference calls, Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Start a conference call

Start a conference call from a task or an incident communication plan by inviting one or more users to join a call. The conference will not start until at least two participants join.

## Before you begin

Role required: notify\_view, incident\_communication\_manager

## About this task

Call participants can include:

-   Users who have been assigned specific responsibilities
-   Ad-hoc user contacts
-   Other involved parties who are not recorded as users, such as third-party contacts

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

2.  Open the relevant incident communication plan.

3.  Click the **Initiate Conference Call** related link.

4.  From the dialog box that appears, choose the **Conference Bridge** that you want to dial from.

5.  Select the participants for the conference.

    ![Initiating a conference call.](../image/StartCall.png "Initiate a conference call")

    The dialog box displays the Recommended and Selected participants for the conference. All users from the **User Contacts**list in the incident communication plan are in the Recommended section by default. The user who initiates the conference call is added to the selected list of participants.

    If a shift exists for the group contacts, the primary and secondary on-call resources are shown in the **Recommended** list.

    Calls are placed to the number in the **Mobile** phone field on the user record. If that information is blank, the user cannot be contacted through Notify. The mobile phone number has to be an E.164 compliant phone number. If the phone number is a local number, without the + prefix, the number will be retrieved based on the user's location and, if possible, converted into a valid E.164 number.

6.  To select ad-hoc participants,

<table id="choicetable_b2f_p4c_lq"><tbody><tr><td id="d164744e151">

**Click the reference lookup icon, and select the relevant user.**

</td><td>

Click **Add to selected**.

</td></tr><tr><td id="d164744e163">

**Enter the participant's phone number**

</td><td>

Click **Add to selected**.

</td></tr></tbody>
</table>7.  After the participant list is finalized, click **Start Call**.

    The conference call starts and a **Conference call initiated** message is displayed at the top of the incident communication plan form. Each user is called and can accept the call to join the conference.

8.  Click the **Conference call initiated** message to see details of that conference call.

    When the final participant leaves the conference, the conference call closes.

    **Note:** VoIP phone systems, which do not use touch tone phones, may encounter issues with recognizing key presses. To avoid problems, ensure that conference call users use touch tone phones, or configure your VoIP system settings to recognize key presses, as described in your VoIP system documentation.


**Parent Topic:**[Using Notify for making conference calls](../concept/c_NotifyConferenceCalls.md)

