---
title: Proactive Triggers release notes
description: Version history for the Proactive Triggers application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ci-proactive-triggers.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Proactive Triggers release notes

Version history for the Proactive Triggers application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.10 - December 2025 \(Zurich\)**

    Fixed bugs.

-   **Version 3.0.9 - August 2025 \(Zurich\)**
    -   Fixed:
        -   Proactive trigger \(Message Popups\) getting triggered even when a scripted condition is false in non-English languages.
        -   Issue preventing proactive trigger pop-up message from appearing, in certain conditions.
-   **Version 3.0.6 - November 2024 \(Xanadu\)**

    Bug fixes.

-   **Version 3.0.5 - August 2024 \(Xanadu\)**

    Support Migration of NLU Proactive actions to LLM if Now Assist is enabled as part of topic migration.

-   **Version 2.4.0 - November 2023**

    Minor fixes.

-   **Version 2.0.0 - August 2023 \(Vancouver\)**
    -   New:
        -   Proactive rich-text messages that launches a selection of Virtual Agent topics buttons.
        -   Trigger message based on event or business rules using the Proactive Triggers API.
        -   Sample:Proactive Trigger on Search business rule and related trigger type, rule, and action.
    -   Changed: Virtual Agent Web client Proactive message UI changes.
-   **Version 1.1.0 - May 2023**
    -   Changed:
        -   Updated all admin fields and annotations to include translations.
        -   Added tooltips on Frequency and Delay time fields.
        -   Improved annotation when creating action from rule.
    -   Fixed:
        -   Deleting an active rule inserts an inactive rule with empty values in table.
        -   Proactive Trigger rules with nonzero delay times and the Live Agent trigger type do not trigger.
        -   Rules with no actions can cause other rules not to execute.
        -   Fixed Get\_action language failure.
-   **Version 1.0.0 - February 2023**
    -   Proactive Triggers is a ServiceNow Store application that is available to all Virtual Agent web client customers by default. Proactive Triggers can increase adoption of Virtual Agent by proactively sending context-specific messages to end users. These messages could be as simple as a welcome greeting or as complex as any published Virtual Agent conversation. A rich text pop-up message provides users with actions according to real-time Proactive Triggers data. When end users engage with the Proactive message, the Virtual Agent topic associated with that message runs.
    -   Proactive admins use Proactive rules to define when, where, and how to engage with customers. These rules have related actions.
    -   The Proactive action defines what is executed to the client side when the rule runs. The Trigger type defines the context in which the rule runs \(for example, URL, catalog item, or knowledge article\). The frequency defines when the rule runs and to whom the rule applies. Admins define this criteria based on when customers are most likely need help, such as when ordering equipment, opening an incident/case, or viewing information in a Knowledge Base article. Proactive rules can be applied to any defined URL, including service portal, catalog item, or external site.

**Parent Topic:**[ServiceNow Store - Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-conversational-interfaces-landing.md)

