---
title: Slack spoke release notes
description: Version history for the Integration Hub Slack spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-slack.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Slack spoke release notes

Version history for the Integration Hub Slack spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.0 - June 2026**

    Fixed: Streamline ACLs.

-   **Version 1.8.0 - September 2025**
    -   Fixed:
        -   Required ACL\(s\) or Role\(s\) for agents.
        -   Token refresh for modal via guest user.
-   **Version 1.7.1 - August 2025**
    -   Fixed:
        -   AI Agents: Renaming, and Output transformation strategy
        -   Update OAuth v1 to v2
-   **Version 1.7.0 - March 2025**

    Minor release with new AI agents.

-   **Version 1.6.0 - March 2023**
    -   New: New Action: Open Conversation.
    -   Changed:
        -   Renamed action category from Channel Management to Conversation Management.
        -   Renamed 10 actions.
    -   Fixed: Added support for special characters such as ~.
-   **Version 1.5.10 - December 2022**
    -   New: Localization framework
    -   Fixed: Issue related to approval updated by user, instead of guest
-   **Version 1.5.9 - September 2022**

    Patch version of Slack Spoke for IntegrationHub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.5.8 - October 2021**

    Fixed: This version includes fixes for hardcoded secrets at the Slack configuration, and interceptor being triggered at sys\_decision tables.

-   **Version 1.5.7 - September 2021**

    Fixed: Minor bug where an error was observed within the action - 'Post Response to Slack'

-   **Version 1.5.6 - July 2021**

    Patch release of Slack Spoke for IntegrationHub. This version adds KMF modules for additional security of password2 fields and Rome compatibility. It also includes fixes for custom modal, error at Post Actionable Message, null check in Look Up User action, and the target table field not passed in the payload.

-   **Version 1.5.4 - April 2021**

    Minor release for Slack spoke of IntegrationHub. This version includes configuration of Slack modals.

-   **Version 1.4.0 - January 2021**

    Minor release for the Slack spoke on IntegrationHub. This version includes new action for conversation conformation and changes to LookUp actions.

-   **Version 1.3.4 - December 2020**

    Patch release of Slack spoke for IntegrationHub.

-   **Version 1.3.3 - October 2020**

    Minor release of the Slack spoke for IntegrationHub

-   **Version 1.2.0 - July 2020**

    Provides actions to automate the management of Channels and Users in Slack.


