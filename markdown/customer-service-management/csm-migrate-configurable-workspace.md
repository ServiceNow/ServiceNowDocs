---
title: Migrate to CSM Configurable Workspace
description: Follow the instructions in this topic to migrate from CSM Agent Workspace to CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/csm-migrate-configurable-workspace.html
release: australia
topic_type: concept
last_updated: "2026-11-13"
reading_time_minutes: 5
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate to CSM Configurable Workspace

Follow the instructions in this topic to migrate from CSM Agent Workspace to CSM Configurable Workspace.

If you are currently using CSM Agent Workspace and want to migrate to CSM Configurable Workspace, you can continue using most of your existing configurations. Some features, however, need to be configured specifically for CSM Configurable Workspace. You can migrate some of the configurations using lists and forms and others using the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md) tool.

<table id="table_rrk_p52_v4b"><thead><tr><th>

Workspace configurations

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Configurations that work in both CSM Agent Workspace and CSM Configurable Workspace without modification.

</td><td>

-   Ribbons
-   Forms

</td></tr><tr><td>

Configurations that are different for CSM Configurable Workspace.

</td><td>

-   Lists
-   List categories

</td></tr></tbody>
</table>Also, be aware that some configuration changes made for one workspace can also affect the other. For example, changes to the CSM Agent Workspace configuration may impact CSM Configurable Workspace. The same applies to changes to the CSM Configurable Workspace configuration, which may impact CSM Agent Workspace.

**Note:** For customers who are **not** currently using CSM Agent Workspace and want to implement CSM Configurable Workspace, use the Configurable Workspace guided setup by navigating to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Configurable Workspace Guided Setup** and select **Get Started**. The guided setup lists configuration categories, such as Branding &amp; Theming, Tab Settings, Lists, and Forms. Select **Get Started** in each category and complete its tasks to set up a new implementation of CSM Configurable Workspace.

## Workspace features

This section provides information, parameters, and steps to complete the migration of CSM Agent Workspace configurations to CSM Configurable Workspace. Select the feature that you want to migrate from the following list.

The features are listed in the order that most administrators migrate them. Start with the configurations that share tables with CSM Agent Workspace, and finish with the ones that must be rebuilt or verified end to end. To see the action required for each configuration, see [Plan the CSM Agent Workspace migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-plan.md).

|Feature|Description|
|-------|-----------|
|[Form headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-headers.md)|Form headers provide an overview of the record.|
|[Ribbons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-ribbons.md)|Ribbons help agents quickly scan relevant information about a record, such as a timeline, a user, or a customer summary.|
|[Highlights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-highlights.md)|Highlights provide background color that visually expresses the status of a highlighted value.|
|[UI Action Bar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-ui-actions.md)|UI actions include custom buttons, menu items, and limiting access to forms based on user role.|
|[Migrate chrome header settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-chrome-header.md)|Chrome header settings control search, notifications, and user preference controls in the workspace header.|
|[Migrate the New Record menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-new-record-menu.md)|The New Record menu lets agents create cases, interactions, and other records without leaving the workspace.|
|[Migrate landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-landing-pages.md)|The landing page is the first page agents see when they open the workspace.|
|[Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-lists.md)|The list view displays filtered lists of records, such as All tasks, Open tasks, and My tasks.|
|[Migrate the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-layout.md)|The form layout controls which fields, sections, and related lists agents see when they open a record.|
|[Migrate the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-contextual-side-panel.md)|The contextual side panel gives agents access to tools and information without leaving the record page.|
|[Configure Lookup and Verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-lookup-and-verify.md)|Lookup and Verify helps agents identify and authenticate a caller at the start of an interaction.|
|[Migrate client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-client-scripts.md)|Client scripts control how fields behave on forms.|
|[Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-activity-stream.md)|Activity Stream enables agents to communicate with requesters and make internal notes about the work done on a record.|
|[Declarative actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-declarative-actions.md)|Declarative actions add custom functionality to your Workspace forms, fields, lists, and related lists without writing custom scripts or learning APIs.|
|[Agent assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-agent-assist.md)|Agent assist provides agents with automatic search results that show possible solutions for records they open.|
|[Agent Chat for CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-agent-chat.md)|Agent Chat enables agents to interact with customers, create incident or case records, or transfer chats to another agent or queue.|
|[Global Search in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-search-config.md)|Global Search provides users with the ability to search for information within the defined search sources.|
|[Email Composer and Email Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-compose-preview-email.md)|The Email Composer enables requestors and fulfillers to use email to communicate.|
|[Configure response templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-response-templates.md)|Response templates let agents insert standard replies into email and chat responses.|
|[Customer Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-custom-central.md)|Customer Central displays all the touch points that a customer has had with a contact center in the form of information cards.|
|[Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-forms.md)|The form is the user interface where agents do most of their work.|
|[Branding and theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-branding-theming.md)|Branding and theming enables you to customize CSM Configurable Workspace to your company branding and theming.|

