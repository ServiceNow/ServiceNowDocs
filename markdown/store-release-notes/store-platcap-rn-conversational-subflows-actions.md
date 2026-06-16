---
title: Conversational subflows and actions release notes
description: Version history for the Conversational subflows and actions application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-conversational-subflows-actions.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Conversational subflows and actions release notes

Version history for the Conversational subflows and actions application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.2.2 - April 2026 \(Zurich, Australia\)**
    -   Changed:
        -   Updated buttons and AI icon
        -   Changed to new condition builder for Advanced Rule view
-   **Version 29.1.1 - March 2026 \(Zurich\)**
    -   Changed: Get conversational status and fetch skills without reloading flow
    -   Removed: Save and Test from Conversational Skills Panel
-   **Version 28.2.7 - January 2026 \(Yokohama, Zurich, Australia\)**

    Changed: Updated version for General AI Controller dependency version change.

-   **Version 28.1.5 - October 2025 \(Yokohama, Zurich\)**

    NA

-   **Version 26.0.13 - October 2025 \(Xanadu\)**

    New: Enhanced security measures with granular role controls to further safeguard conversational workflows, ensuring data integrity and preventing unauthorized access during runtime.

-   **Version 28.1.4 - September 2025 \(Yokohama, Zurich\)**
    -   New:
        -   Configure multiple skills for a subflow or action, enabling more flexible dialogue design and better modularization across experiences.
        -   Added granular role controls to enhance security, safeguard data integrity, and prevent unauthorized access during runtime.
    -   Changed: The conversational subflow and action settings menu has been moved to the side panel for easier navigation.
-   **Version 27.3.6 - May 2025 \(Yokohama, Zurich\)**
    -   New:
        -   Check for conversational compatible subflows and actions. Run a compatibility check on new or all subflows and actions to determine if they are conversation compatible.
        -   Generate skill and input descriptions for conversational subflows and actions. Configure conversational settings for conversational subflows and actions by generating skill and input descriptions with generative AI.
        -   Set default values for subflow and action inputs. Set a default value for a conversational subflow or action input. Hide subflow or action inputs that have a default value if you don't want users to change the input value in a conversation.
        -   Support additional input data types for conversational subflows and actions. Support conversational subflows and actions that have Dynamic Choice and Array of Objects input types.
-   **Version 27.1.4 - March 2025 \(Yokohama\)**
    -   New:
        -   Provide a new UI experience for the configuration, management and optimization of conversational subflow and actions.
        -   Display conversational compatible and conversational enabled subflows and actions in their own tab.
        -   Display subflow and action output data in a card view.
        -   Provide an execution mode option to run skills either supervised or autonomously.
        -   Provide an option to follow up on skills.
    -   Changed:
        -   Improve the compatibility script that evaluates actions and subflows against compatible data types. The script places items into the conversational compatible and conversational enabled tabs.
        -   Improve the end-user experience by displaying subflow and action output in a card view, providing an option to run skills autonomously, and an option to follow up on skills.
-   **Version 26.0.11 - March 2025 \(Xanadu\)**
    -   New:
        -   Create and configure the conversational skill for Workflow Studio actions and subflows
        -   Run user-configured conversational skills from a Now Assist panel.
-   **Version 27.0.3 - January 2025 \(Yokohama\)**
    -   New:
        -   Added the ability for customers to make subflows and actions conversation compatible.
        -   Added option to enable conversation compatible subflows and actions to be called by conversational interfaces.
        -   Added option to run skills in either autonomous or supervised mode.
    -   Changed:
        -   Improved end user experience to support Card output view.
        -   Improved handling of follow-up skills.
-   **Version 26.0.9 - December 2024 \(Xanadu\)**

    Bug fixes

-   **Version 26.0.8 - December 2024 \(Xanadu\)**
    -   New:
        -   Run a subflow from a conversation
        -   Run an action from a conversation
        -   Configure conversational properties from Workflow Studio
-   **Version 26.0.8 - November 2024**

    Conversational subflows and actions allow end users to complete tasks through conversational interfaces. They capture users' intents when requesting to run specific subflows and actions, along with all necessary details for those subflows and actions. This streamlines the user experience by enabling them to accomplish everything in one place within an agent/AI assistant \(such as Now Assist Panel or Now Assist Virtual Agent\) and channels \(such as MicroSoft Teams or Slack\).


