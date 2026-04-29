---
title: Declarative actions glossary
description: Refer to this glossary for definitions to terminology associated with declarative actions.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Declarative actions glossary

Refer to this glossary for definitions to terminology associated with declarative actions.

<table id="table_isv_zdm_d1c"><thead><tr><th>

Action assignment field

</th><th>

Description

</th><th>

Action model field appears

</th></tr></thead><tbody><tr><td>

Action label

</td><td>

Displays the default label on the button at runtime.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Action name

</td><td>

Populates a unique identifier for the action automatically based on the action label.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Active

</td><td>

Determines whether an action appears.Default: true

Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Application

</td><td>

Associates the action with an application scope.Defaults to your current application scope.

Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Button type

</td><td>

Determines which button variant displays at runtime.Default: Primary

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Client Script

</td><td>

Applicable when the Implemented as field is set to **Client Script**.

Executes client-side scripts that join form or list functions.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Decorator applies to

</td><td>

Determines where the decorator should appear. Only three decorators may appear on a single field at one time.Default: Field type

Required

</td><td>

Field decorator

</td></tr><tr><td>

Description

</td><td>

Describes what the action does for future reference.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Enable for all configurable experiences

</td><td>

Determines if an action should appear in all experiences or only in specified experiences. If true, the action appears in any applicable form regardless of experience.Default: false

</td><td>

Form

</td></tr><tr><td>

Experience restricted

</td><td>

Determines if an action should appear in all experiences or only in specified experiences. If true, the action only appears in specified experiences.Default: false

</td><td>

-   List
-   Related list
-   Field decorator

</td></tr><tr><td>

Field Name

</td><td>

Applicable when the Decorator applies to field is set to **Specific field**.

Determines the specific field that should have the decorator appear.Available options are limited to columns available on the selected table.

Required

</td><td>

Field decorator

</td></tr><tr><td>

Field type

</td><td>

Applicable when the Decorator applies to field is set to **Field type**.

Determines which field type displays the decorator.Available field types:

-   Domain ID
-   List
-   Price
-   Date
-   Date/Time
-   Decimal
-   Document ID
-   Email
-   Floating point number
-   Integer
-   Password \(1-way encrypted\)
-   Phone Number
-   Phone Number \(E164\)
-   Reference
-   String

Field decorators don't support string fields that appear as multiple line text fields at runtime.

Required

</td><td>

Field decorator

</td></tr><tr><td>

Group

</td><td>

Applicable when the Group By field is set to true.Determines which group to add the action to.

Required

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Group By

</td><td>

Determines whether to add the action to a group displayed as a split button at runtime.Default: false

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Implemented as

</td><td>

Determines whether the action is a server script, client script, or UXF client action.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Order

</td><td>

Sets the display order of the action. An action with an order lower than other actions will appear closer to the front.Default: 0

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Server Script

</td><td>

Applicable when the Implemented as field is set to **Server Script**.Executes server-side scripts such as creating, deleting, or reassigning a record.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Specify client action

</td><td>

Applicable when the Implemented as field is set to **UXF Client Action**.Determines the payload dispatched when the action is triggered.

Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Table

</td><td>

Determines the table where the action appears. If set to **Global \[global\]**, the action appears regardless of the table.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Tooltip

</td><td>

Displays text when you hover over the action.

</td><td>

-   Attachment
-   Form
-   Field decorator
-   Related list

</td></tr><tr><td>

UI interaction

</td><td>

Applicable when the Implemented as field is set to **UI interaction**.Determines the UI interaction to execute when the action is triggered.

Required

</td><td>

-   Form
-   List
-   Related List

</td></tr><tr><td>

UXF Client Action

</td><td>

Applicable when the Implemented as field is set to **UXF Client Action**.Executes a page-level event in UI Builder.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

View

</td><td>

Determines the view where the action appears. If left empty, the action appears regardless of view.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr></tbody>
</table><table id="table_ywr_gvs_t3c"><thead><tr><th>

Condition field

</th><th>

Description

</th><th>

Action model field appears

</th></tr></thead><tbody><tr><td>

Client Conditions

</td><td>

Defines the client-side conditions that evaluate whether the action appears.

</td><td>

-   Attachment
-   Field decorator
-   Form

</td></tr><tr><td>

Dynamic Record Conditions

</td><td>

Applicable when the Enable Dynamic Evaluation field is set to true.Defines record-based conditions based on the table's columns that determine whether the action appears.

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Dynamic Script Conditions

</td><td>

Applicable when the Enable Dynamic Evaluation field is set to true.Defines a client-side JavaScript expression that determines whether the action appears. List actions have access to the current record. Related list actions have access to the parent record.

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Enable Dynamic Evaluation

</td><td>

Applicable when the Experience Restricted and Record Selection Required fields are set to true.Determines whether dynamic script and record conditions can evaluate whether the action appears.

</td><td>

-   List
-   Related List

</td></tr><tr><td>

Record Conditions

</td><td>

Defines record-based conditions that determine whether the action is returned to the client.

</td><td>

-   Attachment
-   Field decorator
-   Form

</td></tr><tr><td>

Required user role names

</td><td>

Determines which roles can view the action.Default: snc\_internal

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Requires create access

</td><td>

Requires you to have create access to view the action.Default: false

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Requires delete access-l

</td><td>

Requires you to have delete access to view the action.Default: false

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Requires read access

</td><td>

Requires you to have read access to view the action.Default: true

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Required write access

</td><td>

Requires you to have write access to view the action.Default: false

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Script Condition

</td><td>

Defines a server-side script that determines whether the action is returned to the client for rendering.Form actions have access to the current record, script includes, and the GlideRecord API. Related list actions have access to the parent record.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Scripted Client Condition

</td><td>

Defines a client-side JavaScript expression that dynamically determines whether the action appears. Supports dot-walking and string interpolation using `{{variable}}` syntax.

</td><td>

-   Form
-   Field decorator

</td></tr></tbody>
</table><table id="table_vm4_sdt_t3c"><thead><tr><th>

Related list

</th><th>

Description

</th><th>

Action model field appears

</th></tr></thead><tbody><tr><td>

Action Configurations

</td><td>

Groups actions in an experience. Must be referenced on the corresponding form or list page to display the actions.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Action Exclusions

</td><td>

Defines the tables and views where the action is hidden.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Action Model Fields

</td><td>

Provides contextual runtime data based on the action model.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr><tr><td>

Form Action Layout Item

</td><td>

Determines how the action appears at runtime. Created automatically for any new form actions formatted for Configurable Workspace.

</td><td>

Form

</td></tr><tr><td>

UX Add-on Event Mappings

</td><td>

Applicable when the Implemented as field is set to **UXF Client Action**.Maps an action to a UXF event on a specific page or controller. Can remap the payload to a new structure.

</td><td>

-   Attachment
-   Field decorator
-   Form
-   List
-   Related List

</td></tr></tbody>
</table>