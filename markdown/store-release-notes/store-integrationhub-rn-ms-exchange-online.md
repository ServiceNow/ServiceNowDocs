---
title: Microsoft Exchange Online Spoke release notes
description: Version history for the Integration Hub Microsoft Exchange Online Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-exchange-online.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Exchange Online Spoke release notes

Version history for the Integration Hub Microsoft Exchange Online Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026**

    Fixed: Streamline ACLs

-   **Version 3.14.1 - June 2026**

    Fixed: Retrieve Reservation time format issue.

-   **Version 3.13.0 - March 2026**

    New: Enhance the recurring spoke action to support all exchange options.

-   **Version 3.12.0 - November 2025**

    New: Modifications to support Meeting scheduler AI agent, added 2 subflows, and modified 1 action.

-   **Version 3.11.0 - September 2025**

    Added required ACLs or Roles as per the AI Security Directive guidelines.

-   **Version 3.10.0 - August 2025**
    -   Fixed:
        -   1. Microsoft Exchange Online Spoke AI Agents - March Release : Agents Renaming and Output transformation strategy set to None.
        -   2. "Look up Calendar Views Stream - with Parent Alias" data stream action was broken for different date/time formats at system level other than default date format.
-   **Version 3.9.1 - May 2025**

    Minor release with new AI agents.

-   **Version 3.8.0 - March 2025**

    Minor release with new AI agents.

-   **Version 3.7.3 - December 2024**

    Fixed: Date format support in Look up Calendar View Stream action.

-   **Version 3.7.2 - September 2024**

    Fix for a deleted table that was getting referenced in flow.

-   **Version 3.7.1 - August 2024**

    New: UI action on reservable sync configuration record and populating records.

-   **Version 3.6.5 - May 2024**

    Security fix.

-   **Version 3.6.4 - February 2024**

    Fixed for Start and End date for all day reservations are not set correctly in Events table.

-   **Version 3.6.3 - December 2023**

    Fixed: Fix for Subflow "Delete Event Record" is randomly deleting other events.

-   **Version 3.6.1 - September 2023**
    -   Fixed:
        -   To the Look up MailBox Flow action
        -   The "sn\_ex\_online\_spke.Microsoft Exchange Online Admin" is the only role which is required to access the 'sn\_ex\_online\_spke\_events' table
-   **Version 3.6.0 - August 2023**

    Added feature to notify admin in case exchange online subscription renewal fails for unknown reasons.

-   **Version 3.5.1 - June 2023**

    ATTENTION: Use of this product requires a license for either Integration Hub Professional or HR Service Delivery.

    ServiceNow, as the system of engagement, provides a one-stop-shop for customers to collaborate and communicate with their stakeholders more effectively. By using the Microsoft Exchange Online spoke, the ServiceNow application can now set up meetings and send emails to the customer's teammates or external parties easily. Combing with workflow automation in Flow Designer, this bi-directional integration can also notify the customers whether their meeting has been accepted or declined.

    When both ServiceNow and Microsoft Exchange Online do collaborations together, the possibilities are endless.

-   **Version 3.5.0 - May 2023**
    -   Added a new column to Events table to store the online meeting link
    -   Fixed: Unable to delete events in spoke events table when override alias is enabled
-   **Version 3.4.0 - December 2022**

    Added "Create or Update Subscriptions for Resources" sample subflow for manage subscription lifecycle

-   **Version 3.3.1 - September 2022**

    Patch release of Microsoft Exchange Online Spoke for IntegrationHub. This version includes fixes to improve the installation performance of the spoke, intermittent issues \(Error 429\) in the flow for actions \(Create Calendar Event, Create Subscriptions\), and issues with Retry Policies.

-   **Version 3.3.0 - August 2022**

    New: The minor release of Microsoft Exchange Online Spoke for IntegrationHub. This version adds the functionality to be able to make a reservation without blocking the outlook calendar.

-   **Version 3.2.3 - May 2022**

    Changed: Patch release of Microsoft Exchange Online Spoke. This version increases the field length of Location column in sn\_ex\_online\_spke\_events table.

-   **Version 3.2.2 - April 2022**

    New: Patch release for Microsoft Exchange Online Spoke. This version includes a missing dependency.

-   **Version 3.2.1 - February 2022**

    Fixed: Fixed script to update field length for fields if the table already exists on the instance.

-   **Version 3.1.0 - December 2021**
    -   New: Minor release of Microsoft Exchange Online Spoke for IntegrationHub. This version adds 4 new actions - Create Mailbox, Delete Mailbox, Enable Mailbox, Look up Mailbox
    -   Fixed: This version includes a fix for hardcoded secrets.
-   **Version 3.0.0 - September 2021**

    New: Functionality to look up Out of Office Settings

-   **Version 2.0.2 - July 2021**

    Changed: Patch Release of Microsoft Exchange Online Spoke for IntegrationHub. This version includes fixes to missing error messages in mail management.

-   **Version 1.3.0 - March 2021**

    Minor release of Microsoft Exchange Online spoke for IntegrationHub. This version adds a new action 'Send Mail'.

-   **Version 1.2.0 - December 2020**

    Minor release of Microsoft Exchange Online spoke for IntegrationHub. This version adds functionality related to Look Up Calendar View.

-   **Version 1.1.1 - November 2020**

    Minor release of Microsoft Exchange Online spoke for Integration Hub.

-   **Version 2.5.0 - October 2019**

    Provides actions to automate calendar and mail management in Microsoft Exchange Online.


