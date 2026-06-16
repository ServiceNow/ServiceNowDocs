---
title: ITSM Virtual Agent Conversations release notes
description: Version history for the ServiceNow ITSM Virtual Agent Conversations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itsm-va-conversations.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# ITSM Virtual Agent Conversations release notes

Version history for the ServiceNow® ITSM Virtual Agent Conversations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.3.2 - March 2026**

    Fixed: GlideDateTime objects display inconsistent date formats when queried across different records in the same table.

-   **Version 9.3.1 - December 2025**
    -   Fixed: Fixed Virtual Agent templates appearing on incident forms.
    -   Removed: Remove deprecated Virtual Agent topic: “Get Password Reset Link.”
-   **Version 9.2.4 - May 2025**

    Fixed minor bugs.

-   **Version 9.2.3 - November 2024**

    Fixed: Error while publishing the "Add Comment To Incident" topic.

-   **Version 9.2.2 - August 2024**

    Fixed: Resolved issue where text input control is sending topic Sys\_Id as plain text instead of prompt.

-   **Version 9.2.1 - February 2024**

    Fixed: Resolved issue where walkup appointment details card was showing invalid date errors

-   **Version 9.2.0 - November 2023**

    Changed: Renamed actionable notification topics to be easier to read.

-   **Version 9.1.0 - August 2023**
    -   New:
        -   Added available pre-built topics and plugin dependencies content in the Virtual Agent Designer.
        -   Added email templates for Issue Auto Resolution.
        -   Enabled dialog act for pre-built topics.
    -   Fixed:
        -   Resolved issue with activating actionable notification flows.
        -   Updated category for actionable notifications.
        -   Updated Schedule Meeting EXO topic to handle multiple user records issue.
-   **Version 9.0.1 - May 2023**
    -   New: Enabled AI Search capability to Issue Auto Resolution incident record
    -   Changed: Refactored topics to use newer message localization method
-   **Version 8.2.1 - February 2023**
    -   New:
        -   New topic, Manage Meeting EXO v1.0 to help user manage their meeting.
            -   Schedule a meeting
            -   Reschedule a meeting
            -   Cancel one/all meetings
    -   Changed: Manage Meeting EXO topic has been marked deprecated
-   **Version 8.1.2 - November 2022**

    New: Deflection nodes added to Manage Walk-up \(Template\) topic to instrument whether the users were helped while using the topic.

-   **Version 8.0.1 - August 2022**
    -   New:
        -   Self service topic to help users manage their Walk-up check-ins and appointments. 'Manage Walk-up \(Template\)' will help requesters check in to a queue, or book an in-person/remote appointments or manage their appointments from Virtual Agent Conversation.
        -   Separate topic blocks to take the required action on Walk-up appointments and check-ins
            -   Walk-up Check-in
            -   Schedule Walk-up Appointment
            -   Reschedule Walk-up Appointment
            -   Cancel Walk-up Appointment
    -   Changed:
        -   Walk-up Check-in \(Template\) topic and its associated NLU intent has been deprecated.
        -   Submit A Request \(Template\) topic and its associated NLU intent has been deprecated
-   **Version 7.1.4 - July 2022**
    -   Fixed:
        -   Minor issues with OOB topics fixed
            -   Walk-up Check-in
            -   Submit a Request
            -   Create Office 365 Group
-   **Version 7.1.2 - May 2022 \(San Diego\)**
    -   New:
        -   Multi-language support: Mapped ITSM prebuilt topics to new languages supported by ITSM Virtual Agent.
            -   French Canadian
            -   Dutch
        -   Troubleshoot Slow Computer \(Agent Clicent Collector\) topic helps end users fix their slow computer using Virtual Agent. Topic is built using Agent Client Collector \(ACC\) for automated remediation.
        -   Deflection tracker: Deflection tracker added to topics to save time. New deflection tracker has been added to prebuilt topics catering to fulfillers and requester topics.
    -   Changed:
        -   Updated Walk-up Checkin topic to include entity recognition.
        -   Updated Manage Meeting \(EXO\) topic to enable Webex online meeting scheduling, using Manage Meeting topic.
        -   Updated Set OOO reply Exchange Online \(Template\) to include entity recognition to identify the dates when a user will be out of office.
        -   Updated Set OOO reply Exchange Server \(Template\) to include entity recognition to identify the dates when a user will be out of office.
-   **Version 6.5.3 - May 2022 \(Rome\)**
    -   Fixed:
        -   Submit a Request:
            -   Issue with showing images for catalog items on the Virtual Agent bot
            -   Inactive catalog item being surfaced on search
-   **Version 6.4.1 - February 2022**
    -   New: Mapping of ITSM OOB Topics to new Language Models \(Spanish, Japanese, Italian, Chinese \(Simplified\), Brazilian Portuguese &amp; Korean\)
    -   Changed: Updated 'Submit a Request' topic to utilize the new entity and vocabulary source to improve catalog search
-   **Version 6.3.4 - December 2021**
    -   New:
        -   Provision Citrix Desktop/Application: Helps users get a new Citrix desktop or applications provisioned.
            -   New topics:
                -   Provision Citrix Desktop/Apps \(Template\)
                -   \_citrix\_workspace\_provision\_
            -   New Notification: Citrix provision notification
            -   Functional dependency: Citrix IT Service Management Connector
        -   Manage Meeting \(MS Exchange Server\): Helps on-prem users to schedule, reschedule, and cancel meetings.
            -   New topic: Manage Meetings EXS \(Template\)
            -   Functional dependency: Microsoft Exchange Server
        -   Windows 365 Cloud PC: With this update, any request for Windows 365 Cloud PC would require an approval from manager before getting provisioned.
            -   Topic Updated: Windows 365 Cloud PC \(Template\)
            -   Flow created for approval: Request Windows 365 Cloud PC
            -   Catalog Item: Windows 365 Cloud PC
            -   Functional dependency: Azure AD
-   **Version 6.2.3 - November 2021**
    -   Fixed:
        -   Fixes for book Conference Room EXO and EXS topics
        -   MS Teams Custom control is shipped as active
    -   Changed:
        -   Updated Create Change Request and Create Problem topics to show Configuration Item \(CI\) list
        -   Updated RSA Token topic to support device entity
        -   Changes to GuestWifiAccess Topic, Submit a Request, Check IT Ticket Status topics
        -   Updated content for Troubleshoot MS teams topic block
-   **Version 6.2.0 - October 2021**
    -   New:
        -   New topic: Local Admin Access – ACC \(Template\) - Helps user get admin access on their MAC device. The agent \(Agent Client Collector i.e. ACC\) running on the user's device provides the access automatically.
        -   New actionable notification: Software Installation
    -   Changed:
        -   Add User To Office 365 Group \(Template\): Add multiple users simultaneously
        -   Deflection tracker added to below self-service topics:
            -   Local Admin Access \(Template\)
            -   Book Conference Room EXO
            -   Book Conference Room OnPrem \(Template\)
            -   My Assigned Equipment \(Template\)
            -   Service Disruptions \(Template\)
            -   Open IT Ticket 2.0 \(Template\)
            -   VPN Connectivity \(Template\)
            -   Check IT Ticket Status \(Template\)
            -   Escalate IT Ticket \(Template\)
            -   Meeting Room Issues \(Template\)
            -   Guest Wifi Access \(Template\)
            -   Walk-up Check-in
            -   Process Approval \(Template\)
            -   Submit a request \(Template\)
-   **Version 6.1.2 - September 2021**
    -   New:
        -   Windows 365 Cloud PC \(Template\) topic helps users provision a Windows 365 Cloud PC from Virtual Agent conversation.
        -   MS Teams custom control: User can fill out all the details of a meeting before checking for availability and setting up the meeting.
    -   Changed:
        -   Deflection Tracker added to topics to improve the Virtual Agent Analytics:
            -   Email Setup \(Template\)
            -   Repository Access \(Template\)
            -   RSA Token \(Template\)
            -   Get Zoom Meeting Recording \(Template\)
            -   Email Issues \(Template\)
            -   Printer Issues \(Template\)
            -   Collaboration Applications \(Template\)
            -   Hardware Issues \(Template\)
            -   Add User to AD Group \(Template\)
            -   Remove User from AD Group \(Template\)
            -   Create AD Distribution Group \(Template\)
            -   Show My AD Group Membership \(Template\)
            -   Add Owner to Office 365 Group \(Template\)
            -   Remove Office 365 group Owner \(Template\)
            -   Create Office 365 Group \(Template\)
            -   Add User to Office 365 Group \(Template\)
            -   Remove Office 365 group Users \(Template\)
            -   Get Office 365 Group Details \(Template\)
-   **Version 6.0.4 - July 2021**
    -   New: Mapped topics to French and German NLU model intents
    -   Changed: Actionable notification framework upgrade
    -   Removed: Manage Distribution List VA topic \(Deprecated\)
-   **Version 5.4.1 - June 2021**
    -   New: Topic Block to add MS team meeting link
    -   Changed:
        -   Create Zoom Meeting Link \(Template\)
        -   Set OOO reply Exchange Server \(Template\)
-   **Version 5.3.1 - May 2021**
    -   New: Manage meeting topic to schedule, reschedule and cancel any meeting as a host
    -   Change: Customisable OOO message for Exchange Server
-   **Version 5.2.3 - April 2021**
    -   New:
        -   Actionable Notifications
            -   Approve Topic
            -   Reject Topic
            -   Show Details Topic
        -   Hardware Issues Topic
        -   Incident Auto Resolution and Topic Mapping
    -   Changed:
        -   Get Zoom Meeting Recording Topic
        -   Exchange Online Topics
            -   Set OOO Automatic Reply EXO
        -   Exchange Server Topics
            -   Set OOO Automatic Reply OnPrem
-   **Version 5.1.3 - March 2021**
    -   New:
        -   Actionable Notifications
            -   Approver - Request Approval Notification
            -   Approver - Requested Item Approval Notification
            -   End User - Request Open on Behalf Of
    -   Changed:
        -   Updated existing Get Zoom Meeting Recording topic to provide option for sharing recording to calendar invite attendees.
        -   Refactored additional topics to leverage Rich Text Editor.
        -   Flagged Get Password Reset Link topic for deprecation.
-   **Version 5.0.3 - February 2021**
    -   New:
        -   Get Zoom Meeting Recording Topic
        -   Actionable Notifications
            -   Incidents
                -   Service Desk opened incident on behalf of user
                -   Knowledge base article attached
                -   New Comments
                -   Incident Resolved
            -   Requested Item - Comments
        -   Added support for Incident Auto-Resolution topics
    -   Changed:
        -   Refactored existing topics to leverage Rich Text Editor
-   **Version 4.2.3 - January 2021**
    -   New:
        -   Exchange Online TopicsBook Conference Room EXO
        -   Exchange Server TopicsBook Conference Room OnPrem
    -   Fixed: Resolved minor translation issues with topics.
-   **Version 4.1.3 - December 2020**
    -   New:
        -   Microsoft Active Directory Group Management Topics
            -   Create Distribution List
            -   Add User to a Distribution List
            -   Remove User from a Distribution List
            -   Show Membership Details
        -   Exchange Online Topics
            -   Set Email Auto Reply
        -   Exchange Server Topics
            -   Set Email Auto Reply
        -   Collaboration Software Troubleshooting Topic
        -   Topic Blocks
            -   Add Zoom online meeting link to meeting
            -   MS Teams Troubleshooting
            -   Cisco Webex Troubleshooting
-   **Version 4.0.5 - November 2020**
    -   Changed: Minor changes to error display messages
    -   Removed: Search KB topic was removed to prevent conflicts with the Search Fallback topic
-   **Version 4.0.3 - October 2020**
    -   New:
        -   Office 365 Group Management Topics
            -   Create Office 365 Group
            -   Add User to Office 365 Group
            -   Remove Office 365 Users
            -   Add Owner to Office 365 Group
            -   Remove Office 365 Group Owner
            -   Get Office 365 Group Details
    -   Changed: Updated existing topics to leverage reference choice input control
-   **Version 3.0.4 - July 2020**
    -   New:
        -   5 additional intelligent and dynamic conversation flows to improve user experience.
        -   Pre-built Predictive Intelligence clustering solution definitions to help identify ITSM Virtual Agent conversations that can best support your business.
        -   ITSM Virtual Agent notifications to automatically notify users on the status of incidents and requests. Full release notes can be found below. https://docs.servicenow.com/bundle/paris-release-notes/page/release-notes/it-service-management/itsm-virtual-agent-rn.html

**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

