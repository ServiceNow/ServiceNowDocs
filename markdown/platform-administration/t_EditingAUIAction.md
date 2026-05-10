---
title: Create a UI action
description: You can create a new UI action or edit an existing one.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [UI actions, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a UI action

You can create a new UI action or edit an existing one.

## Before you begin

Role required: ui\_action\_admin or admin

## About this task

You can add UI actions to tables and database views that are in the same scope as the UI action and tables that allow UI actions from another application scope to run on them.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

2.  Click **New** or open an existing record.

3.  Define the UI action by completing the fields.

    You may need to configure the form to see all the fields.

<table id="table_epb_5pl_hp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The text that appears on the button, link, or context menu item.**Note:** If the Action name and Name fields are both exactly the same in two different UI actions, they will be de-duplicated at runtime to prevent users from seeing two of the same actions.

</td></tr><tr><td>

Table

</td><td>

The table on which the UI action is available. By default, the UI action also appears on tables that extend the selected table \(for example, Task actions appear on the Incident table\). Select **Global** to make the action available on all tables.

</td></tr><tr><td>

Order

</td><td>

The order in which the UI action appears. The order applies to buttons from left to right and to menu actions from top to bottom.

</td></tr><tr><td>

Action name

</td><td>

A unique name to use when referencing the UI action in scripts.**Note:** If the Action name and Name fields are both exactly the same in two different UI actions, they will be de-duplicated at runtime to prevent users from seeing two of the same actions.

</td></tr><tr><td>

Active

</td><td>

An option to enable the UI action when selected. To disable a UI action, clear the check box.

</td></tr><tr><td>

Show insert

</td><td>

An option to show a button on new records that have not been inserted.

</td></tr><tr><td>

Show update

</td><td>

An option to show a button on existing records.

</td></tr><tr><td>

Client

</td><td>

An option for the UI action to execute its script in the user's browser, not on the server. When enabled, the **Onclick** field appears above the Condition field.

</td></tr><tr><td>

Form button

</td><td>

An option to put a button on a form.

</td></tr><tr><td>

Form context menu

</td><td>

An option to put an item in a form context menu \(right-click the form header\).

</td></tr><tr><td>

Form link

</td><td>

An option to put a link in the Related Links section of a form.

</td></tr><tr><td>

Form style

</td><td>

-   Primary—Colors the UI Action blue.
-   Destructive—Colors the UI Action red.
-   Unstyled—Does not color the UI Action.


</td></tr><tr><td>

List banner button

</td><td>

An option to put a button in the banner of a list.**Note:** List banner buttons are not intended to support record-specific conditions, so only the first row is considered when the condition is evaluated to determine whether the button will show for the list. Do not use record-specific conditions \(e.g., current.getValue\('state'\) === 'closed'\) in list banner button UI Actions.

</td></tr><tr><td>

List bottom button

</td><td>

An option to put a button at the bottom of a list.**Note:** List bottom buttons show regardless of condition and are evaluated per record on execution.

</td></tr><tr><td>

List context menu

</td><td>

An option to put an item in a list field context menu \(right-click a cell in a list\).

</td></tr><tr><td>

List choice

</td><td>

An option to put an item in the action choice list at the bottom of a list.**Note:** List bottom buttons, like list choice actions, show regardless of condition and are evaluated per record on execution.

</td></tr><tr><td>

List link

</td><td>

An option to put a link in the Related Links section at the bottom of a list.

</td></tr><tr><td>

List style

</td><td>

-   Primary—Colors the UI Action blue.
-   Destructive—Colors the UI Action red.
-   Unstyled—Does not color the UI Action.


</td></tr><tr><td>

Overrides

</td><td>

A UI action that this UI action overrides.

</td></tr><tr><td>

Messages

</td><td>

Text strings that the UI action can use as a key to look up a localized message alternative from the Message \[sys\_ui\_message\] table. Each message key is on a separate line in the Messages field. The instance looks for a localized message string anytime the UI action makes a getMessage\(msg\) call where the msg string matches a key in the Messages field.

</td></tr><tr><td>

Comments

</td><td>

Descriptive content regarding this UI action.

</td></tr><tr><td>

Hint

</td><td>

The text that appears when a user points to the UI action control.

</td></tr><tr><td>

Onclick

</td><td>

The name of the JavaScript function to run when the UI action is executed. The function is defined in the **Script** field.

</td></tr><tr><td>

Condition

</td><td>

A JavaScript conditional statement that restricts when a UI action appears. Conditions always run on the server.**Note:**

-   The current object is not available for conditions on a list context menu. If the **List context menu** option is selected, any use of **current** on these actions is ignored.
-   You can reference the parent record for the UI action conditions on a related list button. For example, to disable the **New** and **Edit** buttons on the Affected CIs related list for closed changes, copy the global m2m UI actions to the task\_ci table and add a condition of **parent.active**.
-   If you leave one of the fields empty that you specify in your condition statement, that condition defaults to **true**.


</td></tr><tr><td>

Script

</td><td>

The script to run when the UI action is executed. Function names must be unique.

</td></tr><tr><td colspan="2">

Workspace

</td></tr><tr><td>

Workspace Form Button

</td><td>

An option to make the UI action appear on the list of UI actions in a workspace.

</td></tr><tr><td>

Workspace Form Menu

</td><td>

An option to make the UI action appear as a list item in the menu associated with UI actions in a workspace.

</td></tr><tr><td>

Format for Configurable Workspace

</td><td>

An option to use the UI action in a Configurable Workspace. If cleared, the UI action applies in Legacy Workspaces.

</td></tr><tr><td>

Workspace Client Script

</td><td>

A script to run when the UI action is executed in workspaces.

</td></tr><tr><td colspan="2">

Requires role

</td></tr><tr><td>

Role

</td><td>

The roles required for the UI action to apply. Users must have at least one of the roles for the UI action to apply.

</td></tr><tr><td colspan="2">

Related lists on the form view

</td></tr><tr><td>

UI Action Visibility

</td><td>

The views of the form that the UI action applies to. Use this option to restrict the UI action to form views that you specify. A UI action is available for the specified view according to the following rules:1.  If there are no visibility rules, the action appears on all views.
2.  Any exclude rule on a given view means that the action does not appear on that view.
3.  If there is at least one include rule, then the action appears only on views that are specifically included.


</td></tr><tr><td>

Versions

</td><td>

All versions of the UI action. Use this list to compare versions or to revert to a previous version.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.

    **Note:** If the UI action is enabled to run on the client side, wrap it in a function. Otherwise, the contents of the **Script** field runs when the page loads.


## Example

As part of a UI action script, you can redirect a user to a URL. For example, you might add links to a form or open a new record after it is created from a UI action. To redirect a user to a URL from a UI action, use this syntax in the **Script** field to define the redirect link:

```javascript
action.setRedirectURL ( '[http://www.mysite.com/mypage.htm](http://www.mysite.com/mypage.htm)' );
```

To direct a user to a record, use this syntax, where **new\_record** is the variable name for the [GlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md):

```javascript
action.setRedirectURL (new_record );
```

**Parent Topic:**[Defining UI actions](../concept/c_UIActions.md)

