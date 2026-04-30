---
title: CSM Configurable Workspace form headers
description: Form headers in CSM Configurable Workspace provide a quick glance of case, account, or contact information.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# CSM Configurable Workspace form headers

Form headers in CSM Configurable Workspace provide a quick glance of case, account, or contact information.

Form headers include a primary value and several secondary values. You can configure the information included in the form header for the Case, Account, and Contact forms.

<table id="table_csm_form_headers"><thead><tr><th>

Form

</th><th>

Primary Value

</th><th>

Secondary Values

</th></tr></thead><tbody><tr><td>

Case

</td><td>

Short description

</td><td>

-   Account and contact \(B2B\)
-   Consumer \(B2C\)
-   Priority
-   State

</td></tr><tr><td>

Account

</td><td>

Account

</td><td>

Primary contact

</td></tr><tr><td>

Contact

</td><td>

Contact

</td><td>

Account

</td></tr></tbody>
</table>## Displaying form header secondary values

You can configure the form header to display secondary values either below the primary value or in the Contextual side panel. The **record\_secondary\_values\_location** property controls this setting.

![Case form header that shows secondary values for case Account, Contact, Priority, and State under the Short description primary value.](../../../product/customer-service-management/image/csm-config-workspace-case-form-header.png "Case form header secondary values displayed below the primary value")

![Case form header that shows secondary values for case Account, Contact, Priority, and State in the Contextual side panel.](../../../product/customer-service-management/image/csm-config-workspace-case-form-header-sidebar.png "Case form header secondary values displayed in the Contextual side panel")

See the following topics for more information about configuring form headers in CSM Configurable Workspace:

-   [Set up a form header in CSM Configurable Workspace](../../../product/customer-service-management/task/config-csm-config-ws-form-header.md)
-   [Display the form ribbon and form header secondary values in the Contextual side panel](../../../product/customer-service-management/task/config-csm-display-header-in-sidebar.md)

**Note:** One form header configuration, **CSM/FSM Configurable Workspace Header Config**, is included with CSM Configurable Workspace.

## Form header components

For CSM Configurable Workspace, the form header is made up of individual components that can be configured with [UI Builder](https://www.servicenow.com/docs/access?context=using-ui-builder&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Individual components provide customers with flexible and granular configuration options. Customers can control the placement, size and spacing of these components, giving them the ability to show additional information that agents may need.

The Data Value Block component is used to display secondary values in the form header and the Contextual side panel. .

