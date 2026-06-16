---
title: Omnichannel Callback release notes
description: Version history for the Omnichannel Callback application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-omnichannel-callback.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Omnichannel Callback release notes

Version history for the Omnichannel Callback application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.8 - June 2026 \(Australia\)**

    Code refactoring changes and defect fixes. There are no major changes in functionality.

-   **Version 2.0.7 - March 2026 \(Australia\)**
    -   Add a boolean column in callback table to identify if the callback is created by agent
    -   Defect fixes.
-   **Version 2.0.5 - December 2025 \(Zurich\)**
    -   UI Policy script to remove specific reason\_type choices for end user.
    -   \[Callback\] Time between reattempts of callback must be configurable \(\#205\)
    -   Callback assign to fix for handling on initial callback external request.
    -   \[CCaaS Callback\] Need data model support to enable CCaaS to route callbacks to the agent that scheduled the callback
    -   The datamodel changes to store metadata related to voicemail in callback task table
    -   Added new field in callback table and system property configuration
    -   Need support to associate source records like lead, oppt to callback task record
    -   Added callback\_author role and ACLs for editing Callback Tasks.
    -   \[CCaaS Callback\]\[VA\] Support for requesting CCaaS callback \(immediate/scheduled\), viewing scheduled callbacks and rescheduling/cancelling callbacks \(\#223\)
    -   \[CCaaS Callback\] Central mechanism to enable use of CCaaS APIs when user requests callback from VA, Web Embeddebable, Portal, EM and Agent Workspace \(\#220\)
    -   Central mechanism to call CCass API - update sys\_cs\_callback on getting resposne from third party
    -   Fixed bugs
-   **Version 2.0.2 - August 2025 \(Zurich\)**
    -   Support external callback and storing additional parameters that CCaaS provides
    -   External callbacks should not be routed by default callback request routing
    -   Populate callback assigned to field with first interaction assigned to field of callback
    -   Enhanced Security Model Adoption Zurich Directive for callback
    -   Callback create, update and reattempt API
-   **Version 1.10.8 - August 2024 \(Xanadu\)**

    Minor bug fixes.

-   **Version 1.10.1 - November 2023**

    Minor fixes.

-   **Version 1.9.0 - August 2023 \(Vancouver\)**

    Minor fixes.

-   **Version 1.8.3 - May 2023**

    Fixed: Incorrect choice value for reason\_type in sys\_cs\_callback.

-   **Version 1.8.1 - February 2023**
    -   New:
        -   Added support for scheduled callback at a specified date and time in addition to auto-scheduled callback.
        -   Added support for video as an outbound channel to complement existing support for voice.
        -   Support callback on all existing conversational integration channels, for example, Slack, Microsoft Teams, Web, Mobile, Facebook Messenger, Facebook Workplace, in addition to Phone.
        -   Added new out-of-the-box topics for messaging and chat channels.
        -   Support for customers using both Virtual Agent chat and Virtual Agent IVR in the same instance.
    -   Changed: Admin configuration has been moved from Conversational Interfaces &gt; Settings &gt; Virtual Agent to Converstional Interfaces &gt; Settings &gt; General to accommodate added support for all integration channels.
-   **Version 1.5.2 - November 2022**

    New:

    -   Added reason field for agents to enter the reason for closing or re-attempting callback tasks.
    -   Added support for transcript and recording for voice callback.
-   **Version 1.1.0 - August 2022**

    Omnichannel Callback adds new set of platform capabilities that enable other ServiceNow applications to display or announce callback options to the users.


**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

