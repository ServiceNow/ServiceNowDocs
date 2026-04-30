---
title: Start a conference call
description: Start a conference call from a task or a major security by inviting one or more users to join a conference call. The conference call would start only when at least two participants join.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Major Security Incident Management Conference Call Integration, Integrating Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Start a conference call

Start a conference call from a task or a major security by inviting one or more users to join a conference call. The conference call would start only when at least two participants join.

## Before you begin

Role required: sn\_msi.workspace\_manager

Make sure you’ve done the following on the ServiceNow® instance:

-   Installed and activated the Notify plugin \(com.snc.notify\).
-   Installed the Notify UI Components for Configurable Workspaces app.
-   Installed and activated the Visual Task Board plugin \(com.devsnc.snb\_vtb\).

For more information, see [Request IntegrationHub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

## About this task

The call participants can include the following:

-   Users who have been assigned specific responsibilities.
-   Ad hoc or on-demand contacts
-   Other third-party contacts

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management**.

2.  From the Major Security Incident list, select a major security incident.

3.  Select the **Start a conference call** action.

4.  You can also start a conference call by selecting the ![Conference call](../image/msim-conf-call-icon.png) icon on the right-context menu and selecting the + icon.

    The Start conference call pop-up appears.

    ![MSIM Conference call option on the major security incident](../image/msim-conf-call.png "MSIM Conference call")

5.  In the Conference bridge field, choose a **Conference bridge** that you want to connect from.

    For example, Microsoft Team, Zoom, or Cisco Webex.

6.  In the Title field, provide a title that describes the reason for the conference call.

7.  In the Add participants field, select the participants for the conference call.

    You can use the search option to find and add the required participants or select the participants from the **Recommendations** list, which provides participant recommendations to add to the conference call.

    The user \(host\) who initiates the conference call is automatically added to the list of selected participants. All the users associated with the major security incident are available by default under the **Recommendations** list.

    **Note:** Make sure the participants that you select have a valid email address.

    ![Steps to start a conference call for the major security incident](../image/msim-start-conf-call.png "Start a conference call")

8.  After selecting the participants, provide a brief description of the reason for starting the conference call in the Description field.

    The description that you provide will be added to the conference record.

9.  After the participant list is finalized, select **Start**.

    The conference call starts in the selected conference bridge. All the participants are notified through email, and they're also notified through the respective conference bridge that was selected.

10. Select the **Click here** option on top of the major security incident to join the conference call.

    The participants can use the link from the email notification or the notification from the selected conference bridge to join the call.

11. Open the associated major security incident to view the conference call details.

    When the final participant leaves the conference, the conference call ends or select **End call** to end the conference call.


**Parent Topic:**[Major Security Incident Management Conference Call Integration](../concept/integrate-msim-conference-calls.md)

**Related topics**  


[Add participants to a conference call](add-participants-conference-call.md)

[Mute participants in a conference call](mute-unmute-participants.md)

[View conference call details](view-conference-call-details.md)

[Integrate MSIM Conference Calls with Microsoft Teams](../concept/integrate-msim-conf-call-ms-teams.md)

[Integrate MSIM Conference Calls with Zoom](../concept/integrate-msim-conf-calls-zoom.md)

[Integrate MSIM Conference Calls with Cisco Webex](../concept/integrate-msim-conf-calls-webex.md)

