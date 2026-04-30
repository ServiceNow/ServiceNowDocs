---
title: Migrate to CSM Configurable Workspace
description: Follow the instructions in this topic to migrate from CSM Agent Workspace to CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Migrating to Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Migrate to CSM Configurable Workspace

Follow the instructions in this topic to migrate from CSM Agent Workspace to CSM Configurable Workspace.

If you are currently using CSM Agent Workspace and want to migrate to CSM Configurable Workspace, you can continue using most of your existing configurations. Some features, however, need to be configured specifically for CSM Configurable Workspace. You can migrate some of the configurations using lists and forms and others using the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) tool.

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

**Note:** For customers who are **not** currently using CSM Agent Workspace and want to implement CSM Configurable Workspace:

-   Use the CSM Configurable Workspace guided setup by navigating to **Customer Service** &gt; **Administration** &gt; **Guided Setup** &gt; **CSM Configurable Workspace**. Clicking **Configure** in this category takes you to the Configurable Workspace guided setup. The information and instructions in the different guided setup categories can help you set up a new implementation of CSM Configurable Workspace.
-   For additional information, see Setting up Workspace.

## Workspace features

This section provides information, parameters, and steps to complete the migration of CSM Agent Workspace configurations to CSM Configurable Workspace. Select the feature that you want to migrate from the following list.

|Feature|Description|
|-------|-----------|
|[Activity stream](migration-activity-stream.md)|Activity Stream enables agents to communicate with requesters and make internal notes about the work done on a record.|
|[Agent assist](migration-agent-assist.md)|Agent assist provides agents with automatic search results that show possible solutions for records they open.|
|[Agent Chat for Customer Service Management Configurable Workspace](migration-agent-chat.md)|Agent Chat enables agents to interact with customers, create incident or case records, or transfer chats to another agent or queue.|
|[Branding and theming](migration-branding-theming.md)|Branding and theming enables you to customize your Configurable Workspace to your company branding and theming.|
|[Email Composer and Email Viewer](migration-compose-preview-email.md)|The Email Composer enables requestors and fulfillers to use email to communicate.|
|[Customer Central](migration-custom-central.md)|Customer Central displays all the touch points that a customer has had with a contact center in the form of information cards.|
|[Declarative actions](migration-form-declarative-actions.md)|Declarative actions add custom functionality to your Workspace forms, fields, lists, and related lists without writing custom scripts or learning APIs.|
|[Forms](migration-forms.md)|The form is the user interface where agents do most of their work.|
|[Form headers](migration-form-headers.md)|Form headers provide an overview of the record.|
|[Global Search in configurable workspaces](migration-search-config.md)|Global Search provides users with the ability to search for information within the defined search sources.|
|[Highlights](migration-form-highlights.md)|Highlights provide background color that visually expresses the status of a highlighted value.|
|[Lists](migration-lists.md)|The list view displays filtered lists of records, such as All tasks, Open tasks, and My tasks.|
|[Ribbons](migration-form-ribbons.md)|Ribbons help agents quickly scan relevant information about a record, such as a timeline, a user, or a customer summary.|
|[UI Action Bar](migration-form-ui-actions.md)|UI actions include custom buttons, menu items, and limiting access to forms based on user role.|

