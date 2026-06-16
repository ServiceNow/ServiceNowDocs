---
title: Zoom spoke release notes
description: Version history for the Integration Hub Zoom spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-zoom.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Zoom spoke release notes

Version history for the Integration Hub Zoom spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.7.0 - June 2026**

    Fixed: Streamline ACLs.

-   **Version 4.6.2 - January 2026**

    Fixed: Defect related to Create Channel tool in Zoom Chat Management AI Agent.

-   **Version 4.6.1 - December 2025**
    -   New:
        -   Agent: Zoom chat manager
        -   Action: Look up Past Meeting Participants Stream
    -   Changed: Agent: Zoom meeting manager, Zoom user manager, Zoom recording: Added data stream actions as tools
-   **Version 4.5.1 - November 2025**
    -   New: Introduced a new subflow ‘Create Zoom Meeting’ and added an inactive action ‘Create Meeting – Simplified’ to enhance meeting creation capabilities
    -   Fixed:
        -   1. Updated table access controls to restrict read access from the admin role, granting it only to MAINT, in alignment with granular admin directives for backend user mapping data
        -   2. Read  only Directive. Refer the global communication for the detailed notes for this directive
-   **Version 4.4.0 - September 2025**

    Fixed - Required ACL\(s\) or Role\(s\) for agents.

-   **Version 4.3.0 - August 2025**
    -   Fixed:
        -   AI Agents: Renaming, and Output transformation strategy
        -   Actions: Look Up Chat Messages
-   **Version 4.2.0 - March 2025**

    Minor release with new AI agents.

-   **Version 4.1.3 - December 2024**

    Fixed: Authentication template.

-   **Version 4.1.2 - December 2023**

    Fixed: Webhook endpoint validation.

-   **Version 4.1.1 - November 2023**

    Fixed: Inadequate ACL for sn\_zoom\_spoke\_user table.

-   **Version 4.1.0 - February 2023**
    -   New: Webhook registry support for participant joined, participant left events.
    -   Changed:
        -   Added support for alternative support for Create Meeting, Update Meeting actions.
        -   Added support for posting permission support for Update Channel action.
-   **Version 4.0.4 - November 2022**

    Fixed: Bug related to Zoom meeting URL found in V4.0.2.

-   **Version 4.0.3 - November 2022 \(True-up\)**
    -   New:
        -   9 Chat Management actions
        -   1 Utility action
    -   Changed: Added timezone input for Create Meeting action
-   **Version 3.1.1 - September 2022**

    Fixed: Improve installation performance of spoke.

-   **Version 3.1.0 - September 2022**

    Minor release of Zoom Spoke for Integration Hub. This version adds two new actions - Look up Meetings Stream \(to list given users meetings\), and Update Meeting \(to update the meeting details for a given meeting\).

-   **Version 3.0.3 - July 2022**

    Fixed: Zoom Meeting Links being generated with Zoom spoke version 3.0.0

-   **Version 3.0.1 - June 2022**
    -   Changed: Patch release of Zoom Spoke. This version includes the below changes:
        -   Update to the order of choices within the action - Update User Settings.
        -   Update of the label for the action - Look up Users Stream.
        -   Update to the order of country list within the action - Update User Phone Settings.
-   **Version 3.0.0 - May 2022**
    -   Changed:
        -   Updated user management by providing actions for user creation and deletion.
        -   Updated user setting management by providing actions for user settings and user phone settings.
        -   Better connection management.
        -   Sample webhook entries, and subflows for inbound events automation.
-   **Version 2.0.4 - May 2022**

    New: This is a patch release and enables creating a meeting with the end time.

-   **Version 2.0.2 - December 2021**

    Changed: Patch release of Zoom Spoke for IntegrationHub. This version includes updates to spoke dependencies.

-   **Version 2.0.1 - September 2021**

    Fixed: Minor bug - unexpected token error at Create Meeting and Add Meeting Registrant actions

-   **Version 2.0.0 - May 2021**

    Major version release for the Zoom spoke.

-   **Version 1.7.0 - April 2021**

    Minor release of the Zoom spoke for IntegrationHub. This version adds functionality related Get Meeting Recordings Settings.

-   **Version 1.6.0 - December 2020**

    Minor release of the Zoom spoke for IntegrationHub. This version adds functionality related Look Up Recordings, Get Meeting Recordings and Look Up Ended Meeting Instances.

-   **Version 1.0.3 - June 2020**

    Patch release of Zoom spoke for IntegrationHub

-   **Version 1.0.2 - September 2019**

    Provides actions to start and manage a Zoom meeting from the ServiceNow instance.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

