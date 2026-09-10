---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.The ServiceNow Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.The ServiceNow Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Service Operations Workspace, ITSM, Australia release, Service Operations Workspace, ITSM, Australia release, Service Operations Workspace, ITSM, Australia release]
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.

## About Service Operations Workspace for ITSM

-   Redirect UI16 module navigation links to the equivalent SOW experience.
-   Access SOW configuration and property pages of various SOW applications using granular admin roles.
-   Improve the focus on relevant contextual information by hiding the contextual side panel for a specific table and tab combination.
-   Configure reference field auto-load behavior from the SOW Admin Center.
-   Enable service desk agents to create, manage, and track checklists for Request and RITM records directly within the workspace to confirm that all steps are completed.
-   Starting in version 9.2, you can do the following:
    -   Perform various actions on the post incident report \(PIR\) if you have the incident\_write role and added as co-contributor to the PIR.
    -   Investigate and resolve incidents by using the AI incident summary and resolution plan suggestion in the **Overview** tab of an incident record.

See [Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/sow-landing-page.md) for more information.

## Activation and other requirements

**Important:** Service Operations Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Service Operations Workspace for ITSM is active by default and its default version is `9.0` in Australia. When you upgrade from any previous release to Australia from the ServiceNow Store, Service Operations Workspace for ITSM `9.0` is automatically installed.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-service-management-rn-landing.md)

## June 2026

The ServiceNow® Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.

### What's new

-   **[Review AI incident summary and suggestions in the incident record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/view-update-inc-overview-tab.md)**

    Investigate and resolve incidents efficiently by reviewing the AI-generated incident summary and suggested resolution plan in the AI summary and suggestions card on the **Overview** tab of an incident record. If the **Overview** tab is hidden for L1 service desk agents, the card appears on the **Details** tab.


### What's changed

-   **[Generate, update and publish PIR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/review-update-pir-mim-sow.md)**

    Perform the following actions on the PIR if you have the incident\_write role and added as co-contributor to the PIR:

    -   Update the state or publish the PIR.
    -   Refresh the Incident Summary data on the PIR.
    -   Create PIR custom event.
    -   Search, add, edit and save co-contributors \(Users\) for PIR.

## Australia

The ServiceNow® Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. Service Operations Workspace for IT Service Management was enhanced and updated in the Australia release.

### What's new

-   **[UI16 links to SOW redirection behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/manage-admin-console-sow-itsm.md)**

    Redirect UI16 module links such as forms and lists to the equivalent SOW experience. The UI16 module link redirection behavior is supported for all the applications in SOW when the system property **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** is set to `true`.

    For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center. You can enable this feature for the UI16 links and user groups or specifically for a custom table. You can also enable this feature for specific user groups or all user groups within the custom table or applications in SOW.

-   **[Mapping granular admin roles with SOW granular roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/roles-in-sow.md)**

    Using granular admin roles, provide full administrative access to the configuration and property pages for the applications in SOW without requiring the administrator \(admin\) role. These granular admin roles are mapped with ACLs and contain the corresponding existing SOW granular roles.

-   **[UX property to hide contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/manage-admin-console-sow-itsm.md)**

    Use the Hide contextual side panel for specific table and tab combination option from the SOW Properties section in the SOW Admin Center to configure the hide **ContextualSidebar** UX page property. This property enables you to define the table with tab combination for which the default primary contextual side panel must be hidden, prioritizing the embedded contextual side panel within the tab instead.


### What's changed

-   **[Configure reference field auto-load behavior from SOW Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/admin-center-sow.md)**

    Use the Reference field auto-load behavior option from the SOW Properties section of the SOW Admin Center to configure the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property. The option enables you to configure the automatic searching of field value results displayed for reference fields such as Configuration item, Service offering, and Service.

-   **[Recent list links in SOW record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/view-inc-record-info-contextual-sidepanel.md)**

    Select the Recent incidents, Recent interaction, or Recent tasks links from the Record information side panel of a SOW record displays the 10 most recent records irrespective of their timeline instead of showing the records from last seven days. You can select the **View All** option to view additional records as well.


