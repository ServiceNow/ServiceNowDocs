---
title: Configure Playbooks for Customer Service Management
description: Configure different playbook settings, such as selecting the activity view and determining activity visibility.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure Playbooks for Customer Service Management

Configure different playbook settings, such as selecting the activity view and determining activity visibility.

Some of the configuration for a playbook is performed in UI Builder as part of the playbook component configuration. Additional settings can be configured in the playbook experience configuration record. These settings include selecting the playbook activity view and configuring playbook stage and activity visibility.

<table id="table_bhd_hgd_1cc"><thead><tr><th>

Configuration task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create or customize a playbook record page

</td><td>

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. The following playbook record pages are available with the Playbooks for Customer Service Management application \[com.sn\_csm\_playbook\]:-   [Case playbook: horizontal stages page](csm-playbook-horizontal-stages.md)
-   [Case playbook: vertical stages page](csm-playbook-vertical-stages.md)

For more information, see [Manage UI Builder pages and page variants](https://www.servicenow.com/docs/access?context=work-pages&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Configure the playbook record page settings

</td><td>

Each UI Builder record page includes the following settings:-   **Active**: Enabling this check box makes the page available to the selected audience.
-   **Order**: This value indicates the page priority. The page with the lowest order value is the default page.
-   **Conditions**: Determine when a page variant is displayed.
-   **Audience**: Determines who can see the page.

For more information, see the following topics:

-   [Case playbook: horizontal stages page variant settings](csm-playbook-horizontal-stages.md#table_f5m_bhx_qbc)
-   [Case playbook: vertical stages page variant settings](csm-playbook-vertical-stages.md#table_f5m_bhx_qbc)

</td></tr><tr><td>

[Select a playbook activity view](../task/playbook-select-activity-view.md)

</td><td>

The activity view determines how the stages and activities are displayed in the playbook. -   **Stacked**: &lt;add description&gt;
-   **Focused**: &lt;add description&gt;

Users with the system administrator role can select a playbook activity view in the playbook component configuration in UI Builder.

</td></tr><tr><td>

[Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md)

</td><td>

The following fields control the visibility of playbook stages and activities.

-   **Hide Inaccessible Activity**: Accessibility is determined by user permissions. When enabled, the user cannot see an activity if they do not have permissions to view the data associated with the activity. If all activities in a stage are inaccessible to the user, the stage is also hidden.
-   **Control Activity Display**: Pending activities are those activities that have not yet been triggered. Select one of the options in this field to show or hide pending activities.

 Users with the system administrator role can in the playbook experience configuration record.

</td></tr><tr><td>

Configure a playbook to use compact mode

</td><td>

Compact mode moves the playbook from a tab in the Workspace to the contextual side panel. Agents can complete playbook activities in the side panel while viewing other tabs in the record page.Users with the system administrator role can configure a playbook to use compact mode in the playbook component configuration in UI Builder.

</td></tr><tr><td>

Preview a playbook

</td><td>

Users with the playbook experience admin role \[playbook\_experience.admin\] can preview a playbook in real time within a non-production environment. With this feature, playbook experience administrators can easily see and test different playbook settings.

</td></tr><tr><td>

Select a playbook experience

</td><td>

A playbook experience is a defined set of configurations that determines how the system renders a playbook in Workspace. You can use playbook experiences to customize the look and feel of a playbook, map user actions, and override activities.The Playbook Experience plugin \(com.playbook\_experience\) includes the Global Playbook Experience record, which defines a default playbook configuration.

The Playbooks for Customer Service Management plugin \(com.sn\_csm\_playbook\) includes the following additional playbook experience records:

-   CSM Configurable Workspace Playbook
-   CSM Agent Workspace Playbook

Users with the system administrator role can select a playbook experience when adding a playbook to a page in UI Builder.

Different playbooks for the same record type can use different playbook experiences. For example, if a complaint case uses two playbooks, each playbook can use a different playbook experience.

</td></tr><tr><td>

[Set up a record generator for a case type](../task/setup-record-generator-for-case-type.md)

</td><td>

Create a record for a case type by using a playbook record generator. With a record generator, the system creates a record as the first step in the playbook.

</td></tr><tr><td>

[Configure an optional activity for a playbook](../task/configure-optional-activity-for-a-case-type-playbook.md)

</td><td>

Configure optional playbook activities so that agents and fulfillers can insert activities during a playbook run. For example, a customer may want to schedule an optional activity such as making an appointment to visit a location.

</td></tr></tbody>
</table>## Playbook experiences

Playbook experiences are used to customize the look and feel of a playbook. Settings in a playbook experience control how [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US) renders a playbook in the CSM workspaces. System administrators can configure settings in the playbook experience record that determine the playbook stage and activity visibility.

Within UI Builder, system administrators can configure playbook component settings such as:

-   Selecting a playbook experience
-   Selecting an activity view
-   Enabling compact mode

For more information, see [Configuring playbooks for Customer Service Management](csm-playbooks-configuring.md).

