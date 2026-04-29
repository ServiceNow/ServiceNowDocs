---
title: UI interaction toolbox steps
description: Find details about UI interaction toolbox steps, organized by interaction type, with step descriptions and any available outgoing events. Steps are added to a UI interaction using the toolbox in the UI interaction editor. The available steps depend on the type you selected when you created the UI interaction, whether Generic, Form, or List.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# UI interaction toolbox steps

Find details about UI interaction toolbox steps, organized by interaction type, with step descriptions and any available outgoing events. Steps are added to a UI interaction using the toolbox in the UI interaction editor. The available steps depend on the type you selected when you created the UI interaction, whether Generic, Form, or List.

## Available for all interaction types

The following steps are available regardless of whether your UI interaction type is Generic, Form, or List.

Steps that show **None** in the Events column connect directly to the End node or the next step. They execute and do not return a confirmation that they have finished. To continue building the interaction after one of these steps, use an **And** branch.

Steps that show **Success and/or Error** events allow you to define what happens next depending on the outcome, giving you full control over the interaction flow.

<table id="table_rgp_lhl_m3c"><thead><tr><th>

Step

</th><th>

Category

</th><th>

Description

</th><th>

Events

</th></tr></thead><tbody><tr><td>

Add alert notification

</td><td>

Alert

</td><td>

Adds an alert notification banner to the UI.

</td><td>

Alert action selected

</td></tr><tr><td>

If/Else

</td><td>

Logic

</td><td>

Evaluates conditions to branch the interaction flow. Branches evaluate top to bottom; the first true branch executes.

</td><td>

None

</td></tr><tr><td>

And

</td><td>

Logic

</td><td>

Executes multiple branches in parallel \(executes in order top to bottom\). Use when activities should happen at the same time.

</td><td>

None

</td></tr><tr><td>

Server script

</td><td>

Script

</td><td>

Executes a server-side script. Requires at least one user role.

</td><td>

Success, Error

</td></tr><tr><td>

Close workspace tab

</td><td>

Navigation

</td><td>

Closes the current Workspace tab. Can optionally prompt the user before closing.

</td><td>

None

</td></tr><tr><td>

Navigate to record

</td><td>

Navigation

</td><td>

Navigates the user to a specific record page.

</td><td>

None

</td></tr><tr><td>

Navigate to route

</td><td>

Navigation

</td><td>

Navigates the user to a custom \(non-record\) route.

</td><td>

None

</td></tr><tr><td>

Navigate to URL

</td><td>

Navigation

</td><td>

Navigates the user to a URL, optionally in a new browser tab.

</td><td>

None

</td></tr><tr><td>

Alert

</td><td>

Modal

</td><td>

Displays a modal that notifies users without requiring further input.

</td><td>

Modal closed

</td></tr><tr><td>

Confirm

</td><td>

Modal

</td><td>

Displays a modal prompting the user to confirm or cancel an action.

</td><td>

Modal closed, Primary button clicked, Secondary button clicked

</td></tr><tr><td>

Confirm and destroy

</td><td>

Modal

</td><td>

Displays a modal for irreversible actions \(such as deletion\), with directive language and warnings.

</td><td>

Modal closed, Primary button clicked, Secondary button clicked

</td></tr><tr><td>

User input

</td><td>

Modal

</td><td>

Displays a modal with fields for the user to complete. Fields can be added manually or sourced from a table.

</td><td>

Modal closed, Primary button clicked, Secondary button clicked

</td></tr><tr><td>

Create modal

</td><td>

Modal

</td><td>

Opens UI Builder component building to create a custom modal.

</td><td>

Modal closed; additional events can be defined by the custom component

</td></tr><tr><td>

Form

</td><td>

Modeless dialog

</td><td>

Displays a form inside a modeless dialog, allowing users to multi-task within their current context.

</td><td>

Modeless dialog closed, Primary button clicked, Secondary button clicked

</td></tr><tr><td>

Create modeless dialog

</td><td>

 

</td><td>

Opens UI Builder component building to create a custom modeless dialog.

</td><td>

Modeless dialog closed; additional events can be defined by the custom component

</td></tr></tbody>
</table>## Form interaction type only

The following steps are only available when the UI interaction type is set to Form. Form interactions require a form controller on the page and provide access to form-specific data and actions.

Field actions modify individual fields on the form. They do not produce success or error events; the step connects directly to the next step or end.

|Step|Description|Events|
|----|-----------|------|
|Add field message|Adds a message below a specified field.|None|
|Clear field message\(s\)|Clears messages from a specified field.|None|
|Clear field messages by type|Clears all field messages of a given type. For example, all info messages.|None|
|Clear field value|Clears the value of a specified field.|None|
|Set field invalid|Sets a field to valid or invalid.|None|
|Set field label|Updates the label of a specified field.|None|
|Set field placeholder value|Sets the placeholder value of a specified field.|None|
|Set field read-only|Sets a specified field to read-only.|None|
|Set field required|Sets a field as required or optional.|None|
|Set field value|Sets the value of a field. Can trigger or bypass dirty state.|None|
|Set field visibility|Shows or hides a specified field.|None|

Form actions operate on the form as a whole and include capabilities such as saving the form, validating the form, or displaying alerts.

|Step|Description|Events|
|----|-----------|------|
|Add form alert|Displays an alert at the top of the form component.|None|
|Clear all form alerts|Removes all alert notifications from the form.|None|
|Clear form alerts by type|Removes form alert notifications of a specified type.|None|
|Execute client script|Runs a client script on the form.|Success, Error|
|Execute UI action|Executes a UI action, client and server side, that has been enabled for Configurable Workspace.|Success, Error|
|Refresh form|Refreshes the form component.|Success|
|Save|Saves the form.|Success|
|Show/hide annotations|Shows or hides annotations on the form.|None|
|Submit form using UI action|Submits the form using a specified UI action.|Success, Error|
|Validate|Validates the form.|Success, Error|

## List interaction type only

The following steps are only available when the UI interaction type is set to List. List interactions require a list controller on the page and provide access to list-specific data and actions.

|Step|Description|Events|
|----|-----------|------|
|Execute client script|Runs a client script on the list.|Success, Error|
|Group by column|Groups the list by a specified column.|None|
|Refresh list|Refreshes the list component.|Success|
|Set query|Updates the encoded query of the list.|None|
|Sort|Sorts the list by a specified column, ascending or descending.|None|

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)

