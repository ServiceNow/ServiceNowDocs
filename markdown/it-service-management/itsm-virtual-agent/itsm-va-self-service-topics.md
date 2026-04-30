---
title: Self-Service pre-built topics for ITSM Virtual Agent
description: Self-Service topic conversations are designed to give users to access IT-related information, such as open or check IT ticket status, verify assigned equipment, and Knowledge Base search.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Use pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Self-Service pre-built topics for ITSM Virtual Agent

Self-Service topic conversations are designed to give users to access IT-related information, such as open or check IT ticket status, verify assigned equipment, and Knowledge Base search.

## Book Conference Room EXO

Users can book a conference room in Microsoft Exchange Online using Virtual Agent.

Requirement: [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(sn\_ex\_online\_spke\)

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

Basic flow:

1.  User selects a city for the meeting.

    The city must be configured as a room resource.

2.  User selects number of attendees and start date and time.
3.  User selects meeting duration.

    By default, the minimum duration is 30 minutes.

4.  Virtual Agent provides a list of available rooms.

    Room availability lookup is done in batches of 10 rooms. Five rooms are displayed at a time, with pagination through the lookup results.

5.  User provides a meeting subject and can send the invitation to attendees if the user provides email addresses.
6.  User confirms meeting details, and the request is submitted.

![Book Conference Room Exchange Online topic.](../image/BookingEO4.png)

## Book Conference Room OnPrem

Users can book a conference room in on-premises Microsoft Exchange Server using Virtual Agent.

Requirement: [Microsoft Exchange Server spoke](https://www.servicenow.com/docs/access?context=msexchangeserver-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(sn\_exchange\_spoke\)

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

Basic flow:

1.  User selects a city for the meeting.

    The city must be configured as a room resource.

2.  User selects number of attendees and start date and time.
3.  User selects meeting duration.

    By default, the minimum duration is 30 minutes.

4.  Virtual Agent provides a list of available rooms.

    Room availability lookup is done in batches of 50 rooms. Five rooms are displayed at a time, with pagination through the lookup results.

5.  User provides a meeting subject and can send the invitation to attendees if the user provides email addresses.
6.  User confirms meeting details, and the request is submitted.

![Book Conference Room OnPrem topic confirmation.](../image/BookingOnPrem7.png)

## Check IT Ticket Status

Users can check the status of active IT tickets \(incidents or requests\). When a user asks about a ticket status, Virtual Agent responds with a list of all active tickets for that user. Each ticket includes a link to the incident or request, the item, the status \(**Stage**\), and when it was updated.

Users can add comments and also ask to chat with a live agent.

![Check IT Ticket status topic.](../image/CheckITTicketStatus.png)

## Check Ticket and Support Status

Users can search for an incident, a customer case, or an HR ticket by the ticket number, short description, or description. A search using the short description or description shows the ticket updated within the past month.

## Escalate IT Ticket

Users can raise the urgency of an IT ticket for a faster resolution. Escalating a ticket priority requires choosing the incident and verifying the escalation. Users must provide a justification to escalate the incident. Virtual Agent escalates the incident to the next urgency level, for example, from low to medium, or from medium to high. If an incident is already at high-level urgency, Virtual Agent alerts the user to this and asks if the user would like to add a comment to help expedite resolution.

![Escalate IT Ticket topic.](../image/EscalateITTicket.png)

## Get Password Reset Link \(deprecated\)

This topic is deprecated. Use [Reset Password](../concept/itsm-password-management.md#itsm-va-reset-password-topic) instead.

Users can access a password reset link when system lockout occurs or when passwords are forgotten. When a user enters keywords related to password reset, Virtual Agent provides a link to the password reset process. If a user is not authenticated in the system, Virtual Agent requests the user's email address. If a user is not enrolled in Password Reset, Virtual Agent provides a link to **Password Enrollment**.

**Note:** An admin must properly configure the password reset process with a valid verification type for this topic to work as described. For details, see [Configure your Password Reset process](https://www.servicenow.com/docs/access?context=t_CreateAPasswordResetProcess&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

## Get Zoom Meeting Recording

Users can get a recording of a Zoom meeting that they hosted in Microsoft Exchange Online.

Requirements:

-   [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(com.sn.msexchange.spoke\)
-   [Zoom spoke](https://www.servicenow.com/docs/access?context=zoom-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(com.sn.zoom.spoke\)
-   User email address must be configured in the User \[sys\_user\] table
-   User email address must match the address in Microsoft Exchange Online and Zoom

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

Basic flow:

1.  User enters when the meeting took place.
2.  Virtual Agent returns a list of possible meetings.
3.  User selects the desired meeting.
4.  Virtual Agent sends a link to the recording.

    If the recording has a passcode enabled, the email includes the passcode.

    The user can also share the recording with the meeting invitees or to a list of emails. If the host shares the meeting link, recipients receive an email notification.


![Get Zoom Meeting Recording topic.](../image/ZoomRecording4.png)

## My Assigned Equipment

Users can view a list of all assigned equipment, such as laptops, mobile phones, and monitors. Clicking an item link provides additional details about the asset. Users can also create an asset-related incident directly within the conversation. Opening an incident from this conversation initiates the Open IT Ticket conversation topic by using the Create Incident topic block.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

![My Assigned Equipment topic.](../image/MyAssignedAssets.png)

## Open IT Ticket \(deprecated\)

This topic is deprecated. Use Open IT Ticket 2.0 instead.

**Note:** This conversation topic is refactored to use the Create Incident topic block.

Users can open an incident or access relevant knowledge base articles to resolve an issue. After typing keywords, such as `open ticket` or `incident`, Virtual Agent prompts the user to enter a short description of the issue. Virtual Agent returns links to relevant knowledge base articles and asks if an article resolved the issue. If it did not, Virtual Agent asks for the urgency of the issue and creates an incident, providing a link to the actual incident.

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Contextual Search
-   Create Incident

When creating an incident, if you also want to create an associated Universal Request and display the Universal Request card in Virtual Agent instead of the incident, the [Universal Request plugin](https://www.servicenow.com/docs/access?context=setup-configure-ur&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) \(com.snc.universal\_request\) must be active, and the **Create Universal Request with incident** system property \(**com.snc.create\_universal\_request\_with\_incident**\) must be set to **Yes** \(the default is Yes\).

**Note:** Locate the property within the **Incident Properties** module, in the **Incident VA Conversation** category. Users with the itil\_admin role have read and write permissions.

## Open IT Ticket 2.0

This topic is recommended to create an IT incident. Users can leverage machine-learning algorithms with application logic for predicting similar open tickets. Prevent users from opening duplicate incidents by finding similar incidents and asking if the user wants to add comments to the similar incident.

Requirement: [Predictive Intelligence for Incident plugin](../../incident-management/task/request-predictive-intelligence-for-im.md) \(com.snc.incident.ml\)

This topic uses the following [topic blocks](itsm-va-topic-blocks.md):

-   Add Comments-Similar Incident
-   Contextual Search
-   Create Incident

This topic was formerly called Intelligent Open IT Ticket. Both the Open IT Ticket and Report IT issue topics have been deprecated and replaced with this topic. If you have been using any of these three topics directly prior to the ITSM Virtual Agent Conversations version 5.6 release, the deprecated topic name will display in the portal and must be updated. To update to the new template, navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**. Duplicate the Open IT Ticket 2.0 topic, save it, and then select **Publish**.

## Process Approval

Users with the approver\_user role can access active approval requests. Virtual Agent returns all active approvals as a list. Users click an approval to access the actual approval record to approve or reject.

## Service Disruptions

Users can access all known outage information. When a user asks if a particular system is down, Virtual Agent returns a list of links displaying planned or unplanned outages and any system degradations. Users can click the links for more detailed information about a specific outage or degradation, as well as click **Show more** when additional outages are known.

![Service Disruptions topic.](../image/ServiceDisruptions.png)

## Set OOO reply Exchange Server

Users can set an automatic out-of-office reply for Microsoft Exchange Server using Virtual Agent. The user selects the start and end time using their current local time zone. This topic recognizes date-range entities and intents. The message is hard-coded and is the same for internal and external recipients.

Requirement: [Microsoft Exchange Server spoke](https://www.servicenow.com/docs/access?context=msexchangeserver-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(sn\_exchange\_spoke\)

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Set OOO reply Exchange Server topic.](../image/SetOOOExchangeServer3.png)

## Submit a request \(deprecated\)

**Note:** While you can use the Submit a request topic to search for and request catalog items, the recommended method is to use the [Fallback setup topic](https://www.servicenow.com/docs/access?context=working-setup-topics&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

Users can submit a request by choosing from all available options. For example, when a user is requesting an item, the Virtual Agent prompts the user to enter a search keyword. After the user enters the keyword, Virtual Agent responds with available choices in a carousel view.

This topic uses the following [Service Catalog topic blocks](https://www.servicenow.com/docs/access?context=request-topic-blocks-va&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US):

-   Request Catalog Item
-   Search Catalog Item

When the user selects the required item, the following scenarios are possible:

-   A user can submit a request in the conversation mode \(by answering the questions in line\). After the request submission, a requested item card is displayed with the request number as a link to the request page.![Requested completed card in Virtual Agent](../../service-catalog-management/image/va-request-complete.png)

    **Note:** In Now® Mobile, the URL opens the native screen.

-   A user can submit a request in a popup or a window.

    -   In case of a popup, Virtual Agent provides a link for the user to submit the request in a popup without navigating to a new tab. A non-conversational catalog item can be rendered as a popup only if it does not have any Custom, Custom with label, or UI Page variables. For more information, see [Service Catalog topic blocks in Virtual Agent](https://www.servicenow.com/docs/access?context=request-topic-blocks-va&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   In case of a window, Virtual Agent provides a link for the user to submit the request in the Service Portal defined in the **sn\_itsm\_va.com.snc.itsm.virtualagent.portal\_url** property. A non-conversational item will be rendered as a window it has a Custom, Custom with label, or UI Page variable. For more information, see [Service Catalog topic blocks in Virtual Agent](https://www.servicenow.com/docs/access?context=request-topic-blocks-va&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    **Note:** Now Mobile opens the item in Mobile Employee Service Portal \(mesp\).

    ![Submit a Request virtual agent chatbot dialogue.](../../service-catalog-management/image/SubmitaRequest.png)


## Walk-up Check-in

Users can check into a ServiceNow® Walk-up Experience location and secure a place in the queue, or they can schedule an appointment at a walk-up location for themselves. Users can also schedule an appointment on behalf of someone else.

Requirement: [Walk-up Experience plugin](../../walk-up-experience/task/activate-walkup-experience.md) \(com.snc.walkup\)

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Walk-up Check-in topic.](../image/WalkupCheckin.png)

![Video icon](../image/icon-video-link.png) [Virtual Agent Academy: Get service faster with Virtual Agent and Walk-Up Experience](https://www.youtube.com/watch?v=hE5weOQVFe4&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH) \(video from the Virtual Agent Academy\)

## Windows 365 Cloud PC

Users can request a Microsoft 365 Cloud PC for themselves through a Virtual Agent conversation.​ The provisioning is reviewed by the user's manager.

Requirements:

-   [Microsoft Azure Active Directory spoke](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \(com.sn.azure\_ad.spoke\)
-   Integration with the Microsoft service via ServiceNow® Integration Hub and Workflow Studio

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

![Windows 365 Cloud PC topic.](../image/CloudPC1.png)

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

