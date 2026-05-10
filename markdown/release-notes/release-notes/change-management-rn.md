---
title: Change Management release notes
description: The ServiceNow Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. Change Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Change Management release notes

The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. Change Management was enhanced and updated in the Australia release.

## Change Management highlights for the Australia release

-   Configure the properties in Change Management application using the sn\_change\_admin role.
-   Manage conflict detection for change request using the new **Exclude from conflict detection** option.
-   Configure change templates with a specific change model.
-   Use change templates to manage the change request creation process.

See [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_ITILChangeManagement.md) for more information.

## New in the Australia release

-   **[Granular admin role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/installed-with-cm-itsm-roles.md)**

    Assign the single feature-specific granular sn\_change\_admin role to users to grant permission to configure Change Management features and system properties. This role replaces the previous general admin and ITIL roles. The sn\_change\_admin role includes the sn\_change\_writer, change\_manager, and sn\_change\_cab.cab\_manager roles.

-   **[Exclude change request records from conflict check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-conflict-properties.md)**

    Exclude change requests from the conflict check process by setting the **Exclude from conflict detection** field to true. This setting also means that the change record is not displayed as a conflicting change when conflict checker is run on other change records.

-   **[Create change templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/create-change-template.md)**

    Control mandatory and read-only fields for change models by configuring change templates and defining template field policies. Change templates provide baseline standardization for common changes, making changes easier to create as well as driving a higher standard of change and compliance. Similar to the concepts used for existing standard change templates, templates used for change models can be proposed, reviewed, versioned, or retired.

-   **[Enhanced data model for change templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-data-model.md)**

    Use the enhanced data model that supports better categorization and role-based access for change templates for all change models automatically. This feature is optional for newly created standard changes.

    This data model does not impact the existing standard change catalog and migration of these standard changes is not required.


## Activation information

Change Management is a ServiceNow AI Platform feature that is active by default. The Change Management plugins listed are activated by default.

## Plugin information

-   **Change Management plugins**

    The following plugins are new in Australia:

    -   Change Management-Flows \(com.snc.service.change\_management.flows\): Implements the Change-Refresh Impacted Services flow to manage the Refresh Impacted Services process instead of relying on the Progress Worker table.
    -   ITSM Dynamic CI Flows \(com.snc.service.dynamic\_ci\_flows\): Implements flow \(IPC- Dynamic CI Group\) to manage the Sync Affected CI Dynamic Group process instead of relying on the Progress Worker table.
    -   Provides flows for State Transition Models \(com.snc.itsm.state\_transition\_model.flows\): Provides flows that manage the publishing and retirement life cycles of the State Transition templates.

## Accessibility information

-   **Reflow for Create a change request page**

    The Create a change request page now supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

