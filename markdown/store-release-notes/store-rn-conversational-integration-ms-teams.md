---
title: Conversational Integration with Microsoft Teams release notes
description: Version history for the Conversational Integration with Microsoft Teams on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-conversational-integration-ms-teams.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Conversational Integration with Microsoft Teams release notes

Version history for the Conversational Integration with Microsoft Teams on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.3.4 - June 2026 \(Australia\)**
    -   Fixed:
        -   Ensure "skip" is honored
        -   Adjustments to Copilot manifests
        -   Resolves issue where LLM conversations would get stuck in the thinking stage
        -   Accidental double processing messages being sent to the end user
        -   Stream activities for all transformers
        -   Ensure messages always send in the correct order when streaming is enabled
    -   Enhancement\(s\): Pre-selected choices in pickers
-   **Version 10.3.1 - March 2026 \(Australia\)**
    -   Fixed: Self-configured bot issue for bots deployed after 10/22/2025 due to tenancy change from Microsoft
    -   Fixed: Supported additional file types in live agent conversation
    -   Changed Various experience enhancements and big fixes
-   **Version 10.3.0 - December 2025 \(Zurich\)**

    Minor bug fixes and enhancements

-   **Version 10.2.0 - October 2025**
    -   Streaming is enabled for Teams and Copilot with the Assistant configuration
    -   Enhancements to the processing and streaming messages
    -   Minor defects addressed
-   **Version 10.1.1 - September 2025 \(Zurich\)**

    New: Migrated to Custom Engine Agent, a new agent framework from Microsoft that enables end-to-end conversational VA capabilities within Microsoft 365 Copilot. Note that live agent interactions and notifications are not supported.

-   **Version 10.0.3 - September 2025 \(Yokohama\)**

    Minor bug fixes.

-   **Version 10.0.2 - August 2025 \(Yokohama\)**
    -   Enhanced the choice picker experience for Microsoft Teams
    -   New native Microsoft Teams components
        -   AI label for Now Assist responses
        -   Feedback loop for Now Assist responses
    -   Improved configurations to enable Copilot
-   **Version 9.2.0 - May 2025**
    -   New: Added people card component that shows up within a synthesized response in a Teams conversation.
    -   Fixed: Minor bugs in Copilot and Teams experiences
-   **Version 9.1.0 - March 2025 \(Yokohama\)**

    New: Microsoft Teams now supports streamed message for all Now Assist responses.

-   **Version 9.0.0 - February 2025 \(Yokohama\)**

    Minor improvements and bug fixes for the Microsoft Copilot integration.

-   **Version 8.1.1 - January 2025 \(Xanadu\)**

    Bug fixes for the Microsoft Copilot integration.

-   **Version 7.4.3 - December 2024 \(Washington DC\)**

    Added support for Synthesized Responses for Now Assist conversations.

-   **Version 8.1.0 - November 2024 \(Xanadu\)**
    -   New: Support of Synthesized Responses in Teams
    -   Fixed: HTML code rendering in Teams
-   **Version 8.0.4 - October 2024**

    Fixed an issue while generating manifests for "ServiceNow for Microsoft Teams."

-   **Version 8.0.1 - August 2024 \(Xanadu\)**
    -   New: Copilot integration - Customers can use Copilot to query KB articles and catalog items
    -   New: Copilot integration - Customers wanting to integrate ServiceNow and Copilot will need to use the self-configured bot to integrate and have Now Assist turned on
    -   New: Copilot integration - Customers will need a Copilot and Now Assist license to use functionality, this is not needed to use the Teams integration
-   **Version 7.2.0 - May 2024**

    Minor improvements and bug fixes.

-   **Version 7.1.1 - April 2024 \(Washington DC\)**

    Fix for new scripted pagination introduced by VA Server.

-   **Version 7.1.0 - March 2024 \(Washington DC\)**

    New: Support multi-select for pickers.

-   **Version 7.0.0 - February 2024 \(Washington DC\)**
    -   New: Support for "Now Assist in Virtual Agent"
    -   Fixed minor issues
-   **Version 6.1.0 - November 2023**
    -   New: Support for Now Assist Q&amp;A Genius Results.
    -   Fixes related to message logging.
-   **Version - August 2023**
    -   for Virtual Agent in MS Teams
    -   Improved localization experience and settings
    -   Changed: Pagination of large-size dynamic choice list
-   **Version 4.1.3 - July 2023**

    Fixes on live agent sending non-image attachments to the end user.

-   **Version 5.1.0 - May 2023**
    -   New:
        -   Improved support for multi-attachment upload.
        -   Improved localization experience.
        -   Message batching for improved performance in MS Teams.
    -   Changed: Preventing deletion of adapter-specific configuration records.
    -   Fixed: Deletion of manifest record when the bot is deleted.
-   **Version 4.1.1 - March 2023 \(Tokyo\)**

    This version includes fixes for generating links with markdown and preventing deletion of provider records.

-   **Version 5.0.0 - February 2023**
    -   New:
        -   Improved link opening and authentication experience.
        -   Manifest generator for self-configured bots.
    -   Changed: Improved Admin UI for Microsoft Teams integrations.
    -   Fixed: Improved attachment handling.
-   **Version 4.1.0 - November 2022**
    -   New:
        -   Option to turn off confirmation banner when a user sends a response to Virtual Agent.
        -   Improved catalog ordering experience from AI search.
    -   Fixed:
        -   Display orders of static choice lists.
        -   MS Teams integration on cloned instances.
        -   Live agent messages involving emojis.
-   **Version 3.0.15 - November 2022**
    -   Fixed:
        -   MS Teams integration on cloned instances.
        -   Live agent messages involving emojis.
-   **Version 4.0.1 - August 2022**
    -   New:
        -   One-click uninstallation of Microsoft Teams integration.
        -   MS Teams now displays Promoted topics to end users during conversation.
        -   Batch-messaging is enabled for certain select cards.
    -   Fixed:
        -   Recommendation link in Live Agent diagnosis.
        -   Message with Emoji in live agent chat.
        -   Technical issues: Install Self-configured Bot popup, Node IDs in headers, , 'Go to Tips' button, Card output, YouTube Card and 'Got it' button, Catalogue Card, Live Agent conversation.
        -   Installation issues.
        -   Uninstallation issues.
        -   Bot identification issue.
        -   Issues with System properties.
        -   Post survey issue.
        -   User interface display: Welcome message, Genius AI card, Carousel, Message order.
        -   Translation issues: UI message translation, Field labels on install window.
        -   High memory consumption issue.
        -   Conversation language change issue.
-   **Version 3.0.10 - May 2022**
    -   New:
        -   Run a health check scan using the Conversational Diagnostics app to capture common errors in the Microsoft Teams integration. The app groups errors by category and provides links to relevant Knowledge Base articles for resolution.
        -   Notifications now have a preview of the message content or title, where applicable.
        -   Drop-down picker controls now allow users to type and search for a particular choice from the list.
    -   Changed: Non-card bot response controls are converted into adaptive cards.
    -   Fixed:
        -   User interface display: content preview, KB and incident links, welcome message, task module, pop-up.
        -   Controls: text, table header, carousel option display.
        -   Installation issue.
-   **Version 3.0.6 - February 2022**
    -   New: Unified Logging Framework has been enabled.
    -   Fixed:
        -   The sys\_notification\_channel record configuration issue during upgrade from Paris to Quebec.
        -   The estimated wait time displayed in seconds to be displayed in minutes.
        -   L10 warning.
        -   The order of No and Yes suggestion buttons.
        -   The unified logging backward compatibility condition.
        -   The vendor information for MS Teams app to be set to ServiceNow.
        -   The issue with text on agent wait time card to display in user chosen language.
-   **Version 3.0.5 - December 2021**
    -   New: Content preview is now enabled within Microsoft Teams application for KB articles, catalog items, and incidents records.
    -   Fixed:
        -   Notification delivery issue.
        -   The agent name display issue when user connects to a live agent.
        -   Non-alphabetical order of the reference choice control options on the bot.
        -   Auto-linking failure due to mismatch between 'User Principal Name' and the email of the sys\_user record.
        -   The broken hyper link in the Click here button on the welcome card.
        -   The missing 'VA Teams Inbound' Scripted REST API issue.
-   **Version 3.0.1 - October 2021**
    -   New: Make all card templates in the Conversational Integration with Microsoft Teams available in the same template framework/table.
    -   Fixed:
        -   Security fixes
        -   Multiflow button display in card
        -   Text in Virtual Agent welcome card
        -   Backward compatibility issue
        -   Translation of card text
        -   Unnecessary display of available UI actions after user selection
        -   Reference and Static Choice controls with header card not working
        -   Auto-linking failure due to mismatch between principal user name and user email record
-   **Version 2.0.0 - August 2021**
    -   New:
        -   YouTube URL unfurling.
        -   Support for rich text using markdown in notification messages.
        -   Allow masking of sensitive user input.
        -   Batch linking of Virtual Agent users.
        -   URL redirect to Service Portal page.
    -   Fixes
-   **Version 1.0.4 - March 2021**

    Fixed: Addresses an issue with the installation of the Conversational Integration with Microsoft Teams app by correcting access to a scripted extension point.

-   **Version 1.0.2 - February 2021**
    -   New:
        -   Support for actionable notifications
        -   Users can subscribe to or unsubscribe from notifications

**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

