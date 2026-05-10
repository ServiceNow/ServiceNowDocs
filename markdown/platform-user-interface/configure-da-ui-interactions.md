---
title: Trigger a UI interaction from a declarative action
description: Trigger a UI interaction from a declarative action to extend a page without taking ownership.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Trigger a UI interaction from a declarative action

Trigger a UI interaction from a declarative action to extend a page without taking ownership.

## Before you begin

Complete the following actions:

1.  Create a UI interaction in UI Builder. For instructions, see [Create a UI interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-ui-interaction-show-alert.md).
2.  Create a declarative action and add the button to a workspace. For instructions, see [Creating declarative action buttons](../concept/creating-declarative-actions.md).

Role required:

-   **ui\_interaction\_admin**

    Provides full CRUD permissions and is inherited by admin and ui\_builder\_admin.

-   **ui\_interaction\_developer**

    Provides permissions to create, read, and update but not to delete UI interactions or their inputs.


## About this task

UI interactions are reusable flows that combine UI elements and logic into a single unit. They help you avoid repeating the same wiring across multiple pages and make your designs easier to maintain.

A UI interaction defines what you want to happen, and how you apply a UI interaction defines how and when it happens. You can trigger UI interactions from page events in UI Builder or from declarative actions.

-   Trigger a UI interaction from a declarative action if you need a button on a form or list without page customization.
-   Trigger a UI interaction from a UI Builder page event to customize buttons and components on a page you own.

A UI interaction can be used instead of a UXF client action to simplify configuration since there's no need to configure add-on event mapping on a corresponding UI Builder page.

For a detailed overview of UI interactions, see [UI interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-ui-interactions.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** and select **Form Actions**, **List Actions**, or **Related List Actions**.

    **Note:** UI interactions are only available for form, list, and related list actions.

2.  From the Action Assignment list, select an action.

    An Action Assignment record opens.

3.  In the Implemented as field, select **UI interaction**.

    A new field named UI interaction appears.

    ![UI interaction field](../image/da-ui-interaction-field.png)

4.  In the UI interaction field, select a UI interaction.

    The Configure inputs dialog box opens with the UI interaction's default values.

    Inputs define the data parameters the UI interaction needs to execute.

    The fields displayed in the Configure inputs dialog box depend on the inputs configured for the selected UI interaction in UI Builder. If no inputs were defined, the Configure inputs dialog box doesn't open.

    For example, a UI interaction to create a new record may require you to define an input for the table of the new record.

    ![Configure inputs dialog box](../image/da-configure-inputs.png)

5.  To define a static value for an input, enter a specified value.

    For example, if the selected UI interaction to create a new record defines an input for the table of the new record and you want to pass data from the Incident \[incident\] table, enter `incident`.

6.  Define a dynamic value for an input.

    1.  Select the data icon \(![data icon](../image/da-data-icon.png)\).

    2.  Enter a value encapsulated by double opening and closing braces.

        Use values from the Action Model Definition \[sys\_declarative\_action\_model\_definition\] table for the action type you're configuring, such as Form, List, or Related List.

    For example, if the selected UI interaction to create a new record defines an input for the table of the new record and you want to pass data dynamically from the current table, enter `{{table}}`.

7.  Select **Save** to save changes and close the Configure inputs dialog box.

8.  Select **Update**.


## Result

When the form or list button is selected, the specified inputs pass data to the UI interaction, and the UI interaction performs the action it was configured to do.

