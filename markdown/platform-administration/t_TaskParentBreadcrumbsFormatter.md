---
title: Parent breadcrumbs formatter
description: The parent breadcrumbs formatter on the Task table provides breadcrumbs that show the parent or parents of the current task. This formatter can be used also on any table that extends Task.You can customize the parent breadcrumbs formatter to control what breadcrumbs appear.The parent breadcrumbs formatter can be used on non-Task tables as long as the table has a reference to itself through a field called parent.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Formatters, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Parent breadcrumbs formatter

The parent breadcrumbs formatter on the Task table provides breadcrumbs that show the parent or parents of the current task. This formatter can be used also on any table that extends Task.

## Before you begin

Role required: personalize\_form

## About this task

To add the parent breadcrumbs formatter to a form, configure the form and add **Parent Breadcrumbs** to the desired location. The breadcrumbs show only six levels of parents. If more levels exist, the breadcrumbs display an ellipsis \('''...'''\).

The **Parent** reference field also has to contain a value for the breadcrumbs to appear. You may need to configure the form to contain the **Parent** field as well.

![Problem Task showing breadcrumbs and the Parent reference field](../image/ParentBreadcrumbReferenceField.png "Breadcrumbs")

**Parent Topic:**[Using formatters](../concept/c_Formatters.md)

## Customize the parent breadcrumbs formatter

You can customize the parent breadcrumbs formatter to control what breadcrumbs appear.

### Before you begin

Role required: ui\_macro\_admin

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Formatters**.

2.  Select **Parent Breadcrumbs**.

3.  Click **View UI Macro for this Formatter** to view or modify the underlying formatter.

    By default, the breadcrumb uses the default display field, **gr.getDisplayValue\(\),** as the link in the breadcrumb. To customize this, add the following line, replacing the **fieldName** parameter with the desired field name \(not the field label\):

    ```
    pc.setLabelField("fieldName")
    ```

    If a user points to a breadcrumb, the short description for that record appears as a hint by default. To display alternate hints for the breadcrumb, add the following line, replacing the **fieldName** parameter with the desired field name \(not the field label\):

    ```
    pc.setTitleField("fieldName")
    ```

    Be sure to add these lines in the proper location, as shown in the following example:

    ```
    //parent crumb functions - script include 
    var pc = new ParentCrumbs(now_GR);
    pc.setLabelField("short_description");
    
    //override the default display field to be used for label
    pc.setTitleField("number");
    
    //override default short_description hover text 
    var crumbs = pc.getCrumbs();
    ```

    ![Customized parent breadcrumb](../image/ParentBreadcrumbsCustomized.png)


## Use the parent breadcrumbs formatter on non-Task tables

The parent breadcrumbs formatter can be used on non-Task tables as long as the table has a reference to itself through a field called **parent**.

### Before you begin

Role required: ui\_macro\_admin

### About this task

To make the formatter available for a different table, duplicate the formatter used by the Task table:

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Formatters**.

2.  Select **Parent Breadcrumbs**.

3.  Set the **Table** field to the appropriate table.

4.  Right-click the form header and choose **Insert**.

5.  Add the new formatter to the appropriate form.


