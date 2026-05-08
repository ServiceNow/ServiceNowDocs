---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.

## ServiceNow® highlights for the Australia release

-   Redirect UI16 module navigation links to the equivalent SOW experience.
-   Access SOW configuration and property pages of various SOW applications using granular admin roles.
-   Improve the focus on relevant contextual information by hiding the contextual side panel for a specific table and tab combination.
-   Configure reference field auto-load behavior from the SOW Admin Center.
-   Enable service desk agents to easily create, manage, and track checklists for Request and RITM records directly within the workspace to confirm that all steps are completed.

See Service Operations Workspace for ITSM for more information.

**Important:** Service Operations Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **UI16 links to SOW redirection behavior**

    Improve the fulfiller experience by redirecting UI16 module links such as forms and lists to the equivalent SOW experience. The UI16 module link redirection behavior is supported for all the applications in SOW when the system property **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** is set to `true`.

    For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center. You can enable this feature for the UI16 links and user groups or specifically for a custom table. You can also enable this feature for specific user groups or all user groups within the custom table or applications in SOW.

-   **Mapping granular admin roles with SOW granular roles**

    Using granular admin roles, provide full administrative access to the configuration and property pages for the applications in SOW without requiring the administrator \(admin\) role. These granular admin roles are mapped with ACLs and contain the corresponding existing SOW granular roles.

-   **UX property to hide contextual side panel**

    Use the Hide contextual side panel for specific table and tab combination option from the SOW Properties section in the SOW Admin Center to configure the hide **ContextualSidebar** UX page property. This property enables you to define the table with tab combination for which the default primary contextual side panel must be hidden, prioritizing the embedded contextual side panel within the tab instead.


## Changed in this release

-   **Configure reference field auto-load behavior from SOW Admin Center**

    Use the Reference field auto-load behavior option from the SOW Properties section of the SOW Admin Center to configure the **Reference search on click ** \(**ref\_search\_on\_click**\) UX page property. The option enables you to configure the automatic searching of field value results displayed for reference fields such as Configuration item, Service offering, and Service.

-   **Recent list links in SOW record**

    Selecting the Recent incidents, Recent interaction, or Recent tasks links from the Record information side panel of a SOW record displays the 10 most recent records irrespective of their timeline instead of showing the records from last seven days. You can select the **View All** option to view additional records as well.


## Activation information

Service Operations Workspace for ITSM is active by default and its default version is 9.0 in Australia. When you upgrade from any previous release to Australia from the ServiceNow Store, Service Operations Workspace for ITSM 9.0 is automatically installed.

## Related ServiceNow applications and Features

-   **Change Management**

    Control the life cycle of a change and implement the change with minimum disruption to IT services.

-   **Incident Management**

    Enable users to identify IT issues and log incidents through the Incident Management system. Efficiently track, classify, and prioritize incidents to work effectively toward their resolution.

-   **Interaction Management**

    Respond to an incoming chat, phone, walk-up, or messaging interaction quickly by using an interaction that provides a centralized location for all communication channels.

-   **Notify**

    Provide support for SMS and voice channels on the platform to communicate with your team and customers.

-   **On-Call Scheduling**

    Identify available on-call members of a support group who can be contacted to resolve an issue.

-   **Password Reset**

    The ServiceNow® Password Reset application enforces strong and secure passwords by enabling end users to reset or change their passwords either by using the self-service process or by requesting the assistance of a service desk agent.

-   **Predictive Intelligence**

    Use machine-learning algorithms to provide dynamic and contextual recommendations for resolving an incident.

-   **Problem Management**

    Identify the root cause of recurring incidents or a major incident to help prevent them from happening again.

-   **Recommended Actions for ITSM in Service Operations Workspace**

    Get field recommendations and guidance in the side panel for the incident form in Service Operations Workspace.

-   **Request Management**

    Initiate a catalog request flow from a different IT Service Management flow, such as an incident flow, by using catalog requests.

-   **Service Level Management**

    Access incident service level agreement \(SLA\) information on the Service Operations Workspace for ITSM landing page and incident record page.

-   **Service Operations Workspace for ITOM**

    Configure your operator experience through a unified interface for multiple ServiceNow® IT Operations Management workflows.

-   **Walk-up Experience**

    Manage walk-up interactions and queues effortlessly by using Service Operations Workspace for ITSM.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

