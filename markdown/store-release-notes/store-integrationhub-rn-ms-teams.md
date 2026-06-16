---
title: Microsoft Teams Graph Spoke release notes
description: Version history for the Integration Hub Microsoft Teams Graph Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-teams.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Teams Graph Spoke release notes

Version history for the Integration Hub Microsoft Teams Graph Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.5.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 4.4.1 - February 2026**

    Fixed - Action: Add Member to Channel

-   **Version 4.4.0 - November 2025**

    Fixed - Security defect related to read-only field.

-   **Version 4.3.0 - September 2025**

    Fixed - Required ACL\(s\) or Role\(s\) for agents.

-   **Version 4.2.1 - August 2025**

    Fixed - AI Agents: Agent capabilities, proficiency, and description

-   **Version 4.2.0 - May 2025**

    Minor release with new AI agents.

-   **Version 4.1.2 - December 2024**

    Fixed: Delta token compatibility.

-   **Version 4.1.1 - September 2024**

    Fixed a performance issue.

-   **Version 4.1.0 - May 2024**

    New: Post Record Details action. This is an action similar to Post Incident Details, Post Change Details and Post Problem Details and allows you to choose fields to create a customised message card to be sent for any ServiceNow record.

-   **Version 4.0.1 - September 2023**
    -   Fixed:
        -   Error evaluation setting
        -   Filter XSS from callback URLs
        -   'report\_view' ACLs for multiple tables
-   **Version 4.0.0 - August 2023**
    -   New:
        -   Added equivalent of deprecated actions
            -   Application Management - Install Application to User \(install\_application\_to\_user\_v2\), Look up User App Installation \(look\_up\_user\_app\_installation\)
            -   Calendar Management - Create Meeting \(create\_meeting\_v2\), Delete Meeting \(delete\_meeting\_v2\), Look up Meeting \(look\_up\_meeting\), Look up Meeting Occurrences \(look\_up\_meeting\_occurrences\), Update Meeting \(update\_meeting\_v2\)
            -   Channel Management - Create Channel \(create\_channel\), Delete Channel \(delete\_channel\_v2\), Look up Channel by Name \(look\_up\_channel\_by\_name\), Look up Channel \(look\_up\_channel\), Look up Channels \(look\_up\_channels\_v2\), Look up Channel Messages \(look\_up\_channel\_messages\)
            -   Chat Management - Create Chat \(create\_chat\_v2\), Look up Chats \(look\_up\_chats\_v2\), Look up Message \(look\_up\_message\), Look up Chat Messages \(look\_up\_chat\_messages\), Post Message to Chat \(post\_message\_to\_chat\)
            -   Notification Management - Post Change Details \(post\_change\_details\_v2\), Post Incident Details \(post\_incident\_details\), Post Message \(post\_message\), Post Problem Details \(post\_problem\_details\), Post Reply to Message \(post\_reply\_to\_message\_v2\)
            -   Team Management - Archive Team \(archive\_team\_v2\), Create Team \(create\_team\_v2\), Look up Team \(look\_up\_team\), Look up Teams by User \(look\_up\_teams\_by\_user\), Unarchive Team \(unarchive\_team\_v2\), Update Team \(update\_team\_v2\)
            -   Webhook Management - Look up Webhook Subscription \(look\_up\_subscription\), Renew Webhook Subscription \(renew\_webhook\_subscription\_v2\), Subscribe Webhook \(subscribe\_webhook\_v2\), Unsubscribe Webhook \(unsubscribe\_webhook\_v2\)
        -   Added new actions:
            -   Calendar Management - Look up Schedules
            -   Channel Management - Add Member to Channel, Remove Member from Channel, Look up Channel Members
            -   Team Management - Add Member to Team, Delete Team, Remove Member from Team, Look up Team Members Stream
        -   Added sample flow - Post ServiceNow Incident Worknotes Updates to Microsoft Teams Chat
        -   Added API Version in Connection Attributes
    -   Changed:
        -   Calendar Management - Look up Meetings Stream \(look\_up\_meetings\_stream\)
        -   Chat Management - Look up Chat Message Deltas Stream \(look\_up\_chat\_message\_deltas\_stream\), Look up Message Replies Stream \(look\_up\_message\_replies\_stream\)
        -   Webhook Management - Look up Webhook Subscriptions Stream \(look\_up\_subscriptions\_stream\)
        -   Updated subflows to use newer upgraded actions instead of the deprecated ones.
    -   Removed:
        -   Deprecated actions
            -   Application Management - Install Application to User \(install\_application\_to\_user\), Look up User App Installation \(get\_user\_app\_installation\)
            -   Calendar Management - Create Meeting \(create\_meeting\), Delete Meeting \(delete\_meeting\), Look up Meeting by Meeting ID \(look\_up\_meeting\_by\_meeting\_id\), Look up Occurrence Meeting ID \(look\_up\_occurrence\_meeting\_id\), Update Meeting \(update\_meeting\)
            -   Channel Management - Create Channel in a Team \(create\_channel\_in\_a\_team\), Delete Channel \(delete\_channel\), Look up Channel ID by Name \(get\_channel\_id\_by\_name\), Look up Channel Metadata \(get\_channel\_metadata\), Look up Channels by Team or Group ID \(look\_up\_channels\), Look up Messages from Channel \(get\_messages\_from\_channel\)
            -   Chat Management - Create Chat \(create\_chat\), Look up Chats \(look\_up\_chats\) , Look up Message by ID \(look\_up\_message\_by\_id\), Look up Messages from Chat \(get\_messages\_from\_chat\), Send Message to Chat \(send\_message\_in\_a\_chat\)
            -   Notification Management - Post Change Details \(post\_change\_details\), Post Incident Details \(msteamsdemo\), Post Message \(post\_message\_in\_channel\), Post Problem Details \(post\_a\_problem\_\_details\), Post Reply to Message \(post\_reply\_to\_message\)
            -   Team Management - Archive Team \(archive\_team\), Create Team \(create\_team\), Look up Team by Team or Group ID \(get\_team\), Look up Teams by User ID \(list\_teams\), Unarchive Team \(unarchive\_team\), Update Team \(update\_team\)
            -   Webhook Management - Look up Subscription by ID \(look\_up\_subscription\_by\_id\), Renew Webhook Subscription \(renew\_webhook\_subscription\), Subscribe Webhook \(subscribe\_webhook\), Unsubscribe Webhook \(unsubscribe\_webhook\)
-   **Version 3.7.4 - September 2022**

    Patch version of Microsoft Teams Graph Spoke for IntegrationHub. This version includes a fix to improve installation performance of spoke.

-   **Version 3.7.1 - August 2022**

    Fixed: Patch release of the Microsoft Teams Spoke for IntegrationHub. This version includes a fix for display name that is not appearing in the output of these actions - Look up Teams by Team and Look up Teams by Group ID.

-   **Version 3.7.0 - June 2022**

    New: Minor release of Microsoft Teams Graph Spoke. This version adds 2 new actions - Create Chat and Send Message in a Chat, and a fix for error handling.

-   **Version 3.6.6 - May 2022**

    Fixed: Patch release of Microsoft Teams Graph Spoke. This version fixes an issue with Mentions input in Post Message action.

-   **Version 3.6.5 - February 2022**

    New: Added new actions: Create, look up, update, and delete meeting

-   **Version 3.5.2 - November 2021**

    Fixed: Patch release of Microsoft Teams Graph Spoke for IntegrationHub. This release fixes a security issue.

-   **Version 3.5.1 - September 2021**

    Fixed: Patch release of the MS Teams Graph spoke. This version includes two fixes.

-   **Version 3.5.0 - August 2021**
    -   Updated some actions to allow adding attachment
    -   Webhook management
    -   Update some actions from raw JSON string to Objects so that user can drag-n-drop data pills to build the workflow
-   **Version 3.4.0 - June 2021**

    Minor release of the Microsoft Teams Graph spoke for IntegrationHub. This version includes two new actions: 'Get User App Installation' and 'Install Application to User'.

-   **Version 3.3.0 - January 2021**

    Patch release for the Microsoft Teams Graph spoke on IntegrationHub.

-   **Version 3.2.0 - September 2020**

    Licensing patch for the Microsoft Teams Graph spoke on IntegrationHub.

-   **Version 3.0.0 - April 2020**

    Licensing patch for the Microsoft Teams Graph spoke on IntegrationHub.

-   **Version 1.0.1 - August 2019**

    Licensing patch for the Microsoft Teams Graph spoke on Integration Hub

-   **Version 1.0.0 - April 2019**
    -   Team Management
        -   Create Team
        -   Update Team
        -   Get Team
        -   Archive Team
        -   Unarchive Team
    -   Channel Management
        -   Create Channel in a Team
        -   Get Channel Metadata
        -   Get Channel ID by Name
        -   Delete Channel

