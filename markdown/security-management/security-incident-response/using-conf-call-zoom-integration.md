---
title: Use the MSIM Conference Call Zoom integration
description: The following steps give you a walkthrough of how you can manage and initiate a Zoom conference call directly from a major security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate MSIM Conference Calls with Zoom, Major Security Incident Management Conference Call Integration, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the MSIM Conference Call Zoom integration

The following steps give you a walkthrough of how you can manage and initiate a Zoom conference call directly from a major security incident.

## Before you begin

Role required: sn\_msi.workspace\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management**.

2.  From the Major Security Incident list, select a major security incident.

3.  Click the **Start a conference call** action.

4.  You can also start a conference call by clicking the ![Conference call](../image/msim-conf-call-icon.png) icon on the right-context menu and selecting the + icon.

    The Start conference call pop-up appears.

5.  Choose **Zoom** as the conference bridge that you want to connect from.

6.  In the Title field, provide a title that describes the reason for the Zoom conference call.

    ![Steps to start a conference call using Zoom](../image/msim-conf-call-zoom.png "Using the Conference Call Zoom integration")

7.  In the Add participants field, select the participants for the Zoom conference call.

    You can use the search option to find and add the required participants or select the participants from the **Recommendations** list, which provides participant recommendations to add to the Zoom conference call.

    The user \(host\) who initiates the Zoom conference call is automatically added to the list of selected participants. All the users associated with the major security incident are available by default under the **Recommendations** list.

    **Note:** Make sure the participants that you select have a valid email address.

8.  After selecting the participants, provide a brief description of the reason for starting the conference call in the Description field.

    The description that you provide will be added to the conference record.

9.  After the participant list is finalized, click **Start**.

    The conference call starts in the Zoom app. All the participants are notified through two emails, one email is sent to the participants from the MSIM app and the other email is sent from the Zoom conference bridge.

10. Select the **Click here** option on top of the major security incident to join the conference call on the Zoom app.

    The participants can use the link from the MSIM email notification or the notification from the Zoom app to join the call.

    ![MSIM email notification for the Zoom conference call](../image/msim-conf-zoom-email.png "Email notification")

11. Open the associated major security incident in the MSIM workspace to view the conference call details.

    When the final participant leaves the call, the conference call ends or select **End call** in the Conference call section to end the conference call.

    If the conference call was recorded, then the recording will be available in the Conference call section of the associated major security incident after sometime.


**Parent Topic:**[Integrate MSIM Conference Calls with Zoom](../concept/integrate-msim-conf-calls-zoom.md)

