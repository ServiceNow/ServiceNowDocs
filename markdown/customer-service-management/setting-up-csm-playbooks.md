---
title: Playbooks in Customer Service Management
description: Playbooks provide customer service agents with step-by-step guidance for resolving specific types of cases. Agents can follow a playbook in CSM Configurable Workspace and complete guided activities to resolve customer issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/setting-up-csm-playbooks.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Playbooks in Customer Service Management

Playbooks provide customer service agents with step-by-step guidance for resolving specific types of cases. Agents can follow a playbook in CSM Configurable Workspace and complete guided activities to resolve customer issues.

## Playbook overview

A [playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md) is an end-to-end workflow that includes the stages, steps, and guidance to lead users through a business process. A playbook visualizes a workflow in a task-oriented view and guides users through sequences of tasks.

A playbook takes a workflow and breaks it into multiple stages. Each stage in a playbook includes a logical group of sequential activities for an agent to complete. Stages can also include automated activities, such as sending an email to a customer when a stage or activity is complete.

Playbooks include:

-   A series of steps that a user must complete in order to achieve a particular goal and the necessary guidance for completing those steps.
-   One or more stages, or groups of tasks, and sequences of activities within each stage.

Playbooks are created in the [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio.md) application. Pages that display playbooks in a workspace are created in the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md) application. Agents use playbooks in [CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md) to complete activities. End users can also use playbooks from service portals to create requests and provide information. For more information, see the following sections in this topic:

-   [Playbook users and tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md)
-   [Configuring and configuring playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md)

## Playbook users and tools

The following table describes the different user roles that are involved in the creation, configuration, and use of playbooks. It also describes the tools and applications used by each of those roles.

<table id="table_jd2_s2d_ybc"><thead><tr><th>

User role

</th><th>

Tool / application

</th></tr></thead><tbody><tr><td>

Playbook admin\[playbook.admin\]

</td><td>

Uses the [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio.md) application to author, configure, and monitor playbooks.Workflow Studio is the design environment where playbook owners build playbooks.

</td></tr><tr><td>

Playbook experience admin\[playbook\_experience.admin\]

</td><td>

Uses the [About Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-ui.md) application to create playbook experience records. These records define how playbook activities appear within a playbook.

</td></tr><tr><td>

UI Builder admin\[ui\_builder\_admin\]

</td><td>

Uses the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md) application to create or customize pages that display playbooks in [CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md).UI Builder is a web user interface builder. Users with the UI Builder admin role use the tool to create pages, which are collections of components that make up a workspace user interface.

**Note:** Playbook page templates are available for UI Builder admins to use as a starting point for creating playbook pages.

</td></tr><tr><td>

Customer service agent\[sn\_customerservice\_agent\]

</td><td>

Uses playbooks in CSM Configurable Workspace to complete activities and resolve cases.The playbook runtime experience is where end users, such as agents, follow the playbook to complete a business process.

</td></tr><tr><td>

End user\[sn\_customerservice.customer\]

</td><td>

Uses playbooks create cases, provide requested information, and complete assigned tasks. For more information, see [Playbooks for portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbooks-for-portals.md).

</td></tr></tbody>
</table>## Creating and configuring playbooks

Creating and configuring a playbook involves different tools and applications. Playbooks are created using the Workflow Studio application. Some of the configuration for a playbook is performed in UI Builder as part of the playbook component configuration. Additional settings can be configured in the playbook experience record in the Core UI. These settings include selecting the playbook activity view and configuring playbook stage and activity visibility.

<table id="table_lwt_dbd_ybc"><thead><tr><th>

Tools

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio.md)

</td><td>

Workflow Studio is the design environment where playbook owners \(users with the playbook.admin role\) build playbooks. For more information, see the following topics:-   [Exploring Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/exploring-workflow-studio.md)
-   [Getting started with Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/getting-started-processes.md)

</td></tr><tr><td>

[About Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-ui.md)

</td><td>

Playbook experience records define how playbook activities appear within a playbook.-   Users with the playbook\_experience.admin role can create playbook experience records.
-   Users with the ui\_builder\_admin role can select a playbook experience when adding a playbook to a page in UI Builder.

The playbook experience record includes settings for the playbook stage and activity visibility, such as hiding or displaying playbook activities based on user role or activity state.

</td></tr><tr><td>

[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md)

</td><td>

Users with the ui\_builder\_admin role can use UI Builder to create or customize pages, which are collections of components that make up a workspace user interface. Some of the playbook configuration tasks in UI Builder include:-   **Selecting a playbook activity view**: The activity view determines how the stages and activities are displayed in the playbook. Select a playbook activity view in the playbook component configuration in UI Builder.
-   **Selecting a playbook experience**: The playbook experience determines how the system renders a playbook in a workspace. You can use playbook experiences to customize the look and feel of a playbook, map user actions, and override activities. Select a playbook experience when adding a playbook to a page in UI Builder.
-   **Configuring a playbook to use compact mode**: Compact mode moves the playbook to the contextual side panel. Agents can complete playbook activities in the side panel while viewing other information in the record page. Configure a playbook to use compact mode in the playbook component configuration in UI Builder.

</td></tr></tbody>
</table>## Playbook applications

Several applications are available that enable you to create and use playbooks with Customer Service Management. See [Playbook plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md) for detailed plugin and dependency information.

|Application|Description|
|-----------|-----------|
|Playbooks for Customer Service Management|Use this application to create or customize playbooks based on your individual business needs. Create playbooks that support case types or the base customer service case.|
|[Case Playbook for Onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-onboarding.md)|Use this application to manage the process for taking on new customers or enrolling customers in new products. An onboarding case captures the details of the new customer, including their selection of products and services.|
|[Case Playbook for Complaints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-complaint-overview.md)|Use this application to manage the process for handling customer complaints. A complaint case captures the details of the problem reported by the customer and the expected resolution.|
|[Case Playbook for Product Support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-product-support.md)|Use this application to guide agents through the steps that are needed to resolve product issues. A product support case captures information about the customer, the product, and the reported issue.|

## Playbook plugins

The Playbooks for Customer Service Management plugin \(sn\_csm\_playbook\) is available from the ServiceNow Store. This plugin requires the following plugins:

-   Customer Service \(com.sn\_customerservice\)
-   Dynamic Related Records \(com.snc.uib.sn\_dyn\_rel\_rec\)
-   Playbook Experience \(com.playbook\_experience\)

The following playbook applications are available for use with Customer Service Management and are available from the ServiceNow Store:

-   Case Playbook for Onboarding
-   Case Playbook for Complaints
-   Case Playbook for Product Support

These playbooks require the following plugins:

-   Playbooks for Customer Service Management \(com.sn\_csm\_playbook\)
-   Customer Service Case Types \(com.snc.csm\_case\_types\)

## Using playbooks

Customer service agents can use the guidance available with playbooks to complete the tasks and activities that are needed to resolve specific types of cases.

A playbook includes multiple stages and each stage includes one or more activities for an agent to complete. When using a playbook, agents can:

-   View the stages and activities.
-   Select an activity and perform the work necessary to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities necessary to resolve the case.

Several features are available to agents when using a playbook, depending on the playbook configuration.

| | |
|---|---|
||If a playbook is configured to use the record generator feature, customer service agents can create a record using a playbook activity.|
|[Filter playbook activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-filter-activities.md)|Filter the activities in playbook stages by the selected user or activity state.|
||Customer service agents can access the activity stream in the contextual side panel to communicate with requesters and make internal notes about the work done on a record.|
||Customer service agents can view dynamic related records that dynamically change based on the context of the current record or playbook activity.|
||Customer service agents can view ribbon information in the contextual side panel, including the case overview and timeline, Customer 360, and SLAs.|
|[Add an optional activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/using-customized-playbook-experience-for-customer-service-management.md)|Add optional activities to different stages in a playbook as needed. For example, a customer may want to schedule an appointment to visit a location.|
||Use the ServiceNow Otto for CSM case summarization skill to summarize the case details and display this information on the case record.|

## Configuring Playbooks

Some of the configuration for a playbook is performed in UI Builder as part of the playbook component configuration. Additional settings can be configured in the playbook experience configuration record. These settings include selecting the playbook activity view and configuring playbook stage and activity visibility.

<table id="table_bhd_hgd_1cc"><thead><tr><th>

Configuration task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create or customize a playbook record page

</td><td>

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. The following playbook record pages are available with the Playbooks for Customer Service Management application \[com.sn\_csm\_playbook\]:-   Case playbook: horizontal stages page
-   Case playbook: vertical stages page

For more information, see [Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/work-pages.md).

</td></tr><tr><td>

Configure the playbook record page settings

</td><td>

Each UI Builder record page includes the following settings:-   **Active**: Enabling this check box makes the page available to the selected audience.
-   **Order**: This value indicates the page priority. The page with the lowest order value is the default page.
-   **Conditions**: Determine when a page variant is displayed.
-   **Audience**: Determines who can see the page.

For more information, see the following topics:

-   Case playbook: horizontal stages page variant settings
-   Case playbook: vertical stages page variant settings

</td></tr><tr><td>

[Select a playbook activity view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-select-activity-view.md)

</td><td>

The activity view determines how the stages and activities are displayed in the playbook. -   **Stacked**: &lt;add description&gt;
-   **Focused**: &lt;add description&gt;

Users with the system administrator role can select a playbook activity view in the playbook component configuration in UI Builder.

</td></tr><tr><td>

[Configure playbook stage and activity visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-config-activity-visibility.md)

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

Set up a record generator for a case type

</td><td>

Create a record for a case type by using a playbook record generator. With a record generator, the system creates a record as the first step in the playbook.

</td></tr><tr><td>

[Configure an optional activity for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-optional-activity-for-a-case-type-playbook.md)

</td><td>

Configure optional playbook activities so that agents and fulfillers can insert activities during a playbook run. For example, a customer may want to schedule an optional activity such as making an appointment to visit a location.

</td></tr></tbody>
</table>## Playbook experiences

Playbook experiences are used to customize the look and feel of a playbook. Settings in a playbook experience control how [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md) renders a playbook in the CSM workspaces. System administrators can configure settings in the playbook experience record that determine the playbook stage and activity visibility.

Within UI Builder, system administrators can configure playbook component settings such as:

-   Selecting a playbook experience
-   Selecting an activity view
-   Enabling compact mode

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

**Related topics**  


[Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-ui.md)

