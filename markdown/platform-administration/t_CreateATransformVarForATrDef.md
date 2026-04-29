---
title: Create a transform variable for a transform definition
description: Transform variables enable an administrator to apply the same definition to different fields in different ways.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default transform definitions, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a transform variable for a transform definition

Transform variables enable an administrator to apply the same definition to different fields in different ways.

## About this task

Transform variables contain values used by a script to perform a field transformation. Scripts and variables can be created in either order, but the script must use the transform variables. Transform variables are populated with values when a user configures a transform type.

## Procedure

1.  In the Transform Definition record, click **New** in the **Transform Variables** Related List.

2.  Complete the form.

    Important considerations for completing a form:

    -   The Column name is an entry in the fn\_transform\_var table for this variable. This becomes the variable in the script, in the form of variables.&lt;variable name&gt;. For example, `odd_even`.
    -   The value in the Label field appears as the variable field label in the Transform form. For example, `Odd/Even`.
    -   The field Type defines the field type of the variable value. Because the values for the variables used are **even** and **odd**, this is a type of string.
    -   The Order of the variables controls the order in which they are displayed in lists and records.
    -   This variable has a choice list with two options: **Even** and **Odd**. Select **Dropdown without - None** as the format for the list in the Choice field and define a Default value of **even** when the list is displayed.
    -   Create a Hint that becomes a tooltip for the variable in the Transform record.
3.  Right-click in the header bar and select **Save** from the context menu.

    The **Variables Choice List** Related List appears.

4.  Click **New** in the Variables Choice List and define the list options.

5.  Create records for **Even** and **Odd**.

    **Note:** The **Element** value is the same as the **Column** name in both selections for the choice list.

6.  Save the choice list variables and return to the transform definition form to create the script.


