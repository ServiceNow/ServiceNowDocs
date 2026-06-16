---
title: Field Service Virtual Agent Conversations release notes
description: Version history for the Field Service Management Field Service Virtual Agent Conversations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-field-service-va-conversations.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Field Service Management release notes, ServiceNow Store release notes]
---

# Field Service Virtual Agent Conversations release notes

Version history for the Field Service Management Field Service Virtual Agent Conversations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.0 - August 2025**
    -   New:
        -   Virtual agent improvements for Task Dependencies
            -   We have updated the Virtual Agent conversational flows for both "Upcoming Tasks" and "Nearby Tasks" to better handle task dependencies. When an agent attempts to start work or start travel on a task with dependency conflicts, the VA will now inform the agent about the dependency and offer options to either start the task anyway, navigate to the previous dependent task, or cancel the action. This mirrors the platform behavior for a consistent experience.
            -   Setting dependency for nearby tasks: Nearby Task visibility and override behavior are controlled by the AllowOverridesWhenDependencyConflictsFound setting. If this setting is enabled, tasks will be shown even if there are dependency conflicts, and agents can choose to override the conflicts during the conversation. If the setting is disabled, tasks with unresolved dependency conflicts will not be displayed in the list. In both cases, when starting a task with conflicts, agents will be guided through the updated conversational flow.
    -   Changed: Previously, the distance unit and maximum travel radius for an agent were fetched from the Work Parameters table. Now, they are fetched from the Resource Schedule Attributes table. Customers should configure these attributes in the new table going forward to get the nearby tasks for agent.
-   **Version 1.6.0 - August 2024**

    Changed: Replaced the existing API to get SM Config properties with newer version which allows Field Service application to have multiple SM Configs.

-   **Version 1.5.0 - August 2023**
    -   New
        -   Dark theme uptake
-   **Version 1.4.0 - February 2023**
    -   Changed:
        -   Code refactoring due to work management plugin dependency changes
        -   Updated Near by tasks topic to handle the situation when agent and task is at same location and work parameter information is not specified for agent
-   **Version 1.3.0 - July 2021**
    -   New:
        -   Consider field service agent work parameters 'maximum travel radius' to show near by tasks
        -   Display crew tasks along with individual tasks in Upcoming tasks topic
-   **Version 1.2.2 - February 2021**

    Fixed: minor bug fixes

-   **Version 1.2.1 - December 2020**

    Fixed: Provided patch to fix insecure user reference check

-   **Version 1.2.0 - November 2020**

    New: The topic 'Debrief tasks' is created to allow field service agents to report time worked and incidentals

-   **Version 1.0.0 - October 2020**

    Get instant access to frequently performed activities with Field Service Virtual Agent Conversations - an automated, conversational chatbot that understands natural human language. The Field Service Virtual Agent Conversations application provides field service workers the capability to act upon upcoming tasks and pick nearby tasks.


