---
title: UI Policy API - ServiceNow Fluent
description: The UI Policy API defines user interface \(UI\) policies \[sys\_ui\_policy\] that dynamically change the behavior of information on a form and control custom process flows for tasks.Create a UI policy sys\_ui\_policy to configure form behavior.Configure the actions \[sys\_ui\_policy\_action\] that the UI policy performs on fields.Configure the visibility of related lists \[sys\_ui\_policy\_rl\_action\] on a form for a UI policy.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# UI Policy API - ServiceNow Fluent

The UI Policy API defines user interface \(UI\) policies \[sys\_ui\_policy\] that dynamically change the behavior of information on a form and control custom process flows for tasks.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

UI Policies can make fields mandatory, read-only, visible, hidden, or cleared when certain conditions are met. You can also use client scripts to perform all of these actions, but for faster load times use UI policies when possible.

For general information about UI policies, see [Using UI policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAUIPolicy.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## UiPolicy object

Create a UI policy sys\_ui\_policy to configure form behavior.

<table id="table_esc_lnn_rhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

table

</td><td>

String

</td><td>

Required. The table of the form to modify.

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

Required. A description of the policy and its purpose.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the policy is applied to the form.Default: true

</td></tr><tr><td>

global

</td><td>

Boolean

</td><td>

Flag that indicates whether to which form views the policy applies. If true, the policy applies to all views of the table. If false, the policy is specific to the form view specified with the view property.

 Default: true

</td></tr><tr><td>

onLoad

</td><td>

Boolean

</td><td>

Flag that indicates when the policy executes. If true, the policy runs every time a form is loaded if the conditions are satisfied.Default: true

</td></tr><tr><td>

reverseIfFalse

</td><td>

Boolean

</td><td>

Flag that indicates whether to invert the policy behavior when the condition evaluates to false. If true, the policy action is undone when the conditions of its policy evaluate to false.Default: true

</td></tr><tr><td>

inherit

</td><td>

Boolean

</td><td>

Flag that indicates whether tables that extend the current table inherit the policy. If true, extended tables inherit the policy.When a child table has an inherited policy from its parent table, the policy on the child table runs first. This event is true regardless of the order of the policies.

 Default: false

</td></tr><tr><td>

isolateScript

</td><td>

Boolean

</td><td>

Flag that indicates whether to run scripts in isolated scope. If true, the script runs in isolated scope. This property only applies if the runScripts is set to true.Default: false

</td></tr><tr><td>

conditions

</td><td>

String

</td><td>

A filter query that specifies the fields and values that must be true for users to access the object. For more information, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md). To set conditions using a script, use a client script instead.Conditions are only rechecked if a user manually changes a field on a form. If the change is made by a UI action, context menu action, or through the list editor, it isn’t evaluated.

</td></tr><tr><td>

runScripts

</td><td>

Boolean

</td><td>

Flag that indicates whether advanced behavior can be scripted for both true and false conditions. If true, scripts defined with the scriptTrue, scriptFalse, uiType, and isolateScript properties run when applicable. Default: false

</td></tr><tr><td>

scriptTrue

</td><td>

String

</td><td>

Client-side script that runs if the conditions of the policy are met. This property is required if the runScripts property is set to true.Format: `function onCondition() {}`

Default: `function onCondition() {\n\n}`

</td></tr><tr><td>

scriptFalse

</td><td>

String

</td><td>

Client-side script that runs if the conditions of the policy aren’t met and the reverseIfFalse property is set to true. This property is required if the runScripts property is set to true.Format: `function onCondition() {}`

Default: `function onCondition() {\n\n}`

</td></tr><tr><td>

uiType

</td><td>

String

</td><td>

The type of user interface to which the policy applies. This property is required if the runScripts property is set to true.Valid values:

-   desktop: The policy applies to desktop interfaces.
-   mobile-or-service-portal: The policy applies to mobile and Service Portal interfaces.
-   all: The policy applies to all interfaces.

Default: desktop

</td></tr><tr><td>

actions

</td><td>

Array

</td><td>

A list of field actions to apply if the conditions are met. For more information, see [actions array](fluent-ui-policy-api.md#).

</td></tr><tr><td>

relatedListActions

</td><td>

Array

</td><td>

A list of visibility controls for related lists. For more information, see [relatedListActions array](fluent-ui-policy-api.md#).

</td></tr><tr><td>

description

</td><td>

String

</td><td>

Additional information about the policy.

</td></tr><tr><td>

modelId

</td><td>

String

</td><td>

The sys\_id of the parent UI policy to which the policy applies when this policy is inherited. This property works in conjunction with model\_table property.

</td></tr><tr><td>

modelTable

</td><td>

String

</td><td>

The name of the parent table to which the policy applies when a UI policy is inherited from a parent table. This property works in conjunction with the model\_id property.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The execution order in which to apply policies if more than one policy fits the conditions.For inherited UI policies, the extended table's policies are executed first. Then the base table policies are executed.

Default: 100

</td></tr><tr><td>

setValues

</td><td>

String

</td><td>

\(Deprecated\) The field values to set using an encoded string format. Use UI policy actions \[sys\_ui\_policy\_action\] instead.

</td></tr><tr><td>

view

</td><td>

Reference or String

</td><td>

Required. The variable identifier or name of the UI view \[sys\_ui\_view\] which applies, or the default view. To define a UI view, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).To use the default view \(`default_view`\), you must import it:

```javascript
import { default_view } from '@servicenow/sdk/core'
```

</td></tr></tbody>
</table>```javascript
import { UiPolicy } from '@servicenow/sdk/core';

export const securityIncidentPolicy = UiPolicy({
  $id: Now.ID['security_incident_policy'],
  table: 'incident',
  shortDescription: 'Lock critical fields for security incidents',
  active: true,
  onLoad: true,
  conditions: 'category="security"',
  actions: [
    {
      field: 'security_notes',
      mandatory: true,
      visible: true
    },
    {
      field: 'caller_id',
      readOnly: true  // Lock caller field when category is security
    },
    {
      field: 'assignment_group',
      readOnly: true  // Lock assignment group when category is security
    },
    {
      field: 'priority',
      readOnly: true  // Lock priority when category is security
    }
  ],
  relatedListActions: [
    {
      // Using plain GUID for system relationships 
      list: 'b9edf0ca0a0a0b010035de2d6b579a03', // Attachments
      visible: false
    },
    {
      // Using table.field format for reference fields
      list: 'x_snc_17sepapp1_expenseitem.expensereport', // Example reference field
      visible: true
    }
  ]
})
```

## actions array

Configure the actions \[sys\_ui\_policy\_action\] that the UI policy performs on fields.

Use the actions array within the UiPolicy object. Actions are processed in the order that they appear in the array. At least one of the `visible`, `readOnly`, `mandatory`, or `cleared` properties must be specified for each action in the array.

<table id="table_y3j_vtn_rhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field

</td><td>

String

</td><td>

Required. The name of the field to which the action applies.**Note:** If the specified field isn’t found on the form, the UI policy performs the action on the variable with the same name.

</td></tr><tr><td>

visible

</td><td>

Boolean or String

</td><td>

An option to control the visibility of the field.Valid values:

-   true: The field is visible.
-   false: The field is hidden.
-   'ignore': The field isn’t changed.

Default: ignore

</td></tr><tr><td>

readOnly

</td><td>

Boolean or String

</td><td>

An option to control access to edit the field.Valid values:

-   true: The field is read-only.
-   false: The field is editable.
-   'ignore': The field isn’t changed.

Default: ignore

</td></tr><tr><td>

mandatory

</td><td>

Boolean or String

</td><td>

An option to control whether the field is required.Valid values:

-   true: The field is required.
-   false: The field is optional.
-   'ignore': The field isn’t changed.

Default: ignore

</td></tr><tr><td>

cleared

</td><td>

Boolean

</td><td>

Flag that indicates whether the field should be cleared if the conditions of the policy are met.Default: false

</td></tr><tr><td>

table

</td><td>

String

</td><td>

The table to which the action applies, which overrides the table specified by the policy. If empty, the table specified by the policy applies.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

The value to set the field to if the policy conditions are met.

</td></tr><tr><td>

fieldMessage

</td><td>

String

</td><td>

A message to display about the field if the policy conditions are met.

</td></tr><tr><td>

fieldMessageType

</td><td>

String

</td><td>

A message type that determines how the field message is presented.Valid values:

-   error
-   info
-   warning
-   none

Default: none

</td></tr><tr><td>

valueAction

</td><td>

String

</td><td>

An action to perform on the field value.Valid values:

-   set\_value
-   clear\_value
-   ignore

Default: ignore

</td></tr></tbody>
</table>```javascript
actions: [
        {
            field: 'assignment_group',
            mandatory: true,
            value: 'Critical Response Team', // Set default value
            fieldMessage: 'This incident requires immediate attention from the Critical Response Team',
            fieldMessageType: 'error' // Show as error message
        },
        {
            field: 'urgency',
            value: '1', // Set to High urgency
            fieldMessage: 'Urgency has been automatically set to High',
            fieldMessageType: 'info'
        },
        {
            field: 'impact',
            value: '1', // Set to High impact
            fieldMessage: 'Impact has been automatically set to High',
            fieldMessageType: 'warning'
        }
    ]
```

## relatedListActions array

Configure the visibility of related lists \[sys\_ui\_policy\_rl\_action\] on a form for a UI policy.

Use the relatedListActions array within the UiPolicy object. Related list actions are processed in the order that they appear in the array. Either the list or visible property must be specified for each related list action in the array.

<table id="table_y3j_vtn_rhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

list

</td><td>

String

</td><td>

A reference to a related list on the form. If empty, the action applies to all related lists. This property is required if the visible property is not set.Format:

-   sys\_ID: The sys\_ID for the list. Use this format for custom queries, attachments, and system-defined related lists.
-   table.field: The table and field name associated for the list, such as `'incident.caller_id'`. Use this format for reference field-based relationships.

</td></tr><tr><td>

visible

</td><td>

Boolean or String

</td><td>

An option to control the visibility of the related list. This property is required if the list property is not set.Valid values:

-   true: The related list is visible.
-   false: The related list is hidden.
-   'ignore': The related list isn’t changed.

Default: ignore

</td></tr></tbody>
</table>```javascript
 relatedListActions: [
    {
      // Using plain GUID for system relationships 
      list: 'b9edf0ca0a0a0b010035de2d6b579a03', // Attachments
      visible: false
    },
    {
      // Using table.field format for reference fields
      list: 'x_snc_17sepapp1_expenseitem.expensereport', // Example reference field
      visible: true
    }
  ]
```

