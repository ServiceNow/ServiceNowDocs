---
title: Declarative actions glossary
description: Refer to this glossary for definitions to terminology associated with declarative actions.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Declarative actions glossary

Refer to this glossary for definitions to terminology associated with declarative actions.

<table id="table_isv_zdm_d1c"><thead><tr><th>

Action field

</th><th>

Description

</th><th>

Action model field appears

</th></tr></thead><tbody><tr><td>

Action label

</td><td>

The default label that appears on the button at runtime.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Action name

</td><td>

A unique identifier of the action that populates automatically based on the action label used to avoid duplication at runtime.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Active

</td><td>

Setting that determines whether an action appears.Default: true

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

Defaults to your current application scope. Application scope that the action is tied to.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

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

Specify client action

</td><td>

Applicable when the**Implemented as** field is set to **UXF client action**. The field contains a payload to dispatch the internal event when the action is triggered and enables client action selection.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Table

</td><td>

An action appears only on the table that it's applied to. If set to **Global**, the action appears regardless of the table.Required

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

View

</td><td>

An action appears only on the forms or lists with the specified view. If left empty, the action appears regardless of view.

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
-   Field decorator
-   Related list

</td></tr><tr><td>

Tooltip

</td><td>

Text that appears when you move to the actions' tooltip icon.

</td><td>

-   Attachment
-   Form
-   Field decorator
-   Related list

</td></tr><tr><td>

Description

</td><td>

Details of the action.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Client script

</td><td>

Applicable when the **Implemented as** field is set to **client script**. Executes client-side scripts that join form or list functions.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr><tr><td>

Server script

</td><td>

Applicable when the **Implemented as** field is set to **server script**. Executes server-side scripts such as creating, deleting, or reassigning a record.

</td><td>

-   Attachment
-   Form
-   List
-   Field decorator
-   Related list

</td></tr></tbody>
</table>