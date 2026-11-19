---
title: Declarative actions
description: Learn how the CSM Agent Workspace declarative actions function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-form-declarative-actions.html
release: zurich
topic_type: concept
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Declarative actions

Learn how the CSM Agent Workspace declarative actions function with CSM Configurable Workspace.

Declarative actions add custom functionality to your CSM Agent Workspace forms, fields, lists, and related lists without writing custom scripts or learning APIs. Declarative actions include: form and list actions, related list actions, and field decorators.

If your agents rely on custom declarative actions and you don't migrate them, those buttons, menu items, field decorators, and related list actions don't appear in CSM Configurable Workspace.

<table id="table_lby_n12_jqb"><thead><tr><th>

Legacy table name

</th><th>

UIB table name

</th></tr></thead><tbody><tr><td>

Action Assignment\[sys\_declarative\_action\_assignment\]

</td><td>

Action Assignment \[sys\_declarative\_action\_assignment\]

 UX Add-on Event Mapping \[sys\_ux\_addon\_event\_mapping\]

</td></tr></tbody>
</table>To migrate a declarative action, convert your custom declarative actions to new UXF Client Action type, and then define the corresponding add-on event mapping. For more information, see the following topics:

-   [Customizing your workspace with declarative actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/declarative-actions-landing.md)
-   Create a UXF client action for forms
-   [Declarative actions glossary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/declarative-actions-glossary.md)

## Before you migrate declarative actions

-   Review all custom declarative actions in CSM Agent Workspace.
-   Identify which actions use the UXF Client Action type and which use legacy action types. Only legacy action types need to be converted.

## Convert and map declarative actions

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions**, select the module for the action type, such as **Form Actions**, **List Actions**, or **Related List Actions**, and open the custom declarative action that you want to migrate.
2.  Convert the action to the UXF Client Action type.
3.  Navigate to **All**, enter `sys_ux_addon_event_mapping.LIST`, and press **Enter**.
4.  Select **New**, and create an add-on event mapping record that maps the declarative action to the correct event in CSM Configurable Workspace.
5.  Select **Submit**.
6.  Repeat these steps for each custom declarative action that you need to migrate.

**Related topics**  


[Manage actions in UI Builder pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/work-events.md)

[Bind an event to a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/bind-event-declarative-action.md)

