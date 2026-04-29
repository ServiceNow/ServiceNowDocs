---
title: Start a conference call in Security Incident Response
description: Using conference call, security analysts can collaborate with other analysts and affected users in real-time. These calls facilitate the exchange of information to help resolve incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaborate using conference call or chat in Security Incident Response, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Start a conference call in Security Incident Response

Using conference call, security analysts can collaborate with other analysts and affected users in real-time. These calls facilitate the exchange of information to help resolve incidents.

## Before you begin

Make sure you’ve done the installed and activated the following apps and plugins:

-   Notify plugin \(com.snc.notify\).
-   Notify UI Components for Configurable Workspaces app.
-   Visual Task Board plugin \(com.devsnc.snb\_vtb\)

Role required: sn\_si.analyst or sn\_si.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open a security incident for which you want to initiate a conference call.

3.  Select **Collaborate**, and then select **Start a Call**, or you can select the conference call icon ![Conference call icon in SIR](../image/icon-conference-call.png) and then select the + icon.

    ![Start conference call in SIR.](../image/start-conference-call-sir.png)

    The Start conference call pop-up appears.

4.  Select a conference bridge in the **Conference bridge** field.

5.  Provide a title for the conference call in **Title**.

    **Note:** By default, the title of the incident is populated as the title of the call. You can modify the default title.

6.  Add or remove call participants in **Add participants**.

    **Note:** Based on the configuration in Conference Call settings, a pre-populated list of participants is added to **Add participants** or a **Recommendations** list of participants is available. For more information, see [Manage Conference Call users and groups](config-conference-call.md).

7.  Provide a brief description for starting the conference call.

8.  Select **Start**.

    The conference call starts in the selected conference bridge. All the participants receive notification through email and through the conference bridge. The participants can use the link or notification to join the call.

9.  Open the associated incident in Security Incident Response application to view the conference call details.

10. Select **Copy invite** to add participants in an active call.

11. Select **End call**.

    When the final participant leaves the conference call, the call ends

12. To restart a conference call, navigate to the **Completed** section and select the **Reinitiate** option of the required conference call.


**Parent Topic:**[Collaborate using conference call or chat in Security Incident Response](../concept/collab-sir-call-chat.md)

