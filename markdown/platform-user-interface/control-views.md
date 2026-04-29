---
title: Control when the system displays a view
description: Administrators can create rules that determine the conditions for when the system should display a form or list in a specified view. Administrators can also restrict views by user role.You can use a script to control the form view used by different roles.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View management, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Control when the system displays a view

Administrators can create rules that determine the conditions for when the system should display a form or list in a specified view. Administrators can also restrict views by user role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **View Rules**.

2.  Click **New**.

3.  Complete the form.

    |Field|Input value|
    |-----|-----------|
    |Name|Specify an identifying name for the rule. This field is case-sensitive and must match exactly the view name.|
    |Active|Select this option to apply the view rule according to the conditions you specified. If unchecked, the view rule is not be applied.|
    |Advanced|Select this option to specify a code-based condition instead of using the condition builder. Selecting this option displays the **Script** field and hides the **Match conditions**, **Conditions**, and **View** fields.|
    |Match Conditions|Select whether **Any** or **All** of the conditions must be met. The system hides this field when you create an advanced View Rule.|
    |Conditions|Use the condition builder to determine when the view is applied. The system hides this field when you create an advanced View Rule.|
    |Application|Displays the application to which the View Rule record belongs.|
    |Table|Select the table on which this view rule is applied. The list shows only tables and database views that are in the same scope as the view rule|
    |Device type|Select which interface this view rule applies to.|
    |View|Enter the name of the View you are creating a rule for. The system hides this field when you create an advanced View Rule.|
    |Script|Enter a script to determine when to display a particular view. The system only displays this field when you create an advanced View Rule.|

4.  Click **Submit**.


**Parent Topic:**[View management](../concept/view-management-overview.md)

## Restrict view by role

You can use a script to control the form view used by different roles.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

Name: `Restrict View by Role`

Type: **System UI** &gt; **View Rules**

Table: `Any`

Description: Generally the view used on a form is controlled by either specifying the **sysparm\_view** parameter in the url or module properties, or by inheriting the view from the previous form or list. Sometimes this does not apply, such as when opening a referenced field form from a record producer. In this case, you may want to control the view of the form based on roles. This script assumes there is a view called **ess** available to the current table.

Parameters:

-   **view** - A string containing the name of the current view.
-   **is\_list** - A Boolean value indicating whether this is a list view.

Script:

```
(function overrideView(view, is_list) {
//Force non-itil users to use the ess view
if (gs.hasRole("itil"))
{return;}
if (view.startsWith("ess"))
{return;}
// do not change view if it starts with sys_ (e.g. sys_ref_list)
if (view.startsWith("sys_"))
{return;}
answer = "ess"; // set the new view to answer
})(view, is_list);
```

