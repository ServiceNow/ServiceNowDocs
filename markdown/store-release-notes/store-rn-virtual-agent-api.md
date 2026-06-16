---
title: Virtual Agent API release notes
description: Version history for the Virtual Agent API on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-virtual-agent-api.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Virtual Agent API release notes

Version history for the Virtual Agent API on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.4.0 - June 2026 \(Australia\)**

    Changes to support nextwave experience and defect fixes.

-   **Version 4.3.0 - April 2026 \(Australia\)**

    New: VA API updated to support Off Glide functionality.

-   **Version 4.2.0 - April 2026 \(Zurich\)**

    Changed: Off-Glide changes to support monthly releases.

-   **Version 3.15.6 - April 2026 \(Yokohama\)**

    Fixed: Fixed a defect Back button to be changed to Camel case.

-   **Version 4.1.2 - March 2026 \(Australia\)**
    -   Send appIboundId in response for custom provider applications.
    -   Send agent-initiated flag in VA API response.
    -   Add Update Context Vars action in VA API.
    -   Fixed a few defects.
-   **Version 4.1.1 - December 2025 \(Zurich\)**
    -   Consolidated multiple dynamic loaders messages into one
    -   Added support for streaming in VA API
    -   Removed description field from carousel options in synthesized response
    -   Updated base system record in sys\_now\_assist\_channel\_config and now\_assist\_va\_search\_results\_output\_type
    -   Fixed defects for VA API
-   **Version 4.0.3 - October 2025**

    Added config files for Bot to Bot.

-   **Version 4.0.1 - September 2025 \(Zurich\)**

    Fixed bugs.

-   **Version 3.15.1 - September 2025 \(Yokohama\)**

    Fixed bugs.

-   **Version 3.14.6 - August 2025**

    Minor bugs.

-   **Version 4.0.0 - August 2025 \(Zurich\)**
    -   Include Interaction Id in both sync and sync subflow
    -   Populate interaction subtype from custom adapter property.
    -   Enhanced Security Model Adoption Zurich Directive for VA API
    -   Add fault conversation api in VA API
    -   Empty response for fault conv action if no conv is open
    -   Add send\_history action
    -   \[UI\]Conversational Interfaces-&gt; Settings screen in dark mode is not showing as expected
    -   Fixing start conversation action to work when called twice \(\#408\)
    -   Fixing message not mandatory for action messages
    -   Change third party chat custom adapter property name.
    -   Change Message value for Back,Repeat,Skip and Next keywords
-   **Version 3.14.7 - August 2025 \(Xanadu\)**

    Minor bugs.

-   **Version 3.14.5 - May 2025 \(Yokohama\)**

    Fixed minor bugs.

-   **Version 3.14.3 - February 2025 \(Yokohama\)**

    Fixed a bug pertaining to incorrect survey values being set in the assessment table through the bot-to-bot channel.

-   **Version 3.14.2 - November 2024**
    -   Fixed:
        -   Messages sent by the user to agent are not visible in the agent chat window if attachment key exists in payload
        -   Evaluated sandbox access for client callable script includes
-   **Version 3.14.1 - August 2024 \(Xanadu\)**

    Changed: Virtual agent API now uses server side pagination.

-   **Version 3.10.0 - February 2024 \(Washington DC\)**
    -   New:
        -   Migrated sn\_va\_as\_service\_cc\_agent\_mapping table to External Agent Management Util Pack.
        -   Added the ability to set user time zone without an active conversation.
    -   Removed: Dependency on Omnichannel Callback
-   **Version 3.9.0 - November 2023**
    -   New: Performance changes and multi-part response translation support for ServiceNow supported languages.
    -   Minor fixes.
-   **Version 3.8.1 - August 2023 \(Vancouver\)**
    -   New: Virtual Agent API response includes file limits \(file size and number of files\) when input control is File Picker.
    -   Minor fixes.
-   **Version 3.7.3 - May 2023**
    -   New:
        -   Added support to upload multiple files through VA API.
        -   Added support for transformation of the VA API response before sending it to the primary bot.
-   **Version 3.7.2 - February 2023**

    Removed: Removed BOT Interconnect and Amazon Connect from this store application and created separate store applications for each.

-   **Version 3.5.2 - November 2022**

    General fixes.

-   **Version 3.2.3 - August 2022**
    -   -   New:
    -   Virtual Agent now integrates with Amazon Connect to enable Interactive Voice Response \(IVR\) between the user and the agent.
    -   New sets of Rest API capabilities that enable Virtual Agent to be used with voice in a Contact Center flow.
-   General fixes.
-   **Version 3.1.0 - May 2022**
    -   Minor release for Virtual Agent API:
        -   New: Bot Interconnect OOTB Integration with Microsoft Azure Power Virtual Agent
        -   Fixed:
            -   Pass the time zone from Bot Interconnect to Secondary Bot in GMT
            -   Using dynamic version in sys\_app\_62c44c6353311010ad77ddeeff7b120c.xml instead of hardcoded version
            -   Reference choice control always shows "no records found" even when there are matching records
            -   Default clean up time for "sys\_cs\_bot\_to\_bot\_control" record in "sys\_auto\_flush" table not available
            -   Add sys\_user active/locked out query condition while linking user account
            -   Unable to run the Microsoft Azure Topic using asynchronous primary topic block
            -   Button rich control gives undefined error on Google Dialogflow, and keyword search doesn't work for Bot Interconnect
            -   For static choice, reference choice, and Boolean inputs, fields are different from the documentation
            -   Security bugs
-   **Version 2.1.0 - October 2021**
    -   New:
        -   Skip node support
        -   System property va.bot.to.bot.logging\_enabled is now available OOB to help with debugging
-   **Version 2.0.0 - August 2021**
    -   New:
        -   Synchronous handshake support
        -   Notifications support in asynchronous mode
        -   Topic switching using topic name or topic intent name
        -   Typing indicator support
        -   Node-skipping support for topics that use it
        -   Additional rich control support, including table, HTML, multi-flow, and rich text
        -   Custom control support
        -   Additional Agent Chat support:
            -   Agent name and avatar
            -   Agent wait time
            -   Pass chat history
        -   Enriched requests from primary bot:
            -   System parameters and context variables
            -   User timezone
-   **Version 1.3.0 - April 2021**
    -   Fixed:
        -   Logger that is enabled through the va.bot.to.bot.logging\_enabled system property.
        -   Cross-scope privileges.
-   **Version 1.0.9 - February 2021**

    New: Use the Virtual Agent API to integrate Virtual Agent and/or Live Agent in any conversational interface. With this API, you can:Integrate a primary bot from your bot ecosystem with Virtual Agent and/or Live Agent as a specialized service delivery bot. Integrate Virtual Agent and/or Live Agent with any channel that supports a conversational interface.

-   **Version 1.0.9 - August 2020**
    -   Initial Release: Use the Virtual Agent API to integrate Virtual Agent and/or Live Agent in any conversational interface. With this API, you can:
        -   Integrate a primary bot from your bot ecosystem with Virtual Agent and/or Live Agent as a specialized service delivery bot.
        -   Integrate Virtual Agent and/or Live Agent with any channel that supports a conversational interface.

**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

