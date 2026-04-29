---
title: Saved flow triggers
description: Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Saved flow triggers

Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

## Benefits

Save flow triggers to gain these benefits:

-   Allow flow authors to select predefined trigger definitions without the hassle of creating a trigger.
-   Push changes to every flow that uses a saved trigger rather than having to update each flow manually.
-   Reuse trigger definitions in multiple flows.

## UI elements

The Workflow Studio home page displays a **Triggers** option in the list of available components and the list of new components.

![Interface for the configure the trigger with numbered callouts for specific UI elements. For a description of the UI elements, see the list in the following text.](../images/trigger-definition.png "Screen to create a record based trigger")

A Workflow Studio **Create trigger** tab consists of these elements:

-   **1. Publish and more actions**

    Publish the trigger for consumption or access the More actions menu to delete the trigger, edit the trigger properties, view flows that are using the trigger, or force save your changes.

-   **2. View options**

    View the draft version of the trigger for all latest changes or view the published trigger.

-   **3. Redo and undo buttons**

    Redo or undo an action that you have performed while creating the trigger.

-   **4. Auto-save icon**

    View if and when your changes are automatically saved.

-   **5. Trigger type &amp; table section**

    Select the trigger type and table from the available options.

    For more information about trigger types, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

    **Note:** Starting in the Yokohama release, only the record-based triggers are supported for saved flow triggers.

-   **6. Conditions section**

    Specify the conditions for the trigger. Add more conditions as you need.

    You can allow flow authors to view the conditions or to view and add more conditions when they use the saved trigger in a flow. The changes don't affect the saved trigger.

-   **7. Advanced Options section**

    Specify the user session requirements needed to start a flow in the **Advanced Options** section.

    -   **When to run the flow**

        Determine the type of session that can trigger the flow, whether to run the flow when triggered by certain users, and which tables can trigger the flow.

        |Option|Description|
        |------|-----------|
        |Only Run for Non-Interactive Session|Flow that is triggered only in non-interactive sessions. See [Non-interactive sessions](https://www.servicenow.com/docs/access?context=c_NonInteractiveSessions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).|
        |Only Run for User Interactive Session|Flow that is triggered only in interactive sessions.|
        |Run for Both Interactive and Non-Interactive Sessions|Flow that is triggered in all sessions.|

        |Option|Description|
        |------|-----------|
        |Do not run if triggered by the following users|Flow that doesn't trigger for a selected list of users. Select the Add User icon \(![Add User Icon](../images/icon-select-users.png)\) to add users to the list.|
        |Only run if triggered by the following users|Flow that triggers only for a selected list of users. Select the Add User icon \(![Add User Icon](../images/icon-select-users.png)\) to add users to the list.|
        |Run for any user|Flow that runs for any user.|

        |Option|Description|
        |------|-----------|
        |Run only on current table|Flow that is triggered only for the selected table.|
        |Run on current and extended tables|Flow that is triggered for the selected table and any extended tables.|

    -   **Where to run the flow**

        Determine whether to run the flow in the background or in the current session.

<table id="table_qhf_fh1_phb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run flow in background \(default\)

</td><td>

Flow that runs asynchronously in the background. Use this option for flows that don't require immediate updates and to allow other system processes to run at the same time.

</td></tr><tr><td>

Run flow in foreground

</td><td>

Flow that runs synchronously in the current session. Use this option to provide immediate updates to an end user. For example, if a flow opens a task after the previous task closes, use this option to open the next task immediately after a user closes one.**Note:** Running a flow in foreground may block the current session thread and prevent user input until the flow finishes. Avoid running flows in the foreground when they contain actions that cannot be interrupted, such as actions that run script. Actions or flow logic that pause a flow will not block a session.

</td></tr></tbody>
</table>    You can allow the users to view and modify the advanced options when they use the saved trigger in a flow. If a user modifies the advanced options, any future changes that you make to the trigger doesn't affect the user modified options.


**Related topics**  


[Create a saved record based trigger](../task/create-saved-trigger.md)

[Edit a saved trigger](../task/edit-saved-trigger.md)

[Delete a saved trigger](../task/delete-saved-trigger.md)

