---
title: ITSM NLU Model for Virtual Agent Conversations release notes
description: Version history for the ServiceNow ITSM NLU Model for Virtual Agent Conversations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itsm-nlu-model-va.html
release: store
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# ITSM NLU Model for Virtual Agent Conversations release notes

Version history for the ServiceNow® ITSM NLU Model for Virtual Agent Conversations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.2.0 - May 2025**

    Removed: Dependency on ServiceNow Studio \(Legacy\) \(com.glide.dev-studio\).

-   **Version 8.1.1 - August 2024**

    Minor bug fixes.

-   **Version 8.1.0 - August 2023**

    New: Added ITSM Issue Auto Resolution model to allow tuning intents.

-   **Version 8.0.1 - May 2023**

    Changed: Updated Japanese NLU model to improve accuracy.

-   **Version 7.1.1 - February 2023**
    -   Fixed:
        -   English ITSM NLU model should be activated and published out-of-the-box
        -   Minor fixes
-   **Version 7.1.0 - November 2022**
    -   Changed:
        -   English NLU model tune-up
        -   Deprecated Disabled ManageO365, GetPasswordResetLink, HardwareIssue, ReportITIssues and IntelligentOpenITTicket Intents
-   **Version 7.0.0 - August 2022**
    -   New: Updated capability with introduction of \#ManageWalkup NLU intent to help user manage their walk-up visits.
    -   Changed:
        -   \#SubmitARequest intent has been deprecated and has been disabled. Going forward Virtual Agent will leverage AI Search to surface the catalog items for users to request them from Virtual Agent itself
        -   \#WalkupCheckin intent has been deprecated and has been disabled. \#ManageWalkupwould help the user in managing their walk-up visits
-   **Version 6.1.0 - May 2022 \(San Diego\)**
    -   New: Multi-language support: ITSM NLU model added to support French Canadian and Dutch
    -   Changed:
        -   Entity recognition \(NLU model updates\): Added additional entities to below intents to improve user request recongnition and understanding
            -   Walk-up Check-in
            -   Set OOO reply Exchange Online \(Template\)
            -   Set OOO reply Exchange Server \(Template\)
-   **Version 5.5.1 - May 2022 \(Rome\)**
    -   New: Added NLU support for French Canadian and Dutch languages.
    -   Changed: Updated the \#submitARequest intent for NLU Model for German, French, Spanish, Japanese.
-   **Version 5.4.1 - February 2022**
    -   New:
        -   ITSM NLU Models supporting
            -   Spanish
            -   Japanese
            -   Italian
            -   Chinese \(Simplified\)
            -   Brazilian Portuguese
            -   Korean
    -   Changed
        -   Updated SubmitARequest intent
            -   New Vocabulary Source added on Catalog Item \(source\)
            -   Vocabulary source leverages 'name' and 'meta' column in SC\_CAT\_ITEM
        -   New intents and entities added to ITSM NLU Model for French\(FR\) &amp; German\(DE\)
-   **Version 5.3.1 - December 2021**
    -   New: NLU intent ProvisionCitrixSesssions added to support Citrix Desktop or Application provisioning
    -   Changed: NLU intent ResetCitrixSessions has been updated to minimize ambiguity and improve performance
-   **Version 5.2.1 - November 2021**
    -   Fixed:
        -   Updated RSA Token to have device entity related utterances
        -   Updated 'ticketnumber' entity to identify the task and task-number accurately
        -   Updated VirtualDesktopProvision intent
        -   Removed the older/unused model artifact files and ml solution records
-   **Version 5.2.0 - October 2021**
    -   Changed:
        -   Updates to the following ITSM intents:
            -   CheckITTicketStatus
            -   EmailSetup
            -   SubmitARequest
-   **Version 5.1.2 - September 2021**

    New: NLU utterance and intent \(VirtualDesktopProvision\) to help users provision a Windows 365 cloud PC from virtual agent conversation

-   **Version 4.6.1 - August 2021**
    -   Changed:
        -   NLU intents 'IntelligentOpenITTicket' and 'ReportITIssue' have been deprecated.
        -   'OpenITTicket' intent updated with new utterances. To help in creating an IT incident, it is recommended to use OpenITTicket intent.
-   **Version 4.3.1 - May 2021**
    -   New:
        -   NLU Model to manage meetings
        -   NLU Model support for French \(FR\) and German \(DE\)
-   **Version 4.2.1 - April 2021**

    New: Added new intent to support Hardware Issues topic.

-   **Version 4.1.1 - March 2021**

    Changed: Minor optimizations to existing intents.

-   **Version 4.0.1 - February 2021**
    -   New: Added new intent to support Get Zoom Recording topic
    -   Changed: Updated model confidence threshold for Quebec NLU changes
-   **Version 3.2.0 - January 2021**
    -   New: New intent added to support Book Conference Room topic.
    -   Changed:
        -   Below intents tuned to improve performance.
            -   IntelligentOpenITTicket
            -   PrinterIssues
            -   RemoveUserFromGroupDistributionList
            -   WalkupCheckIn
            -   AddUserToGroupDistributionList
-   **Version 3.1.1 - December 2020**
    -   New:
        -   Intents added to support Exchange Online and Server topics
        -   Intent for Collaboration Software Issues topic
-   **Version 3.0.1 - November 2020**

    Fixed: Minor fixes to support compatibility for NLU platform changes

-   **Version 3.0.0 - October 2020**

    New: NLU intents to support new Office 365 group topics

-   **Version 2.0.3 - July 2020**
    -   New
        -   Additional utterances added for greater precision for the following topic conversations:
            -   Escalate IT Ticket
            -   Service Disruptions
            -   Email Setup
            -   VPN Connectivity
            -   Guest WiFi Access
            -   https://docs.servicenow.com/bundle/paris-release-notes/page/release-notes/it-service-management/itsm-virtual-agent-rn.html

